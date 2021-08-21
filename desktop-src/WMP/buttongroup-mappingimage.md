---
title: BUTTONGROUP.mappingImage
description: L'attributo mappingImage specifica o recupera il nome dell'immagine che rappresenta la mappa dei pulsanti di BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- ButtonGROUP.mappingImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c26a920042aae4ba144f194845f350030f5675c1b9cc3fcfed552346904add1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119902"
---
# <a name="buttongroupmappingimage"></a>BUTTONGROUP.mappingImage

**L'attributo mappingImage** specifica o recupera il nome dell'immagine che rappresenta la mappa dei pulsanti di **BUTTONGROUP.**

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Si tratta di un attributo obbligatorio che deve essere specificato.

L'immagine di mapping deve avere le stesse dimensioni dell'immagine **principale**. Si tratta di una mappa delle aree selezionabili dell'immagine principale. Costruire la mappa riempiendo ogni area selezionabile con un colore diverso.

Quando si definisce ogni **BUTTONELEMENT,** designarne il colore dalla mappa usando **l'attributo mappingColor.** Ad esempio, se nell'immagine principale è presente un pulsante a forma di stop-sign, è possibile creare una mappa con l'area del segno di colore rosso. **L'attributo BUTTONELEMENT** deve quindi essere specificato in rosso per rendere selezionabile l'immagine del segno di arresto.

I formati di immagine supportati sono BMP, JPG, PNG e GIF (senza GIF animate). Poiché i file JPG sono soggetti a perdita di dati e pertanto soggetti a modifiche di colore impreviste, non sono consigliati per il mapping delle immagini.

## <a name="examples"></a>Esempio

La figura seguente è un esempio di **mappingImage** e dell'immagine visibile a cui corrisponde. Queste immagini fanno parte dell'interfaccia nella cartella Tiny inclusa nell'SDK.

![immagine di mapping di esempio](images/absam01m.png)![immagine di sfondo di esempio](images/absam01f.png)

Vedere *BUTTONELEMENT.* [Attributo mappingColor](buttonelement-mappingcolor.md) per un esempio di codice che illustra l'uso di questo attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.transparencyColor**](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





