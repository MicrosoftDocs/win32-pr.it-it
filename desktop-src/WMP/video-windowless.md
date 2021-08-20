---
title: VIDEO.windowless
description: L'attributo senza finestra specifica o recupera un valore che indica se il controllo Video sarà in finestra o senza finestra; ad esempio se l'intero rettangolo del controllo sarà sempre visibile o ritagliato.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VIDEO.windowless Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98aefde5aab9837f220ccb7df254e6a592e0d5e9d41de43291b2ab73e287321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931741"
---
# <a name="videowindowless"></a>VIDEO.windowless

**L'attributo** senza finestra specifica o recupera un valore che indica se il controllo Video sarà in finestra o senza finestra; ad esempio se l'intero rettangolo del controllo sarà sempre visibile o ritagliato. Può essere impostato solo in fase di progettazione.

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** specificato in fase di progettazione e di sola lettura successivamente.



| Valore | Descrizione                              |
|-------|------------------------------------------|
| true  | Il controllo video sarà senza finestra.        |
| false | Valore predefinito. Il controllo video verrà visualizzato in una finestra. |



 

## <a name="remarks"></a>Commenti

Se si desidera una finestra video non rettangolare o se si vuole coprire qualsiasi parte della finestra video con un'immagine, questo attributo deve essere impostato su true. Ciò consente di migliorare alcune prestazioni per eseguire il ritaglio necessario.

La riproduzione video è ottimizzata per la riproduzione non ritagliata. In questo caso, **l'attributo senza** finestra è impostato su false e l'intero rettangolo video viene sempre visualizzato. Qualsiasi immagine che copre la finestra video viene ignorata e la finestra video ha l'ordine z di livello più alto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> </dl>

 

 





