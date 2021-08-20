---
title: Funzione gluBuild1DMipmaps (Glu.h)
description: La funzione gluBuild1DMipmaps crea mipmap 1D.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- Funzione gluBuild1DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c2b76a37fa7088835ad0238065b0647ff0beb973c1c3ffa1b892f6e0958d97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489691"
---
# <a name="glubuild1dmipmaps-function"></a>Funzione gluBuild1DMipmaps

La **funzione gluBuild1DMipmaps** crea mipmap 1D.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Trama di destinazione. Deve essere GL \_ TEXTURE \_ 1D.

</dd> <dt>

*Componenti* 
</dt> <dd>

Numero di componenti di colore nella trama. Deve essere 1, 2, 3 o 4.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza dell'immagine della trama.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. I valori seguenti sono validi: GL \_ COLOR \_ INDEX, GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, \_ GL RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE o GL \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati per i *dati*. Sono validi i valori seguenti: GL \_ UNSIGNED \_ BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT o GL \_ FLOAT.

</dd> <dt>

*data* 
</dt> <dd>

Puntatore ai dati dell'immagine in memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluBuild1DMipmaps** ottiene l'immagine di input e genera tutte le immagini mipmap (usando [**gluScaleImage**](gluscaleimage.md)) in modo che l'immagine di input possa essere usata come immagine di trama con mipmapped. Viene quindi chiamata la funzione [**glTexImage1D**](glteximage1d.md) per caricare ognuna delle immagini. Se la larghezza dell'immagine di input non è una potenza di due, l'immagine viene ridimensionata alla potenza più vicina di due prima che le mipmap siano generate.

Un valore restituito pari a zero indica l'esito positivo. In caso contrario, viene restituito un codice di errore GLU (vedere [**gluErrorString**](gluerrorstring.md)).

Per una descrizione dei valori accettabili per il *parametro format,* vedere **glTexImage1D.** Per una descrizione dei valori accettabili per il *parametro di tipo,* vedere [**glDrawPixels.**](gldrawpixels.md)

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





