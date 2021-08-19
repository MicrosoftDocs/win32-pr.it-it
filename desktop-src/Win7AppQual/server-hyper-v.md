---
description: Server Hyper-V
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: Server Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cab162355e298cbc21c1c43d8b1a0d16b8c23f958e06c7fb28a8ecb6e3309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328711"
---
# <a name="server-hyper-v"></a>Server Hyper-V

## <a name="platforms"></a>Piattaforme

 **Client** - Windows XP \| Windows Vista \| Windows 7  
**Server** - Windows Server 2008 \| Windows Server 2008 R2  

## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

La virtualizzazione dei server consente l'esecuzione di più sistemi operativi in un'unica macchina fisica come macchine virtuali, consentendo di consolidare i carichi di lavoro dei computer server sottoutilizzati in un numero inferiore di computer completamente utilizzati. Windows 7 include diversi miglioramenti alla versione Windows Server 2008:

-   **Live Migration:** In Windows Server 2008 è stata completata la migrazione rapida. Con Live Migration, è stata migliorata la velocità di migrazione e la flessibilità di archiviazione.
-   **Supporto del processore logico:** Sono stati aumentati i processori host logici da 16LP a 64LP.
-   **Archiviazione a caldo:** È ora possibile aggiungere altri dischi rigidi virtuali o pass-through a una macchina virtuale in esecuzione senza disattivare la macchina virtuale.
-   **Nuovo supporto hardware:** È stato aggiunto il supporto per le tecnologie incluse nei nuovi processori e nelle schede di rete disponibili sul mercato, tra cui SLAT (Second Level Translation), TCP Offload (Chimney) e VMdQ.
-   **Virtualizzazione Servizi terminal ::** È stata centralizzata una soluzione desktop per Hyper-V.

## <a name="manifestation-of-impact"></a>Impatto significativo

-   **Live Migration:** Potrebbe essere necessario modificare il modo in cui sono stati architettati i sistemi di archiviazione per sfruttare appieno questa tecnologia. Anche se queste modifiche potrebbero non essere necessarie, è possibile scegliere di implementarle per sfruttare appieno i vantaggi. Potrebbe essere necessaria un'applicazione di gestione per orchestrare Live Migration.
-   **Supporto del processore logico:** Questa funzionalità non avrà alcun impatto sui clienti o sugli ISV durante la migrazione da Windows Server 2008 a Windows Server 2008 R2.
-   **Archiviazione a caldo:** Questa funzionalità non avrà alcun impatto sui clienti o sugli ISV durante la migrazione da Windows Server 2008 a Windows Server 2008 R2. Le applicazioni di gestione che configurano le impostazioni di una macchina virtuale possono richiedere l'aggiornamento per gestire questa nuova funzionalità.
-   **Nuovo supporto hardware:** Queste funzionalità si applicano solo al nuovo hardware introdotto sul mercato. Poiché non sarà disponibile il supporto di build-in per queste funzionalità, non è probabile che un server fisico di cui viene eseguita la migrazione da Windows Server 2008 a Windows Server 2008 R2 sarà danneggiato. Se queste funzionalità sono disponibili nel server di cui viene eseguita la migrazione, non sono previste modifiche dirette.
-   **Virtualizzazione di Servizi terminal:** Questa funzionalità non avrà alcun impatto per i clienti o gli ISV durante la migrazione da Windows Server 2008 a Windows Server 2008 R2. Le applicazioni che sfruttano Servizi terminal possono essere influenzate. Questa funzionalità si integra direttamente con TS e pertanto le applicazioni che configurano TS possono richiedere l'aggiornamento per gestire questa nuova funzionalità.

## <a name="mitigation"></a>Strategia di riduzione del rischio

-   **Live Migration:** Fornire indicazioni prescrittive agli utenti finali con procedure consigliate e raccomandazioni per la progettazione del sistema di archiviazione. È necessario informare l'utente finale delle opzioni e delle raccomandazioni.

## <a name="leveraging-capabilitities"></a>Uso delle funzionalità

-   **Live Migration:** Questa funzionalità abilita l'ambiente IT dinamico. Gestione della virtualizzazione Gli sviluppatori di applicazioni devono modificare l'applicazione per sfruttare questa nuova funzionalità. Microsoft rende disponibili pubblicamente le interfacce WMI per consentire a uno sviluppatore di integrare applicazioni con questa funzionalità.
-   **Virtualizzazione di Servizi terminal:** Questa funzionalità consente un nuovo scenario di virtualizzazione. Le applicazioni che sfruttano Servizi terminal possono essere influenzate. Questa funzionalità si integra direttamente con TS e pertanto le applicazioni che configurano TS possono richiedere l'aggiornamento per gestire questa nuova funzionalità.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

[Interfacce di gestione WMI per Hyper-V v1.](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) Sebbene la maggior parte di questo contenuto sia applicabile alla versione 2 di Hyper-V, una versione aggiornata con informazioni specifiche della versione 2 dovrebbe essere disponibile più vicino all'avvio Windows 7.

 

 
