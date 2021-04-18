---
description: La proprietà ConfigurableItems di sola lettura dell'oggetto merge restituisce una raccolta di oggetti ConfigurableItem, ognuno dei quali rappresenta una singola riga della tabella ModuleConfiguration.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Proprietà Merge.ConfigurableItems (Mergemod. h)
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
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327323"
---
# <a name="mergeconfigurableitems-property"></a>Merge.Configproprietà urableItems

La proprietà **ConfigurableItems** di sola lettura dell'oggetto [**merge**](merge-object.md) restituisce una raccolta di oggetti [**ConfigurableItem**](configurableitem-object.md) , ognuno dei quali rappresenta una singola riga della [tabella ModuleConfiguration](moduleconfiguration-table.md). Semanticamente, ogni interfaccia nell'enumeratore rappresenta un elemento che può essere configurato dall'utente del modulo. La raccolta è una raccolta di sola lettura e implementa le interfacce di raccolta di sola lettura standard di Item (), Count () e \_ NewEnum (). L'enumeratore **IEnumMsmConfigItems** implementa Next (), Skip (), Reset () e Clone () con la semantica standard.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a>Valore proprietà

## <a name="c"></a>C++

Vedere [**ottenere \_**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) la funzione ConfigurableItems.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




