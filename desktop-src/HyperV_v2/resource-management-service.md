---
description: Il profilo di virtualizzazione delle risorse fornisce i mezzi con cui un client può individuare le risorse virtuali supportate dal sistema di virtualizzazione.
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: Servizio Gestione risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c405cac60df719195466da6ea0c7aadb7bf0d765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058149"
---
# <a name="resource-management-service"></a>Servizio Gestione risorse

Il profilo di virtualizzazione delle risorse fornisce i mezzi con cui un client può individuare le risorse virtuali supportate dal sistema di virtualizzazione. Descrive anche la capacità, o il numero di allocazioni, supportato per ogni tipo di risorsa virtuale. Nella figura seguente viene illustrato il profilo di virtualizzazione delle risorse.

![Profilo di virtualizzazione delle risorse](images/resourcemanagement.png)

Due classi diverse di risorse virtuali sono definite dal profilo di virtualizzazione delle risorse:

-   Risorsa condivisa: rappresenta le risorse dell'host che sono o possono essere condivise tra più macchine virtuali. [**MSVM \_ Il processore**](msvm-processor.md) è un esempio di risorsa condivisa.
-   Risorsa sintetica: rappresenta le risorse virtuali senza risorsa host corrispondente. [**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) è un esempio di risorsa sintetica.

Il pool di risorse viene usato per raccogliere una classe di risorse host in modo che possa essere individuata facilmente mentre le funzionalità e le impostazioni possono essere descritte in una posizione centrale. Non esiste alcun limite al modo in cui l'implementazione della risorsa raccolta può essere di base o avanzata.

Dal pool di risorse, il client può accedere alle funzionalità di allocazione associate (CA). Questa classe descrive le funzionalità della risorsa descritta da questo pool di risorse. Ad esempio, può indicare se il [**\_ EmulatedEthernetPort MSVM**](msvm-emulatedethernetport.md) rappresentato da questo pool di risorse supporta le LAN virtuali (VLAN) o i filtri.

Il profilo AC definisce i mezzi mediante i quali un client può individuare l'intervallo valido di e le impostazioni predefinite per una determinata risorsa virtuale. Un oggetto AC è associato a ogni pool di risorse. Quattro oggetti dati di impostazione di allocazione risorse (RASD) sono associati all'oggetto AC per descrivere i valori minimo, massimo, predefinito e incrementale per l'allocazione della risorsa specificata. Insieme, queste classi descrivono la gamma complessiva di funzionalità supportate. L'istanza di [**MSVM \_ AllocationCapabilities**](msvm-allocationcapabilities.md) fornisce un punto di ancoraggio per il set di istanze di [**\_ ResourceAllocationSettingData di MSVM**](msvm-resourceallocationsettingdata.md) che specificano l'intervallo di impostazioni predefinito e valido per una risorsa virtuale. La classe di associazione [**MSVM \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md) fornisce il collegamento tra l'istanza di AC e le impostazioni minime, massime, incrementali e predefinite per una risorsa supportata dalla piattaforma di virtualizzazione.

 

 



