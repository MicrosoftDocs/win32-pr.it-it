---
title: Elemento NetworkProfileName (settingsType)
description: Contiene il nome di un profilo di rete. Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento RunOnlyIfNetworkAvailable è impostato su true. Il nome viene usato a scopo di visualizzazione.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Utilità di pianificazione elemento NetworkProfileName
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742159"
---
# <a name="networkprofilename-settingstype-element"></a>Elemento NetworkProfileName (settingsType)

Contiene il nome di un profilo di rete. Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **true**. Il nome viene usato a scopo di visualizzazione.

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

L'elemento **NetworkProfileName** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                      | Derivato da                                                         | Descrizione                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Impostazioni (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





