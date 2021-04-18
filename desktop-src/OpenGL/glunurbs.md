---
title: funzione gluNurbsCallback (Glu. h)
description: La funzione gluNurbsCallback definisce un callback per un oggetto logico B-spline (NURBS) non uniforme.
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- funzione gluNurbsCallback OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301258"
---
# <a name="glunurbscallback-function"></a>gluNurbsCallback (funzione)

La funzione **gluNurbsCallback** definisce un callback per un oggetto logico B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*juje* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*che* 
</dt> <dd>

Callback da definire. L'unico valore valido è GLU \_ Error. Il significato di GLU \_ Error significa che la funzione Error viene chiamata quando viene rilevato un errore. Il suo singolo argomento è di tipo **GLEnum** e indica l'errore specifico che si è verificato. Sono presenti 37 errori univoci per NURBS, denominato GLU \_ NURBS \_ ERROR1 tramite Glu \_ NURBS \_ ERROR37. Le stringhe di caratteri che descrivono questi errori possono essere recuperate con [**gluErrorString**](gluerrorstring.md).

</dd> <dt>

*FN* 
</dt> <dd>

Puntatore alla funzione di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Utilizzare **gluNurbsCallback** per definire un callback che deve essere utilizzato da un oggetto NURBS. Se il callback specificato è già definito, viene sostituito. Se *FN* è **null**, qualsiasi callback esistente verrà cancellato.

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

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





