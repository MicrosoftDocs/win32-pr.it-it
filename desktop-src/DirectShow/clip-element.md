---
description: Il clip epecifica un'origine multimediale.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Elemento clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d937f942ba7b564e65b0e37d9c11929805287da
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908669"
---
# <a name="clip-element"></a>Elemento clip

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`clip`L'oggetto epecifica un'origine multimediale.

## <a name="attributes"></a>Attributi

[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), start , [**stop**](start-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md) [](stop-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Label | Valore |
|----------|----------------------------------|
| Padre   | [**Traccia**](track-element.md)   |
| Children | [**Effetto**](effect-element.md) |



 

## <a name="remarks"></a>Commenti

**L'attributo clsid** specifica il CLSID di un filtro di origine da usare come origine. Non specificare gli attributi **src** e **clsid** all'interno dello stesso `clip` elemento.

Specificare almeno un attributo dell'ora di inizio (**start** o **mstart**) e un attributo stop-time (**stop** o **mstop**). Se uno degli attributi dell'ora di inizio non è specificato, il valore predefinito è 0 (l'inizio della sequenza temporale per **start** o l'inizio del clip per **mstart**). Se uno degli attributi del tempo di arresto non è specificato, DES presuppone una velocità di riproduzione normale e calcola di conseguenza il tempo di arresto non specificato. Se vengono specificati entrambi i tempi di arresto, la riproduzione è più veloce o più lenta del normale, se necessario.

Nell'esempio seguente la durata della sequenza temporale è di sette secondi (**stop** meno **start**). Si presuppone la frequenza di riproduzione normale, quindi il tempo di arresto multimediale è 10 secondi (durata più **mstart**).


```
<clip start="2" stop="9" mstart="3" />
```



Nell'esempio successivo l'ora di inizio del supporto è impostata su 0, forzando la durata del supporto a 10 secondi. La durata della sequenza temporale è di cinque secondi, quindi il clip viene riprodotto al doppio della frequenza normale.


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

 

 



