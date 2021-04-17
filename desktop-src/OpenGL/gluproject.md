---
title: funzione gluProject (Glu. h)
description: La funzione gluProject esegue il mapping delle coordinate dell'oggetto alle coordinate della finestra.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- funzione gluProject OpenGL
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
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478023"
---
# <a name="gluproject-function"></a>gluProject (funzione)

La funzione **gluProject** esegue il mapping delle coordinate dell'oggetto alle coordinate della finestra.

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

Coordinata x dell'oggetto.

</dd> <dt>

*objy* 
</dt> <dd>

Coordinata y dell'oggetto.

</dd> <dt>

*objz* 
</dt> <dd>

Coordinata z dell'oggetto.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Matrice Modelview corrente (come da una chiamata [**glGetDoublev**](glgetdoublev.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

Matrice di proiezione corrente (come da una chiamata **glGetDoublev** ).

</dd> <dt>

*Viewport* 
</dt> <dd>

Viewport corrente (come da una chiamata [**glGetIntegerv**](glgetintegerv.md) ).

</dd> <dt>

*Winx* 
</dt> <dd>

Coordinata x della finestra calcolata.

</dd> <dt>

*vinoso* 
</dt> <dd>

Coordinata della finestra y calcolata.

</dd> <dt>

*winz* 
</dt> <dd>

Coordinata della finestra z calcolata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è GL \_ true.

Se la funzione ha esito negativo, il valore restituito è GL \_ false.

## <a name="remarks"></a>Commenti

La funzione **gluProject** trasforma le coordinate dell'oggetto specificato in coordinate della finestra usando *modelMatrix*, *projMatrix* e *viewport*. Il risultato viene archiviato in *Winx*, *vinoso* e *Winz*.

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

[**glGetDoublev**](glgetdoublev.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluUnProject**](gluunproject.md)
</dt> </dl>

 

 





