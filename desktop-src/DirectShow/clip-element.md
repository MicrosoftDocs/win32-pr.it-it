---
description: La clip epecifies un'origine multimediale.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Elemento clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe975113f370b13e50ba695d6fb3388a43c3a74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480996"
---
# <a name="clip-element"></a>Elemento clip

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

`clip`Epecifies un'origine multimediale.

## <a name="attributes"></a>Attributi

[**CLSID**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**Lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**Stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



|          |                                  |
|----------|----------------------------------|
| Padre   | [**tenere traccia**](track-element.md)   |
| Children | [**effetto**](effect-element.md) |



 

## <a name="remarks"></a>Commenti

L'attributo **CLSID** specifica il CLSID di un filtro di origine da utilizzare come origine. Non specificare gli attributi **src** e **CLSID** nello stesso `clip` elemento.

Specificare almeno un attributo di inizio-ora (**Start** o **mstart**) e un attributo dell'ora di arresto (**Stop** o **mstop**). Se uno degli attributi della fase di avvio non è specificato, il valore predefinito è 0 (l'inizio della sequenza temporale per l' **avvio** o l'inizio della clip per **mstart**). Se uno degli attributi dell'ora di arresto non è specificato, DES presuppone una frequenza di riproduzione normale e calcola di conseguenza l'ora di arresto non specificata. Se vengono specificate entrambe le ore di arresto, la riproduzione è più veloce o più lenta del normale, se necessario.

Nell'esempio seguente la durata della sequenza temporale è di sette secondi (**Stop** minus **Start**). Si presuppone una frequenza di riproduzione normale, quindi il tempo di arresto del supporto predefinito è di 10 secondi (durata più **mstart**).


```
<clip start="2" stop="9" mstart="3" />
```



Nell'esempio seguente l'ora di inizio del supporto viene impostata su 0, forzando la durata dei supporti su 10 secondi. La durata della sequenza temporale è di cinque secondi, quindi la clip viene riprodotta al doppio della normale frequenza.


```
<clip start="5" stop="10" mstop="10" />  
```



Se l'attributo **src** specifica un'immagine ancora, des tenta di caricare una serie di immagini ancora per creare un'animazione. Se, ad esempio, l'attributo **src** è IMAGE001.BMP, DES Cerca IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP e così via. Supponendo che esistano, vengono visualizzati in ordine numerico sequenziale, alla velocità specificata dall'attributo **framerate** .

## <a name="examples"></a>Esempi


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



