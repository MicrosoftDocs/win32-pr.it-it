---
title: BUTTON.image
description: L'attributo image specifica o recupera l'immagine predefinita di BUTTON.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- Proprietà BUTTON.image Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85874c79db8f3174b70af68c3ff1e58511c3f00cc7d648389dbca971c7efd96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342909"
---
# <a name="buttonimage"></a>BUTTON.image

**L'attributo** image specifica o recupera l'immagine predefinita di **BUTTON.**

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura contenente** il nome del file di immagine.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF (incluse le GIF animate).

Se **l'immagine BUTTON** è più grande dell'area definita dagli attributi **width** **e height,** l'immagine verrà ritagliata.

Se l'immagine non è specificata, ma **l'altezza** e la **larghezza** lo sono, viene visualizzata l'immagine direttamente dietro questo controllo. Ciò può semplificare il disegno dell'immagine nella **visualizzazione** stessa, riducendo il numero di file di immagine separati necessari.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita (l'immagine rossa-x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 





