---
description: Il qualificatore dinamico indica una classe le cui istanze vengono create dinamicamente. Il valore di questo qualificatore deve essere impostato su TRUE.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Qualificatore dinamico
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880666"
---
# <a name="dynamic-qualifier"></a>Qualificatore dinamico

Il qualificatore **dinamico** indica una classe le cui istanze vengono create dinamicamente. Il valore di questo qualificatore deve essere impostato su **true**.

Il qualificatore **dinamico** deve essere specificato in tutte le classi che contengono dati e per le quali le istanze vengono create dinamicamente. Il qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) viene in genere specificato anche per identificare il provider responsabile per fornire i dati.

Le classi che contengono solo metodi che necessitano di implementazione non richiedono il qualificatore **dinamico** . Per specificare il nome del provider per fornire l'implementazione è necessario solo il qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .

Tutte le classi derivate da una classe dinamica devono essere dinamiche. Non è possibile derivare una classe statica da una classe dinamica.

Quando si specifica **Dynamic** in una proprietà di un'istanza, è necessario specificare anche il qualificatore **PropertyContext** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualificatori WMI standard**](standard-wmi-qualifiers.md)
</dt> <dt>

[Qualificatori WMI](wmi-qualifiers.md)
</dt> <dt>

[Aggiunta di un qualificatore](adding-a-qualifier.md)
</dt> </dl>

 

 




