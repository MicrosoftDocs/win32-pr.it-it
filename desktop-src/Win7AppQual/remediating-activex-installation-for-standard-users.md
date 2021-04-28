---
description: Correzione dei problemi di compatibilità dell'installazione di ActiveX per gli utenti standard
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: Correzione dei problemi di compatibilità dell'installazione di ActiveX per gli utenti standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88b26ebd0c6e4887a8a304aeab725b176ee04a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116409"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>Correzione dei problemi di compatibilità dell'installazione di ActiveX per gli utenti standard

Per sviluppare un ambiente desktop sicuro, è necessario attenuare le minacce da controlli ActiveX dannosi e fornire un livello appropriato di compatibilità delle applicazioni nell'ambiente. Un *controllo ActiveX* è un frammento di codice eseguibile (in genere un file OCX in pacchetto all'interno di un file CAB) installato ed eseguito tramite Windows Internet Explorer. È possibile creare controlli ActiveX per aggiungere funzionalità alle applicazioni Web che non è possibile ottenere facilmente usando codice HTML standard o uno script semplice.

L'installazione dei controlli ActiveX diventa un problema di compatibilità quando la migrazione a Windows 7 include una transizione per gli utenti standard. Questo tipo di transizione è una procedura consigliata comune in cui i professionisti IT spostano l'ambiente in un [account utente standard.](https://support.microsoft.com/hub/4338813/windows-help) Questa transizione non è un requisito per la distribuzione di Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>Installazione del controllo ActiveX

I controlli ActiveX hanno un semplice modello di download ed esecuzione della distribuzione. I controlli ActiveX vengono installati ed eseguiti tramite l'elemento **oggetto** HTML . **L'attributo CODEBASE** in questo elemento indica Internet Explorer (tramite un URL) dove ottenere il controllo se non è già installato nel computer dell'utente. In tal caso, Internet Explorer il pacchetto di installazione associato, esegue la verifica dell'attendibilità sull'oggetto e richiede all'utente l'autorizzazione di installazione in Internet Explorer.

Durante l'installazione, la pagina di rendering registra ed esegue il controllo . Dopo l'installazione del controllo, tutti gli utenti standard possono eseguire il controllo. Questo semplice meccanismo di distribuzione ed esecuzione offre un modo semplice per distribuire i componenti agli utenti dell'applicazione Web. Tuttavia, gli utenti con account standard non possono installare direttamente i controlli ActiveX per computer e potrebbero avere bisogno di privilegi di amministratore per completare l'installazione.

## <a name="activex-installer-service-axis"></a>Servizio ActiveX Installer (AXIS)

Il servizio ActiveX Installer (AXIS) consente di distribuire controlli ActiveX usando Criteri di gruppo nei computer di un'organizzazione. È possibile configurare AXIS Criteri di gruppo impostazioni, che è possibile modificare usando Console Gestione Criteri di gruppo (GPMC) o Editor Criteri di gruppo locali.

Per AXIS sono disponibili due impostazioni dei criteri:

-   L'impostazione dei criteri Siti di installazione approvati per controlli ActiveX è costituita da un elenco di siti di installazione approvati, che l'ASSE usa per determinare se è possibile installare un controllo ActiveX.
-   L'impostazione dei criteri di installazione ActiveX per i siti nelle aree attendibili identifica come è possibile usare le aree Siti attendibili per installare i controlli ActiveX.

Quando un sito Web tenta di installare un controllo ActiveX, AXIS verifica se l'URL del sito Web è elencato nell'elenco dei siti di installazione approvati o come parte dell'area siti attendibili. Se il sito si trova in uno di questi elenchi, AXIS verifica che il sito soddisfi i requisiti definiti dal criterio. Se il sito e il controllo ActiveX soddisfano tutti i requisiti del criterio, il controllo viene installato. Per ulteriori informazioni vedere [Amministrazione del servizio ActiveX Installer](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
