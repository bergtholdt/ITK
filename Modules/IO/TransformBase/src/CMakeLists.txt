set(ITKIOTransformBase_SRCS
  itkCompositeTransformIOHelper.cxx
  itkTransformFileReader.cxx
  itkTransformFileWriterSpecializations.cxx
  itkTransformIOBase.cxx
  itkTransformIOFactory.cxx
  )

itk_module_add_library(ITKIOTransformBase ${ITKIOTransformBase_SRCS})
if (WIN32)
    set_target_properties(ITKIOTransformBase 
        PROPERTIES COMPILE_FLAGS "$<$<CONFIG:Release>:/GL->")
    set_target_properties(ITKIOTransformBase 
        PROPERTIES COMPILE_FLAGS "$<$<CONFIG:RelWithDebInfo>:/GL->")
    set_target_properties(ITKIOTransformBase 
        PROPERTIES COMPILE_FLAGS "$<$<CONFIG:Debug>:/GL->")
    set_target_properties(ITKIOTransformBase 
        PROPERTIES COMPILE_FLAGS "$<$<CONFIG:MinSizeRel>:/GL->")
endif(WIN32)