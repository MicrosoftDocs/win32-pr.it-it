---
title: BUTTON. image
description: L'attributo Image specifica o recupera l'immagine predefinita del pulsante.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- BUTTON. Image Media Player Windows
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331765"
---
# <a name="buttonimage"></a>BUTTON. image

L'attributo **Image** specifica o recupera l'immagine predefinita del **pulsante**.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome del file di immagine.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF (incluse le gif animate).

Se l'immagine del **pulsante** è più grande dell'area definita dagli attributi **Width** e **Height** , l'immagine verrà ritagliata.

Se l'immagine non è specificata, ma l' **altezza** e la **larghezza** sono, viene visualizzata l'immagine direttamente dietro il controllo. Ciò consente di semplificare il disegno dell'immagine nella **visualizzazione** stessa, riducendo il numero di file di immagine separati necessari.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 





