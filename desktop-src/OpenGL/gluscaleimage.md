---
title: funzione gluScaleImage (Glu. h)
description: La funzione gluScaleImage ridimensiona un'immagine a una dimensione arbitraria.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- funzione gluScaleImage OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400213"
---
# <a name="gluscaleimage-function"></a>gluScaleImage (funzione)

La funzione **gluScaleImage** ridimensiona un'immagine a una dimensione arbitraria.

## <a name="syntax"></a>Sintassi


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Sono validi i valori simbolici seguenti: GL \_ Color \_ index, GL \_ stencil \_ index, GL \_ Depth \_ Component, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance e GL \_ Luminance \_ alpha.

</dd> <dt>

*Larghezza* 
</dt> <dd>

Larghezza dell'immagine di origine ridimensionata.

</dd> <dt>

*altezza* 
</dt> <dd>

Altezza dell'immagine di origine ridimensionata.

</dd> <dt>

*typein* 
</dt> <dd>

Tipo di dati per *dataIn*. Deve essere uno dei seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int o GL \_ float.

</dd> <dt>

*dataIn* 
</dt> <dd>

Puntatore all'immagine di origine.

</dd> <dt>

*Larghezza* 
</dt> <dd>

Larghezza dell'immagine di destinazione.

</dd> <dt>

*altezza* 
</dt> <dd>

Altezza dell'immagine di destinazione.

</dd> <dt>

*digitare* 
</dt> <dd>

Tipo di dati per i *dati*. Deve essere uno dei seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int o GL \_ float.

</dd> <dt>

*dati* 
</dt> <dd>

Puntatore all'immagine di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è zero.

Se la funzione ha esito negativo, il valore restituito è un codice di errore GLU (vedere [**gluErrorString**](gluerrorstring.md)).

## <a name="remarks"></a>Commenti

La funzione **gluScaleImage** ridimensiona un'immagine pixel usando le modalità di archivio pixel appropriate per decomprimere i dati dall'immagine di origine e comprimere i dati nell'immagine di destinazione.

Quando si compatta un'immagine, **gluScaleImage** usa un filtro Box per campionare l'immagine di origine e creare i pixel per l'immagine di destinazione. Quando si ingrandisce un'immagine, i pixel dell'immagine di origine vengono interpolati linearmente per creare l'immagine di destinazione.

Per una descrizione dei valori accettabili per il *formato*, *digitare* *e digitare i parametri,* vedere [**glReadPixels**](glreadpixels.md).

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> </dl>

 

 





