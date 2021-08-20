---
description: L'oggetto ConfigurableItem rappresenta una singola riga della tabella ModuleConfiguration.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Oggetto ConfigurableItem (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: fa0ade829cff2359e074a4c2faf9942e94aa5e063f0cce841a5a0f0a84a5f3e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143730"
---
# <a name="configurableitem-object"></a>Oggetto ConfigurableItem

**L'oggetto ConfigurableItem** rappresenta una singola riga della [tabella ModuleConfiguration](moduleconfiguration-table.md). Si tratta di un singolo "attributo" configurabile del modulo. L'interfaccia è costituita da proprietà di sola lettura, una per ogni colonna nella tabella ModuleConfiguration. La definizione dell'interfaccia è la seguente.

## <a name="members"></a>Membri

**L'oggetto ConfigurableItem** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto ConfigurableItem** ha queste proprietà.



| Proprietà                                                         | Descrizione                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attributi**](configurableitem-attributes.md)<br/>     | Restituisce il valore nel campo Attributi del record di questo oggetto nella tabella ModuleConfiguration.<br/>                            |
| [**Context**](configurableitem-context.md)<br/>           | Restituisce il valore nel campo Context del record di questo oggetto nella tabella ModuleConfiguration.<br/>                               |
| [**DefaultValue**](configurableitem-defaultvalue.md)<br/> | Restituisce il valore nel campo DefaultValue del record di questo oggetto nella tabella ModuleConfiguration.<br/>                          |
| [**Descrizione**](configurableitem-description.md)<br/>   | Restituisce il valore nel campo Description del record di questo oggetto nella tabella ModuleConfiguration.<br/>                           |
| [**Displayname**](configurableitem-displayname.md)<br/>   | Restituisce il valore nel campo DisplayName del record di questo oggetto nella tabella ModuleConfiguration.<br/>                           |
| [**Formato**](configurableitem-format.md)<br/>             | Restituisce il valore nel campo Formato del record di questo oggetto nella tabella ModuleConfiguration.<br/>                                |
| [**Helpkeyword**](configurableitem-helpkeyword.md)<br/>   | Restituisce il valore nel campo HelpKeyword del record di questo oggetto nella tabella ModuleConfiguration.<br/>                           |
| [**HelpLocation**](configurableitem-helplocation.md)<br/> | Restituisce il valore nel campo HelpLocation del record di questo oggetto nella tabella ModuleConfiguration.<br/>                          |
| [**Nome**](configurableitem-name.md)<br/>                 | Restituisce il valore nel campo Nome del record di questo oggetto nella [tabella ModuleConfiguration](moduleconfiguration-table.md).<br/> |
| [**Tipo**](configurableitem-type.md)<br/>                 | Restituisce il valore nel campo Type del record di questo oggetto nella tabella ModuleConfiguration.<br/>                                  |



 

## <a name="c"></a>C++

interfaccia **IMsmConfigurableItem : IDispatch**

## <a name="interface-id"></a>ID interfaccia



| Costante                      | Valore                                  |
|-------------------------------|----------------------------------------|
| **IID \_ IMsmConfigurableItem** | {4D6E6284-D21D-401E-84F6-909E00B50F71} |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




