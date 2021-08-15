---
description: La proprietà ConfigurableItems di sola lettura dell'oggetto Merge restituisce una raccolta di oggetti ConfigurableItem, ognuno dei quali rappresenta una singola riga della tabella ModuleConfiguration.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.ConfigurableItems (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 179594ba7fe7691edb9abe1f72d104742fe9bc9e3a4a23b728ad8607b94c444a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013039"
---
# <a name="mergeconfigurableitems-property"></a>Merge.ConfigurableItems

La proprietà **ConfigurableItems** di sola lettura dell'oggetto [**Merge**](merge-object.md) restituisce una raccolta di oggetti [**ConfigurableItem,**](configurableitem-object.md) ognuno dei quali rappresenta una singola riga della [tabella ModuleConfiguration](moduleconfiguration-table.md). Dal punto di vista semantico, ogni interfaccia nell'enumeratore rappresenta un elemento che può essere configurato dal consumer del modulo. La raccolta è una raccolta di sola lettura e implementa le interfacce di raccolta di sola lettura standard di Item(), Count() e \_ NewEnum(). **L'enumeratore IEnumMsmConfigItems** implementa Next(), Skip(), Reset() e Clone() con la semantica standard.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a>Valore proprietà

## <a name="c"></a>C++

Vedere [**la funzione get \_ ConfigurableItems.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




