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
        PROPERTIES COMPILE_FLAGS "/GL-")
endif(WIN32)