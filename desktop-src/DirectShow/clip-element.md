---
description: Il clip emette un'origine multimediale.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Elemento clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b94ffdbd3d9b49d961cdefdd64de9a212858c5da4859c3beddb77db0ab732d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655515"
---
# <a name="clip-element"></a>Elemento clip

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`clip`Epecifies a media source.

## <a name="attributes"></a>Attributi

[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Etichetta | Valore |
|----------|----------------------------------|
| Padre   | [**Traccia**](track-element.md)   |
| Children | [**Effetto**](effect-element.md) |



 

## <a name="remarks"></a>Commenti

**L'attributo clsid** specifica il CLSID di un filtro di origine da usare come origine. Non specificare gli attributi **src** e **clsid** all'interno dello stesso `clip` elemento.

Specificare almeno un attributo dell'ora di inizio (**start** o **mstart**) e un attributo dell'ora di arresto (**stop** o **mstop**). Se uno degli attributi dell'ora di inizio non è specificato, il valore predefinito è 0 (l'inizio della sequenza temporale per **start** o l'inizio del clip per **mstart).** Se uno degli attributi relativi all'ora di arresto non è specificato, DES presuppone una velocità di riproduzione normale e calcola di conseguenza l'ora di arresto non specificata. Se vengono specificati entrambi gli orari di arresto, la riproduzione è più veloce o più lenta del normale, se necessario.

Nell'esempio seguente la durata della sequenza temporale è di sette secondi (**stop** meno **start**). Si presuppone la frequenza di riproduzione normale, quindi l'ora di arresto del contenuto multimediale è impostata su 10 secondi (durata più **mstart).**


```
<clip start="2" stop="9" mstart="3" />
```



Nell'esempio successivo l'ora di inizio del supporto viene impostata su 0 per impostazione predefinita, forzando la durata del supporto su 10 secondi. La durata della sequenza temporale è di cinque secondi, quindi il clip viene riprodotto al doppio della frequenza normale.


```
<clip start="5" stop="10" mstop="10" />  
```



Se **l'attributo src** specifica un'immagine fisse, DES tenta di caricare una serie di immagini fisse per creare un'animazione. Ad esempio, se **l'attributo src** è IMAGE001.BMP, DES cerca IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP e così via. Supponendo che esistano, vengono visualizzati in ordine numerico sequenziale, alla frequenza specificata **dall'attributo framerate.**

## <a name="examples"></a>Esempi


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 



