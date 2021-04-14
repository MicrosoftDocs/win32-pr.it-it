---
title: Archiviazione avanzata è ora facoltativa per WINPE e SKU del server
description: Archiviazione avanzata è ora facoltativa per WINPE e SKU del server
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104339423"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>Archiviazione avanzata è ora facoltativa per WINPE e SKU del server

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Archiviazione avanzata è sempre disponibile nei dispositivi Windows 7 USB. Con il rilascio di Windows 8, è disponibile per tutti i dispositivi di archiviazione. Nei dispositivi basati su client, è abilitata per impostazione predefinita; nei dispositivi server è facoltativo e deve essere sottoposta a provisioning tramite Ambiente preinstallazione di Windows (WinPE).

## <a name="manifestation"></a>Manifestazione

Il dispositivo server avrà esito negativo se non è abilitata l'archiviazione avanzata.

È necessario eseguire il provisioning dei dispositivi di avvio tramite WinPE con questa funzionalità abilitata.

## <a name="solution"></a>Soluzione

Poiché l'archiviazione avanzata è facoltativa per il server di runtime, gli sviluppatori devono aggiungerla a WinPE per il provisioning e l'attivazione di tali unità. Per informazioni dettagliate, vedere la guida alla distribuzione.

Gli amministratori del server devono quindi configurare in modo esplicito il server per l'utilizzo dell'archiviazione avanzata.

 

 




