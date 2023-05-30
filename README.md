# matrix_gesture_detector-master
Update for Software Image Drag &amp; Drop (onDragEnd)

MatrixGestureDetector detects translation, scale and rotation gestures and combines them into Matrix4 object that can be used by Transform widget or by low level CustomPainter code. You can customize types of reported gestures by passing shouldTranslate, shouldScale and shouldRotate parameters.

The usage is as follows:

  MatrixGestureDetector(
    onMatrixUpdate: (Matrix4 m, Matrix4 tm, Matrix4 sm, Matrix4 rm) {
      setState(() {
        matrix = m;
      });
    },
    child: SomeWidgetThatUsesMatrix(
      matrix: matrix,
      ...
    )
  )
