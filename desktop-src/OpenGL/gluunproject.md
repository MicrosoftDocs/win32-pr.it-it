---
title: funzione gluUnProject (Glu. h)
description: La funzione gluUnProject esegue il mapping delle coordinate della finestra alle coordinate dell'oggetto.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- funzione gluUnProject OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302498"
---
# <a name="gluunproject-function"></a>gluUnProject (funzione)

La funzione **gluUnProject** esegue il mapping delle coordinate della finestra alle coordinate dell'oggetto.

## <a name="syntax"></a>Sintassi


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Winx* 
</dt> <dd>

Coordinata x della finestra da mappare.

</dd> <dt>

*vinoso* 
</dt> <dd>

Coordinata della finestra y da mappare.

</dd> <dt>

*winz* 
</dt> <dd>

Coordinata della finestra z da mappare.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Matrice Modelview (come da una chiamata [**glGetDoublev**](glgetdoublev.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

Matrice di proiezione, come da una chiamata **glGetDoublev** .

</dd> <dt>

*Viewport* 
</dt> <dd>

Viewport, come da una chiamata [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .

</dd> <dt>

*objx* 
</dt> <dd>

Coordinata x dell'oggetto calcolato.

</dd> <dt>

*objy* 
</dt> <dd>

Coordinata dell'oggetto y calcolato.

</dd> <dt>

*objz* 
</dt> <dd>

Coordinata dell'oggetto z calcolato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è GL \_ true.

Se la funzione ha esito negativo, il valore restituito è GL \_ false.

## <a name="remarks"></a>Commenti

La funzione **gluUnProject** esegue il mapping tra le coordinate della finestra specificata e le coordinate dell'oggetto utilizzando *modelMatrix*, *projMatrix* e *viewport*. Il risultato viene archiviato in *objX*, *objy* e *objz*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetDoublev**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluProject**](gluproject.md)
</dt> </dl>

 

 





