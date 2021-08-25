---
description: Memoria dinamica
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Memoria dinamica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 408e54aa1a1d238a98bb0eff8af2dd76862b32b77c26b3d3812d8707bc0099f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329853"
---
# <a name="dynamic-memory"></a>Memoria dinamica

## <a name="affected-platforms"></a>Piattaforme interessate

**Client (in esecuzione come macchine virtuali)** - Windows Vista \| Windows 7  
**Server** - Windows Server 2008 R2 Hyper-V SP1  


## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Alta  






## <a name="description"></a>Descrizione

A livello di alto livello, Hyper-V memoria dinamica è un miglioramento della gestione della memoria per il ruolo Hyper-V incluso in Windows Server 2008 R2 SP1. È progettato per l'uso in produzione e consente ai clienti di ottenere rapporti di densità più elevati di consolidamento/macchina virtuale (VM) ottimizzando al tempo stesso l'utilizzo della memoria nel computer fisico. L'allocazione di memoria statica viene ridotta e la memoria aggiuntiva viene allocata in base alle esigenze. memoria dinamica influisce sugli sviluppatori di software che vogliono garantire il corretto funzionamento del software in un ambiente di macchine virtuali.

## <a name="usage-scenario"></a>Scenario di utilizzo

Esistono due scenari di utilizzo chiave in cui memoria dinamica in gioco, applicazioni lato host e applicazioni lato guest.

**Applicazioni lato host (strumenti di gestione)**

Gli strumenti meno avanzati che gestiscono un nuovo server Windows Server 2008 R2 SP1 non saranno in grado di accedere alle nuove impostazioni memoria dinamica predefinite. Sono state sviluppate nuove API WMI e contatori delle prestazioni per gestire le nuove impostazioni memoria dinamica per le macchine virtuali Hyper-V. Gli sviluppatori software che lavorano sugli strumenti di gestione devono sfruttare queste API e contatori per l'uso con Windows Server 2008 R2 SP1 con il ruolo Hyper-V installato. I dettagli su queste nuove API saranno disponibili tramite la documentazione del [provider WMI Hyper-V in MSDN.](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

**Applicazioni lato guest**

Gli sviluppatori che scrivono software da usare all'interno di una macchina virtuale configurata per l memoria dinamica devono tenere presente che la memoria di sistema della macchina virtuale non è più costante. Di conseguenza, l'applicazione deve liberare memoria quando non è più necessaria per consentire ad altre applicazioni di sfruttare la risorsa.

Le allocazioni di memoria e le deallocazione continuano a funzionare normalmente per le applicazioni utente. memoria dinamica è completamente trasparente per la maggior parte delle applicazioni degli utenti finali. Tuttavia, se il software in fase di sviluppo usa contatori delle prestazioni di memoria nella macchina virtuale, è necessario eseguire test accurati in un ambiente abilitato per memoria dinamica per assicurarsi che il software prende in considerazione le modifiche apportate all'allocazione di memoria del sistema operativo guest. La memoria disponibile non è più "statica" dal punto di vista della macchina virtuale.

## <a name="solutions"></a>Soluzioni

Le macchine virtuali devono avere installato Integration Services (SP1) aggiornato per poter sfruttare memoria dinamica. Assicurarsi che tutti i computer usati nella gestione delle macchine virtuali Hyper-V utilizzino i bit più recenti Windows Server 2008 R2 SP1.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [memoria dinamica blog di Hyper-V](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [Uso del provider WMI Hyper-V](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>Dichiarazione di non responsabilità

Le informazioni contenute in questo documento riguardano prodotti software non definitive che possono essere modificati in modo sostanziale prima della prima versione commerciale. Di conseguenza, le informazioni potrebbero non descrivere o riflettere in modo accurato il prodotto software al primo rilascio commerciale. Questo documento è esclusivamente a scopo informativo. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
