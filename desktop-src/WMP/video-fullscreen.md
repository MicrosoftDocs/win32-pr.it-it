---
title: VIDEO. fullScreen
description: L'attributo fullScreen Specifica o recupera un valore che indica se il video viene visualizzato in modalità schermo intero.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VIDEO. Windows fullScreen Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330104"
---
# <a name="videofullscreen"></a>VIDEO. fullScreen

L'attributo **FullScreen** specifica o recupera un valore che indica se il video viene visualizzato in modalità schermo intero.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                          |
|-------|------------------------------------------------------|
| true  | Il video viene visualizzato in modalità schermo intero.                  |
| false | Valore predefinito. Il video non viene visualizzato in modalità schermo intero. |



 

## <a name="remarks"></a>Commenti

Questa proprietà può essere specificata solo in fase di esecuzione, dopo il caricamento di un file. Deve pertanto essere impostato in un gestore eventi di script. Il pulsante escape viene usato per tornare alla visualizzazione normale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> <dt>

[**VIDEO. maintainAspectRatio**](video-maintainaspectratio.md)
</dt> <dt>

[**VIDEO. shrinkToFit**](video-shrinktofit.md)
</dt> <dt>

[**VIDEO. stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 





