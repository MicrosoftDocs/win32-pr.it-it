---
description: .
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: Server Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6997074e000b17a119a838df5b6fab961b8ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319839"
---
# <a name="server-hyper-v"></a>Server Hyper-V

## <a name="platforms"></a>Piattaforme

 **Client** -Windows XP Windows \| Vista Windows \| 7  
**Server** -windows Server 2008 \| Windows Server 2008 R2  

## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -bassa  





## <a name="description"></a>Descrizione

La virtualizzazione dei server consente l'esecuzione di più sistemi operativi in un singolo computer fisico come macchine virtuali (VM), consentendo di consolidare i carichi di lavoro di computer server sottoutilizzati su un numero inferiore di computer completamente utilizzati. Windows 7 include diversi miglioramenti alla versione di Windows Server 2008:

-   **Live Migration:** In Windows Server 2008 abbiamo avuto una migrazione rapida. Con Live Migration, abbiamo migliorato la velocità di migrazione e la flessibilità di archiviazione.
-   **Supporto del processore logico:** Sono stati migliorati i processori host logici da 16LP a 64LP.
-   **Aggiunta a caldo di archiviazione:** A questo punto è possibile aggiungere altri dischi VHD o pass-through a una macchina virtuale in esecuzione senza spegnere la macchina virtuale.
-   **Nuovo supporto hardware:** È stato aggiunto il supporto per le tecnologie incluse nei nuovi processori e le schede di rete provenienti dal mercato, tra cui la conversione di secondo livello (stecca), TCP Offload (Chimney) e VMdQ.
-   **TSv (Servizi terminal Virtualization):** È stata centralizzata la soluzione desktop per Hyper-V.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

-   **Live Migration:** Potrebbe essere necessario modificare il modo in cui sono stati architettati i sistemi di archiviazione per sfruttare appieno questa tecnologia. Sebbene queste modifiche potrebbero non essere necessarie, è possibile scegliere di implementarle per sfruttare appieno i vantaggi. Potrebbe essere necessaria un'applicazione di gestione per orchestrare Live Migration.
-   **Supporto del processore logico:** Questa funzionalità non avrà alcun effetto su clienti o ISV durante la migrazione da Windows Server 2008 a Windows Server 2008 R2.
-   **Aggiunta a caldo di archiviazione:** Questa funzionalità non avrà alcun effetto su clienti o ISV durante la migrazione da Windows Server 2008 a Windows Server 2008 R2. Le applicazioni di gestione che configurano le impostazioni di una macchina virtuale possono richiedere l'aggiornamento per poter gestire questa nuova funzionalità.
-   **Nuovo supporto hardware:** Queste funzionalità si applicano solo ai nuovi componenti hardware introdotti sul mercato. Poiché non avrà il supporto di compilazione per queste funzionalità, non è probabile che venga influenzato un server fisico di cui è in corso la migrazione da Windows Server 2008 a Windows Server 2008 R2. Se queste funzionalità sono disponibili nel server di cui viene eseguita la migrazione, non vengono previste modifiche dirette.
-   **Virtualizzazione di Servizi terminal:** Questa funzionalità non avrà alcun effetto su clienti o ISV durante la migrazione da Windows Server 2008 a Windows Server 2008 R2. Le applicazioni che sfruttano Servizi terminal possono essere interessate. Questa funzionalità si integra direttamente con Servizi terminal e pertanto le applicazioni che configurano TS possono richiedere l'aggiornamento per poter gestire questa nuova funzionalità.

## <a name="mitigation"></a>Strategia di riduzione del rischio

-   **Live Migration:** Fornire indicazioni per gli utenti finali con procedure consigliate e consigli per la progettazione del sistema di archiviazione. È necessario informare l'utente finale sulle opzioni e sulle raccomandazioni.

## <a name="leveraging-capabilitities"></a>Uso di Capabilitities

-   **Live Migration:** Questa funzionalità consente l'ambiente IT dinamico. Gli sviluppatori di applicazioni di gestione della virtualizzazione devono modificare l'applicazione per sfruttare questa nuova funzionalità. Microsoft renderà le interfacce WMI disponibili pubblicamente per consentire agli sviluppatori di integrare le applicazioni con questa funzionalità.
-   **Virtualizzazione di Servizi terminal:** Questa funzionalità consente un nuovo scenario di virtualizzazione. Le applicazioni che sfruttano Servizi terminal possono essere interessate. Questa funzionalità si integra direttamente con Servizi terminal e pertanto le applicazioni che configurano TS possono richiedere l'aggiornamento per poter gestire questa nuova funzionalità.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

[Interfacce di gestione WMI per Hyper-V V1](/previous-versions/windows/desktop/virtual/windows-virtualization-portal). Sebbene la maggior parte di questo contenuto si applichi alla versione V2 di Hyper-V, una versione aggiornata con informazioni specifiche di v2 dovrebbe essere disponibile più vicino al lancio di Windows 7.

 

 
