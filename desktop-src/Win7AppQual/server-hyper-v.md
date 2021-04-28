---
description: Server Hyper-V
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: Server Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b3149f1c5faa98c9c61be884a193b0e3a1ecceb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116209"
---
# <a name="server-hyper-v"></a>Server Hyper-V

## <a name="platforms"></a>Piattaforme

 **Client** - Windows XP \| Windows Vista Windows \| 7  
**Server** - Windows Server 2008 \| Windows Server 2008 R2  

## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

La virtualizzazione server consente l'esecuzione di più sistemi operativi in una singola macchina fisica come macchine virtuali, consentendo di consolidare i carichi di lavoro di computer server sottoutilizzati in un numero inferiore di computer completamente utilizzati. Windows 7 include diversi miglioramenti alla versione di Windows Server 2008:

-   **Live Migration:** In Windows Server 2008 è stata completata la migrazione rapida. Con Live Migration, abbiamo migliorato la velocità di migrazione e la flessibilità di archiviazione.
-   **Supporto del processore logico:** Sono stati aumentati i processori host logici da 16LP a 64LP.
-   **Aggiunta di risorse di archiviazione a caldo:** È ora possibile aggiungere altri dischi VHD o Pass-through a una macchina virtuale in esecuzione senza disattivare la macchina virtuale.
-   **Nuovo supporto hardware:** È stato aggiunto il supporto per le tecnologie incluse nei nuovi processori e nelle schede di rete in arrivo sul mercato, tra cui SLAT (Second Level Translation), TCP Offload (Chimney) e VMdQ.
-   **Virtualizzazione di Servizi terminal (TSv):** È stata centralizzata la soluzione desktop per Hyper-V.

## <a name="manifestation-of-impact"></a>Manifestazione di impatto

-   **Live Migration:** Potrebbe essere necessario modificare il modo in cui sono stati progettati i sistemi di archiviazione per sfruttare completamente questa tecnologia. Anche se queste modifiche potrebbero non essere necessarie, è possibile scegliere di implementarle per sfruttare appieno i vantaggi. Potrebbe essere necessaria un'applicazione di gestione per orchestrare Live Migration.
-   **Supporto del processore logico:** Questa funzionalità non avrà alcun impatto sui clienti o sugli ISV durante la migrazione da Windows Server 2008 a Windows Server 2008 R2.
-   **Aggiunta di risorse di archiviazione a caldo:** Questa funzionalità non avrà alcun impatto per i clienti o gli ISV durante la migrazione da Windows Server 2008 a Windows Server 2008 R2. Le applicazioni di gestione che configurano le impostazioni di una macchina virtuale possono richiedere l'aggiornamento per gestire questa nuova funzionalità.
-   **Nuovo supporto hardware:** Queste funzionalità si applicano solo al nuovo hardware introdotto sul mercato. Poiché non sarà disponibile il supporto di build-in per queste funzionalità, non è probabile che un server fisico di cui viene eseguita la migrazione da Windows Server 2008 a Windows Server 2008 R2 sarà in impatto. Se queste funzionalità sono disponibili nel server di cui viene eseguita la migrazione, non sono previste modifiche dirette.
-   **Virtualizzazione di Servizi terminal:** Questa funzionalità non avrà alcun impatto sui clienti o sugli ISV durante la migrazione da Windows Server 2008 a Windows Server 2008 R2. Le applicazioni che sfruttano Servizi terminal possono essere influenzate. Questa funzionalità si integra direttamente con TS e pertanto le applicazioni che configurano TS possono richiedere l'aggiornamento per gestire questa nuova funzionalità.

## <a name="mitigation"></a>Mitigazione

-   **Live Migration:** Fornire indicazioni prescrittive agli utenti finali con procedure consigliate e raccomandazioni per la progettazione del sistema di archiviazione. È necessario informare l'utente finale delle opzioni e delle raccomandazioni.

## <a name="leveraging-capabilitities"></a>Uso delle funzionalità

-   **Live Migration:** Questa funzionalità abilita l'ambiente IT dinamico. Gestione della virtualizzazione Gli sviluppatori di applicazioni devono modificare l'applicazione per sfruttare questa nuova funzionalità. Microsoft rende disponibili pubblicamente le interfacce WMI per consentire a uno sviluppatore di integrare applicazioni con questa funzionalità.
-   **Virtualizzazione di Servizi terminal:** Questa funzionalità consente un nuovo scenario di virtualizzazione. Le applicazioni che sfruttano Servizi terminal possono essere influenzate. Questa funzionalità si integra direttamente con Servizi di installazione e pertanto le applicazioni che configurano Servizi t possono richiedere l'aggiornamento per gestire questa nuova funzionalità.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

[Interfacce di gestione WMI per Hyper-V v1](/previous-versions/windows/desktop/virtual/windows-virtualization-portal). Anche se la maggior parte di questo contenuto verrà applicata alla versione 2 di Hyper-V, una versione aggiornata con informazioni specifiche della versione 2 dovrebbe essere disponibile più vicino all'avvio di Windows 7.

 

 
