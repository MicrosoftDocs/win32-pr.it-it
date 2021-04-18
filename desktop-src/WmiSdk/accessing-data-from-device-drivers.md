---
description: Il provider di Windows Driver Model (WDM) concede l'accesso alle classi, alle istanze, ai metodi e agli eventi dei driver hardware conformi al modello WDM.
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: Accesso ai dati dai driver di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a59b59116ca0f71178fb2faed290d6bc76c9d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319313"
---
# <a name="accessing-data-from-device-drivers"></a>Accesso ai dati dai driver di dispositivo

Il provider di Windows Driver Model (WDM) concede l'accesso alle classi, alle istanze, ai metodi e agli eventi dei driver hardware conformi al modello WDM. Le classi per i driver hardware si trovano nello \\ \\ \\ spazio dei nomi WMI radice.

Il provider WDM è di interesse per coloro che scrivono i driver di dispositivo e gli amministratori interessati ai dati dei driver di dispositivo.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Informazioni per i writer di driver di dispositivo](#information-for-device-driver-writers)
-   [Informazioni per amministratori e utenti dei dati dei driver](#information-for-administrators-and-users-of-driver-data)
-   [Argomenti correlati](#related-topics)

## <a name="information-for-device-driver-writers"></a>Informazioni per i writer di driver di dispositivo

Le classi WMI correlate a un driver di dispositivo specifico vengono create quando il provider WDM estrae il file MOF binario dal file eseguibile del driver di dispositivo. Questa operazione viene eseguita ogni volta che WMI viene avviato, viene installato un nuovo driver di dispositivo o viene eliminata l'istanza di [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) per un driver specifico. Controllando wmiprov. log, è possibile determinare se si è verificato un errore durante l'estrazione del file MOF binario. I dettagli degli errori [mofcomp](mofcomp.md) vengono segnalati in mofcomp. log. Per ulteriori informazioni, vedere [file di log WMI](wmi-log-files.md). Per motivi di prestazioni, il provider WDM non genera eventi durante la creazione o l'eliminazione di classi a causa dell'avvio o dell'arresto di un provider WDM.

Il provider WDM trasforma tutti i dati di WNODE in informazioni sulla classe. Se si verifica un errore durante la trasformazione dei dati da WNODE ai dati della classe, questo viene segnalato in wmiprov. log con l'intestazione formattata e i byte sottoposti a rendering nello stesso formato di un dump di memoria.

Le modifiche apportate alle impostazioni di sicurezza del driver non hanno effetto finché il provider WDM non viene scaricato e ricaricato. Per ulteriori informazioni, vedere [scaricamento di un provider](unloading-a-provider.md).

WMI può inoltre creare contatori a prestazioni elevate per i driver hardware disponibili. Per ulteriori informazioni sulla creazione di classi a prestazioni elevate e sulla visualizzazione dei dati in monitoraggio di sistema PerfMon, vedere [miglioramento dell'efficienza di un provider di istanze](improving-the-efficiency-of-an-instance-provider.md). Per ulteriori informazioni sulla scrittura di driver di dispositivo abilitati per WMI, vedere [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) . Per ulteriori informazioni sui qualificatori specifici di WDM nel file MOF, vedere [**qualificatori specifici del provider WDM**](qualifiers-specific-to-the-wdm-provider.md).

## <a name="information-for-administrators-and-users-of-driver-data"></a>Informazioni per amministratori e utenti dei dati dei driver

Elencando le istanze della classe [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) è disponibile un elenco dei driver nel sistema e informazioni sull'eventuale riuscita del provider WDM a compilare il file MOF per ogni driver. È possibile forzare il provider a ricompilare e rigenerare le classi per un driver eliminando l'istanza di WMIBinaryMofResource che rappresenta tale driver. I dettagli degli errori [mofcomp](mofcomp.md) vengono segnalati in mofcomp. log.

Se lo spazio dei nomi WMI è danneggiato, è possibile eliminarlo e riaprirlo per forzare la ricompilazione delle classi di driver da parte di WDM. Per ulteriori informazioni sull'apertura di uno spazio dei nomi, vedere [creazione di gerarchie all'interno di WMI](creating-hierarchies-within-wmi.md).

Le classi di driver possono talvolta ottenere "Stranded" Se il caricamento del driver viene interrotto o se si verificano altre operazioni anomale. Il provider WDM effettuerà la ricerca e la pulizia delle classi "Stranded" solo quando viene installato un nuovo driver o quando il valore della chiave del registro di sistema **\\ Microsoft \\ WBEM \\ WDMProvider del software** **ProcessStrandedClasses** è impostato su **true**. L'impostazione di questo valore su **true** rallenta le prestazioni di avvio WMI a causa dell'operazione di pulizia. Il valore predefinito è **false**. Il provider WDM controlla solo questo valore del registro di sistema quando lo \\ spazio dei nomi "WMI radice" viene aperto per la prima volta.

Se vengono apportate modifiche di sicurezza a un driver di dispositivo WDM, le modifiche non verranno applicate finché il provider WDM non viene scaricato e ricaricato. Per eseguire questa operazione, è necessario arrestare e riavviare il servizio di gestione di Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di WMI](using-wmi.md)
</dt> </dl>

 

 
