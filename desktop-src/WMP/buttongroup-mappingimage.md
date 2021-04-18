---
title: BUTTONGROUP. mappingImage
description: L'attributo mappingImage specifica o Recupera il nome dell'immagine che rappresenta la mappa dei pulsanti di BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- Media Player Windows BUTTONGROUP. mappingImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330257"
---
# <a name="buttongroupmappingimage"></a>BUTTONGROUP. mappingImage

L'attributo **mappingImage** specifica o Recupera il nome dell'immagine che rappresenta la mappa dei pulsanti di **ButtonGroup**.

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Si tratta di un attributo obbligatorio che è necessario specificare.

L'immagine di mapping deve avere le stesse dimensioni dell' **immagine** principale. Si tratta di una mappa delle aree selezionabili dell'immagine principale. Costruire la mappa riempiendo ogni area selezionabile con un colore diverso.

Quando si definiscono i **pulsantielement**, designare il colore dalla mappa utilizzando l'attributo **mappingColor** . Se, ad esempio, nell'immagine principale è presente una rappresentazione grafica di un pulsante con segno di arresto, è possibile creare una mappa con l'area del segno rosso colorato. L'attributo **ButtonElement** deve quindi essere specificato come rosso per fare clic sull'immagine di stop-sign.

I formati di immagine supportati sono BMP, JPG, PNG e GIF (escluse le gif animate). Poiché i jpg sono con perdita di perdite e pertanto sono soggetti a variazioni di colore impreviste, non sono consigliate per il mapping delle immagini.

## <a name="examples"></a>Esempio

L'illustrazione seguente è un esempio di **mappingImage** e dell'immagine visibile a cui corrisponde. Queste immagini fanno parte dell'interfaccia della piccola cartella inclusa nell'SDK.

![immagine di mapping di esempio](images/absam01m.png)![immagine di sfondo di esempio](images/absam01f.png)

Vedere *ButtonElement*. attributo [mappingColor](buttonelement-mappingcolor.md) per un esempio di codice che illustra l'uso di questo attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BUTTONelement. mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. transparencyColor**](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





