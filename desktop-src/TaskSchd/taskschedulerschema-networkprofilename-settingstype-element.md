---
title: Elemento NetworkProfileName (settingsType)
description: Contiene il nome di un profilo di rete. Il Utilità di pianificazione verifica la disponibilità di questa rete quando l'elemento RunOnlyIfNetworkAvailable è impostato su True. Il nome viene usato a scopo di visualizzazione.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Elemento NetworkProfileName Utilità di pianificazione
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 464c8b8f23dfeed6ea7c3412c3eeec07f20e5a8a7fcea662b4a16dfac7cb3fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758491"
---
# <a name="networkprofilename-settingstype-element"></a>Elemento NetworkProfileName (settingsType)

Contiene il nome di un profilo di rete. Il Utilità di pianificazione verifica la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **True.** Il nome viene usato a scopo di visualizzazione.

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

**L'elemento NetworkProfileName** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                      | Derivato da                                                         | Descrizione                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Impostazioni (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





