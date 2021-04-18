---
title: AmbientAttributes.clippingImage
description: L'attributo clippingImage specifica o recupera l'area in cui ritagliare il controllo.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- Media Player Windows AmbientAttributes. clippingImage
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331407"
---
# <a name="ambientattributesclippingimage"></a>AmbientAttributes.clippingImage

L'attributo **clippingImage** specifica o recupera l'area in cui ritagliare il controllo.

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura che indica il nome del file di immagine. e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

L'attributo **clippingImage** supporta file PNG, jpg, BMP e gif (escluse le gif animate). Poiché i jpg sono con perdita di perdite e pertanto sono soggetti a variazioni di colore impreviste, non sono consigliate per le immagini di ritaglio.

Questo attributo è utile quando si desidera visualizzare solo una parte dell'immagine del controllo e non l'intera area rettangolare. L'attributo **clippingColor** indica le aree dell'immagine di ritaglio che corrispondono a parti trasparenti e non selezionabili del controllo. Il controllo può quindi essere di qualsiasi forma. Per ottenere risultati ottimali, l'immagine di ritaglio deve avere le stesse dimensioni dell'immagine del controllo.

L'attributo **clippingImage** non è supportato dagli elementi **playlist**, **View** e **subview** . Un'immagine di ritaglio non funzionerà con l'elemento **video** se *video*. senza **finestra** è impostato su false, né con l'elemento **Effects** se *Effects*. **windowed** è impostato su true.

Poiché l'uso di immagini di ritaglio impone una riduzione delle prestazioni, non è consigliabile usarle quando l'efficienza è un problema.

## <a name="examples"></a>Esempio

Per un esempio che illustra l'uso di questo attributo, vedere l'attributo [ButtonElement. mappingColor](buttonelement-mappingcolor.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingColor**](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





