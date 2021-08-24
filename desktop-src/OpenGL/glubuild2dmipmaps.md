---
title: Funzione gluBuild2DMipmaps (Glu.h)
description: La funzione gluBuild2DMipmaps crea mipmap 2D.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- Funzione gluBuild2DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27dcf3d0e95b0b52d5b7f4c4ce0e5692f3fc856b81d9c1d82c9661a70e2f818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489651"
---
# <a name="glubuild2dmipmaps-function"></a>Funzione gluBuild2DMipmaps

La **funzione gluBuild2DMipmaps** crea mipmap 2D.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Trama di destinazione. Deve essere GL \_ TEXTURE \_ 2D.

</dd> <dt>

*Componenti* 
</dt> <dd>

Numero di componenti di colore nella trama. Deve essere 1, 2, 3 o 4.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza dell'immagine della trama.

</dd> <dt>

*height* 
</dt> <dd>

Altezza dell'immagine della trama.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Deve essere uno dei seguenti: GL \_ COLOR \_ INDEX, \_ GL RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE o GL \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati per *i dati*. Deve essere uno dei seguenti: GL \_ UNSIGNED \_ BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT o GL \_ FLOAT.

</dd> <dt>

*data* 
</dt> <dd>

Puntatore ai dati dell'immagine in memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluBuild2DMipmaps** ottiene l'immagine di input e genera tutte le immagini mipmap (usando [**gluScaleImage**](gluscaleimage.md)) in modo che l'immagine di input possa essere usata come immagine di trama mipmapped. Per caricare ognuna delle immagini, chiamare [**glTexImage2D**](glteximage2d.md). Se le dimensioni dell'immagine di input non sono di due, l'immagine viene ridimensionata in modo che sia la larghezza che l'altezza siano potenza di due prima che le mipmap siano generate.

Un valore restituito pari a zero indica l'esito positivo. In caso contrario, viene restituito un codice di errore GLU (vedere [**gluErrorString**](gluerrorstring.md)).

Per una descrizione dei valori accettabili per il *parametro format,* vedere **glTexImage2D**. Per una descrizione dei valori accettabili per *il tipo*, vedere [**glDrawPixels**](gldrawpixels.md).

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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





