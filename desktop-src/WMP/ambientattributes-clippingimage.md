---
title: AmbientAttributes.clippingImage
description: L'attributo clippingImage specifica o recupera l'area in cui ritagliare il controllo.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- AmbientAttributes.clippingImage Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15302483143b17075b6a6164fcd05da80eb1c7c666a83c76a460408d70ac72e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055189"
---
# <a name="ambientattributesclippingimage"></a>AmbientAttributes.clippingImage

**L'attributo clippingImage** specifica o recupera l'area in cui ritagliare il controllo.

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** che indica il nome del file di immagine. e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

**L'attributo clippingImage** supporta i file PNG, JPG, BMP e GIF (senza includere le GIF animate). Poiché i file JPG sono persi e pertanto soggetti a modifiche di colore impreviste, non sono consigliati per il ritaglio delle immagini.

Questo attributo è utile quando si vuole visualizzare solo una parte dell'immagine del controllo e non l'intera area rettangolare. **L'attributo clippingColor** indica le aree dell'immagine di ritaglio che corrispondono a parti trasparenti e non selezionabili del controllo. Il controllo può pertanto essere di qualsiasi forma. Per ottenere risultati ottimali, l'immagine di ritaglio deve avere le stesse dimensioni dell'immagine del controllo.

**L'attributo clippingImage** non è supportato dagli elementi **PLAYLIST,** **VIEW** e **SUBVIEW.** Un'immagine di ritaglio non funzionerà con **l'elemento VIDEO** se *VIDEO*. **windowless è** impostato su false, né con l'elemento **EFFECTS** se *EFFECTS*. **windowed** è impostato su true.

Poiché l'uso di immagini di ritaglio impone una penalità per le prestazioni, non deve essere usato quando l'efficienza è un problema.

## <a name="examples"></a>Esempio

Vedere [l'attributo BUTTONELEMENT.mappingColor](buttonelement-mappingcolor.md) per un esempio che illustra l'uso di questo attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingColor**](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





