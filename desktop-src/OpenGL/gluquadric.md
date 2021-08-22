---
title: Funzione gluQuadricCallback (Glu.h)
description: La funzione gluQuadricCallback definisce un callback per un oggetto quadric.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- Funzione gluQuadricCallback OpenGL
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
ms.openlocfilehash: 36ce32bf041a59f272b18ebe17916963c4e5fd8d208da9d739468c88b9286dfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488791"
---
# <a name="gluquadriccallback-function"></a>Funzione gluQuadricCallback

La **funzione gluQuadricCallback** definisce un callback per un oggetto quadric.

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

Oggetto quadric (creato con [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*Che* 
</dt> <dd>

Callback da definire. L'unico valore valido è GLU \_ ERROR.



| Valore                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <dt>**ERRORE \_ GLU**</dt> </dl> | La **funzione gluQuadricCallback** viene chiamata quando viene rilevato un errore. Il singolo argomento è di tipo **GLenum** e indica l'errore specifico che si è verificato. Le stringhe di caratteri che descrivono questi errori possono essere recuperate con [**la chiamata gluErrorString.**](gluerrorstring.md)<br/> |



 

</dd> <dt>

*Fn* 
</dt> <dd>

Funzione da chiamare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare **gluQuadricCallback** per definire un nuovo callback che deve essere usato da un oggetto quadric. Se il callback specificato è già definito, viene sostituito. Se *fn* è **NULL,** qualsiasi callback esistente viene cancellato.

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

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





