---
title: Proprietà IPropertyFilter LogicOperator (WdsSharedIDL.h)
description: Operatore logico da usare quando si applica un filtro.
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- Proprietà LogicOperator Funzionalità dell'Windows legacy
- Proprietà LogicOperator Legacy Windows Environment Features , interfaccia IPropertyFilter
- Interfaccia IPropertyFilter Legacy Windows Environment Features , proprietà LogicOperator
topic_type:
- apiref
api_name:
- IPropertyFilter.LogicOperator
- IPropertyFilter.get_LogicOperator
- IPropertyFilter.put_LogicOperator
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fb4638edbb839581ad20ab6c860afc918b0ddd08e5fe6a36fc92f0dd4cea4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963831"
---
# <a name="ipropertyfilterlogicoperator-property"></a>Proprietà IPropertyFilter::LogicOperator

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Operatore logico da usare quando si applica un filtro.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_LogicOperator(
  [in]          FilterLogicOperator op
);

HRESULT get_LogicOperator(
  [out, retval] FilterLogicOperator *op
);
```



## <a name="property-value"></a>Valore proprietà

Imposta il tipo di operatore logico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





