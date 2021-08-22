---
title: VIDEO.fullScreen
description: L'attributo fullScreen specifica o recupera un valore che indica se il video viene visualizzato in modalità schermo intero.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- Video.fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8150843ab14148d398b11cba82aa52711621c15962976ca37d5332a6ae58f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465693"
---
# <a name="videofullscreen"></a>VIDEO.fullScreen

**L'attributo fullScreen** specifica o recupera un valore che indica se il video viene visualizzato in modalità schermo intero.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                                          |
|-------|------------------------------------------------------|
| true  | Il video viene visualizzato in modalità schermo intero.                  |
| false | Valore predefinito. Il video non viene visualizzato in modalità schermo intero. |



 

## <a name="remarks"></a>Commenti

Questa proprietà può essere specificata solo in fase di esecuzione, dopo il caricamento di un file. Deve quindi essere impostato all'interno di un gestore eventi di script. Il pulsante di escape viene usato per tornare alla visualizzazione normale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> <dt>

[**VIDEO.maintainAspectRatio**](video-maintainaspectratio.md)
</dt> <dt>

[**VIDEO.shrinkToFit**](video-shrinktofit.md)
</dt> <dt>

[**VIDEO.stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 





