---
title: funzione gluBuild2DMipmaps (Glu. h)
description: La funzione gluBuild2DMipmaps crea mipmap 2D.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- funzione gluBuild2DMipmaps OpenGL
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
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963921"
---
# <a name="glubuild2dmipmaps-function"></a>gluBuild2DMipmaps (funzione)

La funzione **gluBuild2DMipmaps** crea mipmap 2D.

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

Trama di destinazione. Deve essere di \_ trama GL \_ 2D.

</dd> <dt>

*componenti* 
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

Formato dei dati pixel. Deve essere uno dei seguenti: GL \_ Color \_ index, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance o GL \_ Luminance \_ alpha.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati per i *dati*. Deve essere uno dei seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int o GL \_ float.

</dd> <dt>

*data* 
</dt> <dd>

Puntatore ai dati dell'immagine in memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluBuild2DMipmaps** Ottiene l'immagine di input e genera tutte le immagini mipmap (usando [**gluScaleImage**](gluscaleimage.md)) in modo che l'immagine di input possa essere usata come immagine di trama mipmap. Per caricare tutte le immagini, chiamare [**glTexImage2D**](glteximage2d.md). Se le dimensioni dell'immagine di input non sono potenze di due, l'immagine viene ridimensionata in modo che sia la larghezza che l'altezza siano le potenze di due prima che vengano generati i mipmap.

Un valore restituito pari a zero indica esito positivo. In caso contrario, viene restituito un codice di errore GLU (vedere [**gluErrorString**](gluerrorstring.md)).

Per una descrizione dei valori accettabili per il parametro *Format* , vedere **glTexImage2D**. Per una descrizione dei valori accettabili per il *tipo*, vedere [**glDrawPixels**](gldrawpixels.md).

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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





