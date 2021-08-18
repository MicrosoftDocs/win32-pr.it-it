---
description: Il profilo di virtualizzazione delle risorse consente a un client di individuare le risorse virtuali supportate dal sistema di virtualizzazione.
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: Servizio di gestione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593af3c440ad15add50445a3b05f41d44c8c396a1334635aeaf141838e82e64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746217"
---
# <a name="resource-management-service"></a>Servizio di gestione delle risorse

Il profilo di virtualizzazione delle risorse consente a un client di individuare le risorse virtuali supportate dal sistema di virtualizzazione. Descrive anche la capacità, o il numero di allocazioni, supportata per ogni tipo di risorsa virtuale. La figura seguente mostra il profilo di virtualizzazione delle risorse.

![profilo di virtualizzazione delle risorse](images/resourcemanagement.png)

Due diverse classi di risorse virtuali sono definite dal profilo di virtualizzazione delle risorse:

-   Risorsa condivisa: rappresenta le risorse dell'host che sono o possono essere condivise tra più macchine virtuali. [**Msvm \_ Processore**](msvm-processor.md) è un esempio di risorsa condivisa.
-   Risorsa sintetica: rappresenta le risorse virtuali che non hanno una risorsa host corrispondente. [**Msvm \_ EmulatedEthernetPort è**](msvm-emulatedethernetport.md) un esempio di risorsa sintetica.

Il pool di risorse viene usato per raccogliere una classe di risorse host in modo che sia facilmente individuabile, mentre le relative funzionalità e impostazioni possono essere descritte in una posizione centrale. Non esiste alcun limite al livello di base o avanzato di un'implementazione della risorsa raccolta.

Dal pool di risorse, il client può accedere alle funzionalità di allocazione associate. Questa classe descrive le funzionalità della risorsa descritta da questo pool di risorse. Ad esempio, può indicare se [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) rappresentato da questo pool di risorse supporta reti LAN virtuali (VLAN) o filtri.

Il profilo di controllo di accesso definisce i mezzi con cui un client può individuare l'intervallo valido di impostazioni predefinite e per una determinata risorsa virtuale. Un oggetto AC è associato a ogni pool di risorse. Quattro oggetti RASD (Resource Allocation Setting Data) sono associati all'oggetto AC per descrivere i valori minimo, massimo, predefinito e incrementale per l'allocazione della risorsa specificata. Insieme, queste classi descrivono la gamma complessiva di funzionalità supportate. [**L'istanza \_ AllocationCapabilities msvm**](msvm-allocationcapabilities.md) fornisce un punto di ancoraggio per il set di istanze [**di Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) che specificano l'intervallo predefinito e valido di impostazioni per una risorsa virtuale. La [**classe di associazione Msvm \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md) fornisce il collegamento tra l'istanza di Ca e le impostazioni minime, massime, incrementali e predefinite per una risorsa supportata dalla piattaforma di virtualizzazione.

 

 



