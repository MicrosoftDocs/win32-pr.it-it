---
title: Antimalware ad avvio anticipato
description: Antimalware ad avvio anticipato
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1ca8e52f9d2465038e68b6b585bed70b974432566b3b67d080c97bb998103f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852197"
---
# <a name="early-launch-antimalware"></a>Antimalware ad avvio anticipato

## <a name="platforms"></a>Piattaforme

 **Client** - Windows 8  
**Server** - Windows Server 2012  

## <a name="description"></a>Descrizione

Poiché il software antimalware (AM) è diventato sempre più in grado di rilevare malware di runtime, anche gli utenti malintenzionati stanno diventando più esperti nella creazione di rootkit che possono nascondersi dal rilevamento. Il rilevamento di malware che inizia all'inizio del ciclo di avvio è una sfida che la maggior parte dei fornitori am affronta in modo accurato. In genere, creano hack di sistema che non sono supportati dal sistema operativo host e possono effettivamente comportare il posizionamento del computer in uno stato instabile. Fino a questo punto, Windows non ha fornito un modo efficace per am per rilevare e risolvere queste minacce di avvio anticipato.

Windows 8 introduce una nuova funzionalità denominata Avvio protetto, che protegge la configurazione e i componenti di avvio di Windows e carica un driver antimalware ad avvio anticipato. Questo driver viene avviato prima di altri driver di avvio e abilita la valutazione di tali driver e consente al kernel Windows decidere se devono essere inizializzati.

## <a name="manifestation"></a>Manifestazione

Avviando prima dal kernel, viene garantito l'avvio di ELAM prima di qualsiasi software di terze parti e pertanto è in grado di rilevare malware nel processo di avvio e impedirne l'inizializzazione.

## <a name="mitigation"></a>Strategia di riduzione del rischio

I driver di avvio vengono inizializzati in base alla classificazione restituita dal driver ELAM in base a un criterio di inizializzazione. Per impostazione predefinita, i criteri inizializzano i driver noti corretti e sconosciuti, ma non inizializzano i driver noti non corretti. Un amministratore di sistema può specificare criteri personalizzati tramite Criteri di gruppo che possono impedire l'inizializzazione di driver sconosciuti o abilitare l'inizializzazione dei driver critici per il processo di avvio, ma che sono stati manomissionati.

## <a name="solution"></a>Soluzione

Un driver ELAM deve registrarsi per i callback del kernel per ottenere informazioni su ogni driver di avvio durante l'inizializzazione. Il driver ELAM può quindi restituire una classificazione per ogni driver. Queste funzioni sono obbligatorie:

-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

Un driver ELAM può anche registrarsi per i callback del Registro di sistema. In questo modo il driver ELAM può esaminare i dati di configurazione usati da ogni driver di avvio. Il driver ELAM può quindi bloccare o modificare i dati prima che venga usato dai driver di avvio, se necessario. Queste funzioni sono obbligatorie:

-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

Per altre informazioni sui requisiti dei driver ELAM e sull'utilizzo delle API, vedere [Avvio anticipato di Antimalware.](/windows-hardware/drivers/install/early-launch-antimalware)

## <a name="tests"></a>Test

I driver ELAM devono essere firmati in modo speciale da Microsoft per assicurarsi che siano avviati dal kernel Windows all'inizio del processo di avvio. Per ottenere la firma, i driver ELAM devono superare un set di test di certificazione per verificare le prestazioni e altri comportamenti. Questi test sono inclusi in Windows Kit di certificazione hardware.

## <a name="resources"></a>Risorse

-   [Antimalware ad esecuzione anticipata](/windows-hardware/drivers/install/early-launch-antimalware)
-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [Certifying hardware with the Windows Hardware Certification Kit Build Conference presentation](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [Scaricare kit e strumenti](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
