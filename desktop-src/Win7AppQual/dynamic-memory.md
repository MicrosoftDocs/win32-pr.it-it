---
description: .
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Memoria dinamica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1e868a89714a7f6f1d77f9416515897876c150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318577"
---
# <a name="dynamic-memory"></a>Memoria dinamica

## <a name="affected-platforms"></a>Piattaforme interessate

**Client (in esecuzione come macchine virtuali)** -Windows Vista \| Windows 7  
**Server** -Windows Server 2008 R2 Hyper-V SP1  


## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -alta  






## <a name="description"></a>Descrizione

A un livello elevato, Hyper-V memoria dinamica è un miglioramento della gestione della memoria per il ruolo Hyper-V incluso in Windows Server 2008 R2 SP1. È progettato per l'uso in ambiente di produzione e consente ai clienti di ottenere rapporti di densità di consolidamento/macchina virtuale (VM) più elevati, ottimizzando al tempo stesso l'utilizzo della memoria nel computer fisico. L'allocazione di memoria statica viene ridotta e la memoria aggiuntiva viene allocata in base alle esigenze. Memoria dinamica influisca sugli sviluppatori di software che desiderano garantire il corretto funzionamento del software in un ambiente di macchina virtuale.

## <a name="usage-scenario"></a>Scenario di utilizzo

Esistono due scenari di utilizzo chiave in cui memoria dinamica entra in gioco, applicazioni lato host e applicazioni lato Guest.

**Applicazioni lato host (strumenti di gestione)**

Gli strumenti obsoleti che gestiscono un nuovo server Windows Server 2008 R2 SP1 non saranno in grado di accedere alle nuove impostazioni di memoria dinamica. Sono state sviluppate nuove API WMI e contatori delle prestazioni per gestire le nuove impostazioni memoria dinamica per le macchine virtuali Hyper-V. Gli sviluppatori di software che lavorano sugli strumenti di gestione dovrebbero sfruttare i vantaggi di queste API e contatori per l'uso con Windows Server 2008 R2 SP1 con il ruolo Hyper-V installato. Per informazioni dettagliate su queste nuove API, fare riferimento [alla documentazione del provider WMI Hyper-V su MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).

**Applicazioni lato Guest**

Gli sviluppatori che scrivono software da usare all'interno di una macchina virtuale configurata per usare memoria dinamica necessario tenere presente che la memoria del sistema VM non è più costante. Di conseguenza, l'applicazione deve liberare memoria quando non è più necessaria per consentire ad altre applicazioni di sfruttare la risorsa.

Le allocazioni di memoria e le deallocazioni continuano a funzionare normalmente per le applicazioni utente. Memoria dinamica è completamente trasparente per la maggior parte delle applicazioni per gli utenti finali. Tuttavia, se il software in fase di sviluppo utilizza i contatori delle prestazioni della memoria nella macchina virtuale, è necessario eseguire un test accurato in un ambiente memoria dinamica abilitato per garantire che il software accetti le modifiche apportate all'allocazione di memoria del sistema operativo guest. La memoria disponibile non è più "statica" dal punto di vista della macchina virtuale.

## <a name="solutions"></a>Soluzioni

Per sfruttare i vantaggi offerti da memoria dinamica, nelle macchine virtuali deve essere installato Integration Services (SP1). Assicurarsi che tutti i computer utilizzati per la gestione delle macchine virtuali Hyper-V utilizzino i bit più recenti di Windows Server 2008 R2 SP1.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Blog di memoria dinamica in arrivo a Hyper-V](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [Uso del provider WMI Hyper-V](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>Dichiarazione di non responsabilità

Le informazioni contenute in questo documento si riferiscono al prodotto software provvisorio che può essere modificato in modo sostanziale prima della prima versione commerciale. Di conseguenza, è possibile che le informazioni non descrivano o riflettano in modo accurato il prodotto software alla prima pubblicazione in commercio. Questo documento è esclusivamente a scopo informativo. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
