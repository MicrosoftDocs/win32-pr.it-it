---
title: funzione gluBuild1DMipmaps (Glu. h)
description: La funzione gluBuild1DMipmaps crea mipmap 1-D.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- funzione gluBuild1DMipmaps OpenGL
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
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301356"
---
# <a name="glubuild1dmipmaps-function"></a>gluBuild1DMipmaps (funzione)

La funzione **gluBuild1DMipmaps** crea mipmap 1-D.

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

Trama di destinazione. Deve essere una \_ trama GL \_ 1D.

</dd> <dt>

*componenti* 
</dt> <dd>

Numero di componenti di colore nella trama. Deve essere 1, 2, 3 o 4.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza dell'immagine della trama.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Sono validi i valori seguenti: GL \_ Color \_ index, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance o GL \_ Luminance \_ alpha.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati per i *dati*. I valori seguenti sono validi: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int o GL \_ float.

</dd> <dt>

*data* 
</dt> <dd>

Puntatore ai dati dell'immagine in memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluBuild1DMipmaps** Ottiene l'immagine di input e genera tutte le immagini mipmap (usando [**gluScaleImage**](gluscaleimage.md)) in modo che l'immagine di input possa essere usata come immagine di trama mipmap. Viene quindi chiamata la funzione [**glTexImage1D**](glteximage1d.md) per caricare ogni immagine. Se la larghezza dell'immagine di input non è una potenza di due, l'immagine viene ridimensionata alla potenza più vicina di due prima che vengano generati i mipmap.

Un valore restituito pari a zero indica esito positivo. In caso contrario, viene restituito un codice di errore GLU (vedere [**gluErrorString**](gluerrorstring.md)).

Per una descrizione dei valori accettabili per il parametro *Format* , vedere **glTexImage1D**. Per una descrizione dei valori accettabili per il parametro di *tipo* , vedere [**glDrawPixels**](gldrawpixels.md).

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





