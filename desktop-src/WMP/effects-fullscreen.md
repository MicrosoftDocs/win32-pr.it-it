---
title: EFFECTs. fullScreen
description: L'attributo fullScreen Specifica o recupera un valore che indica se la visualizzazione corrente è visualizzata a schermo intero. Questo attributo può essere impostato solo in fase di esecuzione.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- EFFETTI. Windows fullScreen Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332558"
---
# <a name="effectsfullscreen"></a>EFFECTs. fullScreen

L'attributo **FullScreen** specifica o recupera un valore che indica se la visualizzazione corrente è visualizzata a schermo intero. Questo attributo può essere impostato solo in fase di esecuzione.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                          |
|-------|------------------------------------------------------|
| true  | La visualizzazione viene visualizzata a schermo intero.              |
| false | Valore predefinito. La visualizzazione non viene visualizzata a schermo intero. |



 

## <a name="remarks"></a>Commenti

Una visualizzazione può essere inserita in modalità schermo intero solo quando il supporto viene riprodotto o sospeso. Se il *lettore*. **currentMedia** è un video, deve essere presente un plug-in video. Se è audio, deve essere presente un plug-in di visualizzazione che supporta la visualizzazione a schermo intero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EFFECTs-elemento**](effects-element.md)
</dt> </dl>

 

 





