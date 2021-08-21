---
description: Il provider Windows Driver Model (WDM) concede l'accesso a classi, istanze, metodi ed eventi dei driver hardware conformi al modello WDM.
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: Accesso ai dati dai driver di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bec478f83ddbc6d58419710fb868ddd233f820a06004210c1dac495de86b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131914"
---
# <a name="accessing-data-from-device-drivers"></a>Accesso ai dati dai driver di dispositivo

Il provider Windows Driver Model (WDM) concede l'accesso a classi, istanze, metodi ed eventi dei driver hardware conformi al modello WDM. Le classi per i driver hardware si trovano nello spazio \\ \\ dei nomi WMI \\ radice.

Il provider WDM è di interesse per gli utenti che scrivono driver di dispositivo e per gli amministratori interessati ai dati dei driver di dispositivo.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Informazioni per i writer di driver di dispositivo](#information-for-device-driver-writers)
-   [Informazioni per amministratori e utenti dei dati dei driver](#information-for-administrators-and-users-of-driver-data)
-   [Argomenti correlati](#related-topics)

## <a name="information-for-device-driver-writers"></a>Informazioni per i writer di driver di dispositivo

Le classi WMI correlate a un driver di dispositivo specifico vengono create quando il provider WDM estrae il file MOF binario dal file eseguibile del driver di dispositivo. Ciò avviene ogni volta che WMI viene avviato, viene installato un nuovo driver di dispositivo o viene eliminata l'istanza di [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) per un driver specifico. Controllando Wmiprov.log, è possibile determinare se si è verificato un errore durante l'estrazione del file MOF binario. I dettagli [degli errori mofcomp](mofcomp.md) sono riportati in Mofcomp.log. Per altre informazioni, vedere [File di log WMI.](wmi-log-files.md) Per motivi di prestazioni, il provider WDM non genera eventi durante la creazione o l'eliminazione di classi a causa dell'avvio o dell'arresto di un provider WDM.

Il provider WDM trasforma tutti i dati WNODE in informazioni sulla classe. Se si verifica un errore durante la trasformazione dei dati da WNODE ai dati della classe, viene segnalato in Wmiprov.log con l'intestazione formattata e i byte sottoposti a rendering nello stesso formato di un dump della memoria.

Le modifiche apportate alle impostazioni di sicurezza dei driver non vengono applicate fino a quando il provider WDM non viene scaricato e ricaricato. Per altre informazioni, vedere [Scaricamento di un provider.](unloading-a-provider.md)

WMI può anche rendere disponibili contatori con prestazioni elevate per i driver hardware. Per altre informazioni sulla creazione di classi a prestazioni elevate e sulla visualizzazione dei dati in Monitoraggio di sistema Perfmon, vedere [Improving the Efficiency of an Instance Provider](improving-the-efficiency-of-an-instance-provider.md). Per altre informazioni sulla scrittura di driver di dispositivo abilitati per WMI, vedere [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) . Per altre informazioni sui qualificatori specifici di WDM nel file MOF, vedere [**Qualificatori specifici del provider WDM.**](qualifiers-specific-to-the-wdm-provider.md)

## <a name="information-for-administrators-and-users-of-driver-data"></a>Informazioni per amministratori e utenti dei dati dei driver

L'elenco delle istanze della classe [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) fornisce un elenco dei driver nel sistema e informazioni sul fatto che il provider WDM sia riuscito a compilare i file MOF per ogni driver. È possibile forzare il provider a ricompilare e rigenerare le classi per un driver eliminando l'istanza di WMIBinaryMofResource che rappresenta tale driver. I dettagli [degli errori mofcomp](mofcomp.md) sono riportati nel file Mofcomp.log.

Se lo spazio dei nomi WMI è danneggiato, può essere eliminato e riaperto per forzare WDM a ricompilare le classi di driver. Per altre informazioni sull'apertura di uno spazio dei nomi, vedere [Creazione di gerarchie all'interno di WMI.](creating-hierarchies-within-wmi.md)

Le classi di driver possono occasionalmente essere "bloccate" se il caricamento dei driver viene interrotto o si verificano altre operazioni anomale. Il provider WDM cerca e pulisce le classi "bloccate" solo quando viene installato un nuovo driver o quando il valore della chiave del Registro di sistema Software **\\ Microsoft \\ WBEM \\ WDMProvider** **ProcessStrandedClasses** è impostato su **TRUE.** L'impostazione di questo **valore su TRUE** rallenta le prestazioni di avvio di WMI a causa dell'operazione di pulizia. Il valore predefinito è **FALSE.** Il provider WDM controlla questo valore del Registro di sistema solo quando lo spazio dei nomi \\ "Root Wmi" viene aperto per la prima volta.

Se vengono apportate modifiche di sicurezza a un driver di dispositivo WDM, le modifiche non verranno applicate fino a quando il provider WDM non viene scaricato e ricaricato. A tale Windows, è necessario che il servizio Gestione applicazioni venga arrestato e riavviato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di WMI](using-wmi.md)
</dt> </dl>

 

 
