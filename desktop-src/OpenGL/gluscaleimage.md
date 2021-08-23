---
title: Funzione gluScaleImage (Glu.h)
description: La funzione gluScaleImage ridimensiona un'immagine a dimensioni arbitrarie.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- Funzione gluScaleImage OpenGL
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
ms.openlocfilehash: 0a6bab8865dec475087743f658429fd633fc9bb1443da14bd1198e8a7c73b0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488741"
---
# <a name="gluscaleimage-function"></a>Funzione gluScaleImage

La **funzione gluScaleImage** ridimensiona un'immagine a dimensioni arbitrarie.

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

Formato dei dati pixel. Sono validi i valori simbolici seguenti: GL \_ COLOR \_ INDEX, GL \_ STENCIL \_ INDEX, GL DEPTH \_ \_ \_ COMPONENT, GL \_ RED, GL GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, \_ GL RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE e GL \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*widthin* 
</dt> <dd>

Larghezza dell'immagine di origine ridimensionata.

</dd> <dt>

*heightin* 
</dt> <dd>

Altezza dell'immagine di origine ridimensionata.

</dd> <dt>

*typein* 
</dt> <dd>

Tipo di dati per *datain*. Deve essere uno dei seguenti: GL \_ \_ UNSIGNED BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT o GL \_ FLOAT.

</dd> <dt>

*datain* 
</dt> <dd>

Puntatore all'immagine di origine.

</dd> <dt>

*widthout* 
</dt> <dd>

Larghezza dell'immagine di destinazione.

</dd> <dt>

*heightout* 
</dt> <dd>

Altezza dell'immagine di destinazione.

</dd> <dt>

*typeout* 
</dt> <dd>

Tipo di dati per *dataout.* Deve essere uno dei seguenti: GL \_ \_ UNSIGNED BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT o GL \_ FLOAT.

</dd> <dt>

*dataout* 
</dt> <dd>

Puntatore all'immagine di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è zero.

Se la funzione ha esito negativo, il valore restituito è un codice di errore GLU (vedere [**gluErrorString**](gluerrorstring.md)).

## <a name="remarks"></a>Commenti

La **funzione gluScaleImage** ridimensiona un'immagine pixel usando le modalità di archivio pixel appropriate per decomprimere i dati dall'immagine di origine e creare il pacchetto dei dati nell'immagine di destinazione.

Quando si compatta un'immagine, **gluScaleImage** usa un filtro casella per campionare l'immagine di origine e creare pixel per l'immagine di destinazione. Quando si ingrandire un'immagine, i pixel dell'immagine di origine vengono interpolati in modo lineare per creare l'immagine di destinazione.

Per una descrizione dei valori accettabili per i *parametri format*, *typein* e *typeout,* vedere [**glReadPixels.**](glreadpixels.md)

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

 

 





