---
title: funzione gluQuadricCallback (Glu. h)
description: La funzione gluQuadricCallback definisce un callback per un oggetto quadrica.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- funzione gluQuadricCallback OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0c92e3cd4e723b59ee9060c5e2f33b710e7f69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518412"
---
# <a name="gluquadriccallback-function"></a>gluQuadricCallback (funzione)

La funzione **gluQuadricCallback** definisce un callback per un oggetto quadrica.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*qobj* 
</dt> <dd>

Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*che* 
</dt> <dd>

Callback da definire. L'unico valore valido è GLU \_ Error.



| Valore                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <dt>**\_errore Glu**</dt> </dl> | La funzione **gluQuadricCallback** viene chiamata quando viene rilevato un errore. Il suo singolo argomento è di tipo **GLEnum** e indica l'errore specifico che si è verificato. È possibile recuperare le stringhe di caratteri che descrivono questi errori con la chiamata a [**gluErrorString**](gluerrorstring.md) .<br/> |



 

</dd> <dt>

*FN* 
</dt> <dd>

Funzione da chiamare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare **gluQuadricCallback** per definire un nuovo callback che verrà usato da un oggetto quadrica. Se il callback specificato è già definito, viene sostituito. Se *FN* è **null**, qualsiasi callback esistente verrà cancellato.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





