---
title: L'archiviazione avanzata è ora facoltativa per WINPE e lo SKU del server
description: L'archiviazione avanzata è ora facoltativa per WINPE e lo SKU del server
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3777d4df386b071166fcfa17a60654c62e039d9137f73deaf2d85d54e2519e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028849"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>L'archiviazione avanzata è ora facoltativa per WINPE e lo SKU del server

## <a name="platforms"></a>Piattaforme

**Client** : Windows 8  
**Server** - Windows Server 2012  


## <a name="description"></a>Descrizione

L'archiviazione avanzata era sempre disponibile in Windows 7 dispositivi USB. Con il rilascio di Windows 8, è disponibile per tutti i dispositivi di archiviazione. Nei dispositivi basati su client è abilitato per impostazione predefinita. nei dispositivi server è facoltativo e deve essere effettuato il provisioning tramite Windows Preinstallation Environment (WinPE).

## <a name="manifestation"></a>Manifestazione

Il dispositivo server avrà esito negativo se l'archiviazione avanzata non è abilitata.

È necessario effettuare il provisioning dei dispositivi di avvio tramite WinPE con questa opzione abilitata.

## <a name="solution"></a>Soluzione

Poiché l'archiviazione avanzata è facoltativa per il server di runtime, gli sviluppatori devono aggiungerla a WinPE per il provisioning e l'attivazione di tali unità. Per informazioni dettagliate, vedere la guida alla distribuzione.

Gli amministratori del server devono quindi configurare in modo esplicito il server per l'uso dell'archiviazione avanzata.

 

 




