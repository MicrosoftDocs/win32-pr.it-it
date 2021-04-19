---
description: Archivia e recupera le informazioni sulle sottoscrizioni di eventi. Questa interfaccia estende l'interfaccia IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Interfaccia IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305219"
---
# <a name="ieventsubscription3-interface"></a>Interfaccia IEventSubscription3

Archivia e recupera le informazioni sulle sottoscrizioni di eventi. Questa interfaccia estende l'interfaccia [**IEventSubscription2**](ieventsubscription2.md) .

## <a name="when-to-implement"></a>Quando implementare

Non è necessario implementare l'interfaccia **IEventSubscription3** . Una classe di oggetti evento fornita dal sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription3**.

## <a name="when-to-use"></a>Utilizzo

Il sistema [degli eventi com+](com--events.md) utilizza questa interfaccia per ottenere informazioni sulle singole sottoscrizioni.

## <a name="members"></a>Membri

L'interfaccia **IEventSubscription3** eredita da **IEventSubscription2**. **IEventSubscription3** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IEventSubscription3** ha queste proprietà.



| Proprietà                                                                                  | Tipo di accesso           | Descrizione                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**EventClassApplicationID**](ieventsubscription3-eventclassapplicationid.md)<br/> | Lettura/Scrittura<br/> | GUID dell'applicazione dell'oggetto della classe di evento.<br/> |
| [**EventClassPartitionID**](ieventsubscription3-eventclasspartitionid.md)<br/>     | Lettura/Scrittura<br/> | GUID della partizione dell'oggetto della classe di evento.<br/>   |
| [**SubscriberApplicationID**](ieventsubscription3-subscriberapplicationid.md)<br/> | Lettura/Scrittura<br/> | GUID dell'applicazione del Sottoscrittore.<br/>         |
| [**SubscriberPartitionID**](ieventsubscription3-subscriberpartitionid.md)<br/>     | Lettura/Scrittura<br/> | GUID della partizione del Sottoscrittore.<br/>           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




