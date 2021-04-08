---
title: Antimalware ad esecuzione anticipata
description: Antimalware ad esecuzione anticipata
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104058402"
---
# <a name="early-launch-antimalware"></a>Antimalware ad esecuzione anticipata

## <a name="platforms"></a>Piattaforme

 **Client** -Windows 8  
**Server** -Windows Server 2012  

## <a name="description"></a>Descrizione

Poiché il software antimalware (AM) è diventato migliore e migliore nel rilevamento del malware di runtime, anche gli utenti malintenzionati stanno migliorando la creazione di rootkit che possono nascondere il rilevamento. Il rilevamento di malware che inizia nelle prime fasi del ciclo di avvio è una sfida che la maggior parte dei fornitori di AM deve affrontare diligentemente. In genere, creano hack di sistema non supportati dal sistema operativo host e possono effettivamente comportare il posizionamento del computer in uno stato instabile. Fino a questo punto, Windows non ha fornito un metodo efficace per rilevare e risolvere queste minacce iniziali di avvio.

In Windows 8 è stata introdotta una nuova funzionalità denominata avvio protetto, che protegge i componenti e la configurazione di avvio di Windows, e carica un driver anti-malware (ELAM) con avvio rapido. Questo driver viene avviato prima di altri driver di avvio e consente la valutazione di tali driver e consente al kernel di Windows di decidere se deve essere inizializzato.

## <a name="manifestation"></a>Manifestazione

Quando viene avviato per primo dal kernel, ELAM è sicuro di essere avviato prima di qualsiasi software di terze parti ed è quindi in grado di rilevare malware nel processo di avvio e di impedirne l'inizializzazione.

## <a name="mitigation"></a>Strategia di riduzione del rischio

I driver di avvio vengono inizializzati in base alla classificazione restituita dal driver ELAM in base ai criteri di inizializzazione. Per impostazione predefinita, i criteri inizializzano i driver noti e sconosciuti, ma non inizializzano i driver noti non validi. Un amministratore di sistema può specificare un criterio personalizzato tramite Criteri di gruppo in grado di impedire l'inizializzazione di driver sconosciuti o l'abilitazione di driver critici per il processo di avvio, ma che sono stati manomessi, l'avvio deve essere inizializzato.

## <a name="solution"></a>Soluzione

È necessario registrare un driver ELAM per le richiamate del kernel per ottenere informazioni su ogni driver di avvio che viene inizializzato. Il driver ELAM può quindi restituire una classificazione per ogni driver. Queste funzioni sono obbligatorie:

-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

Un driver ELAM può anche registrarsi per i callback del registro di sistema. Questa operazione consente al driver ELAM di ispezionare i dati di configurazione usati da ogni driver di avvio. Il driver ELAM può quindi bloccare o modificare i dati prima che vengano usati dai driver di avvio, se necessario. Queste funzioni sono obbligatorie:

-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

Per altre informazioni sui requisiti dei driver ELAM e sull'utilizzo delle API, vedere [antimalware ad esecuzione anticipata](/windows-hardware/drivers/install/early-launch-antimalware).

## <a name="tests"></a>Test

I driver ELAM devono essere firmati appositamente da Microsoft per assicurarsi che vengano avviati dal kernel di Windows nelle fasi iniziali del processo di avvio. Per ottenere la firma, i driver ELAM devono passare un set di test di certificazione per verificare le prestazioni e altri comportamenti. Questi test sono inclusi nel kit di certificazione hardware di Windows.

## <a name="resources"></a>Risorse

-   [Antimalware ad esecuzione anticipata](/windows-hardware/drivers/install/early-launch-antimalware)
-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [Certificazione dell'hardware con Windows Hardware Certification Kit Build Conference Presentation](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [Scarica kit e strumenti](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
