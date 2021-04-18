---
description: L'API di distribuzione peer definisce i tipi di dati seguenti.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Tipi di dati dell'API di distribuzione peer (Peerdist. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312253"
---
# <a name="peer-distribution-api-data-types"></a>Tipi di dati dell'API di distribuzione peer

L'API di distribuzione peer definisce i tipi di dati seguenti.


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| Tipo di dati                                                                                                                     | Descrizione                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**\_handle dell'istanza di PEERDIST \_**          | Handle associato all'istanza di distribuzione peer. Questo handle viene creato da [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)e usato nella maggior parte delle operazioni di distribuzione peer.<br/>                                          |
| <span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_handle di contenuto PEERDIST \_**             | Handle associato al contenuto. Questo handle viene creato da [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) e a cui viene fatto riferimento durante l'apertura, la chiusura, l'aggiunta o la pubblicazione di contenuto.<br/>                     |
| <span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**\_handle CONTENTINFO \_ PEERDIST** | Handle associato alle informazioni sul contenuto. Questo handle viene creato da [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)e viene usato durante il recupero delle informazioni sul contenuto codificato.<br/> |
| <span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**\_handle del flusso PEERDIST \_**                | Handle associato a un flusso di dati. Questo handle viene creato da [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) ed è usato come riferimento durante la pubblicazione, la chiusura o l'aggiunta di contenuto trasmesso.<br/>        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 7 Professional\]<br/>                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Peerdist. h</dt> </dl> |



 

 




