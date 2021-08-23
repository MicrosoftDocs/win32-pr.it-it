---
title: Funzione gluProject (Glu.h)
description: La funzione gluProject esegue il mapping delle coordinate dell'oggetto alle coordinate della finestra.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- Funzione gluProject OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324f6c896c225453bfc8bf2ebb4b8619707c498c75e1309ea24fc6557cdd3deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488810"
---
# <a name="gluproject-function"></a>Funzione gluProject

La **funzione gluProject esegue** il mapping delle coordinate dell'oggetto alle coordinate della finestra.

## <a name="syntax"></a>Sintassi


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objx* 
</dt> <dd>

Coordinata dell'oggetto x.

</dd> <dt>

*objy* 
</dt> <dd>

Coordinata dell'oggetto y.

</dd> <dt>

*objz* 
</dt> <dd>

Coordinata dell'oggetto z.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Matrice modelview corrente (come da una [**chiamata glGetDoublev).**](glgetdoublev.md)

</dd> <dt>

*projMatrix* 
</dt> <dd>

Matrice di proiezione corrente (come da una **chiamata glGetDoublev).**

</dd> <dt>

*Finestra* 
</dt> <dd>

Viewport corrente (come da una [**chiamata glGetIntegerv).**](glgetintegerv.md)

</dd> <dt>

*Winx* 
</dt> <dd>

Coordinata della finestra x calcolata.

</dd> <dt>

*Vinoso* 
</dt> <dd>

Coordinata della finestra y calcolata.

</dd> <dt>

*winz* 
</dt> <dd>

Coordinata della finestra z calcolata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è GL \_ TRUE.

Se la funzione ha esito negativo, il valore restituito è GL \_ FALSE.

## <a name="remarks"></a>Commenti

La **funzione gluProject** trasforma le coordinate dell'oggetto specificato in coordinate della finestra usando *modelMatrix*, *projMatrix* e *viewport*. Il risultato viene archiviato in *winx*, *winy* e *winz*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glGetDoublev**](glgetdoublev.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluUnProject**](gluunproject.md)
</dt> </dl>

 

 





