---
description: .
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: Correzione dei problemi di compatibilità di installazione ActiveX per gli utenti standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e50ed2aa9e428164e39b377b65c418d82df1e5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761435"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>Correzione dei problemi di compatibilità di installazione ActiveX per gli utenti standard

Per sviluppare un ambiente desktop protetto, è necessario attenuare le minacce da controlli ActiveX dannosi e fornire un livello appropriato di compatibilità delle applicazioni nell'ambiente in uso. Un *controllo ActiveX* è un frammento di codice eseguibile, in genere un file ocx incluso in un file CAB, installato ed eseguito tramite Windows Internet Explorer. È possibile creare controlli ActiveX per aggiungere funzionalità alle applicazioni Web che non è possibile ottenere facilmente utilizzando codice HTML standard o un semplice script.

L'installazione dei controlli ActiveX diventa un problema di compatibilità quando la migrazione a Windows 7 include una transizione per gli utenti standard. Questo tipo di transizione è una procedura consigliata comune in cui i professionisti IT spostano l'ambiente in un [account utente standard](https://support.microsoft.com/hub/4338813/windows-help). Questa transizione non è un requisito per la distribuzione di Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>Installazione del controllo ActiveX

I controlli ActiveX hanno un semplice modello di distribuzione di download ed esecuzione. I controlli ActiveX vengono installati ed eseguiti tramite l'elemento HTML **Object** . L'attributo **CODEbase** di questo elemento indica a Internet Explorer (tramite un URL) dove ottenere il controllo se non è già installato nel computer dell'utente. In tal caso, Internet Explorer Scarica il pacchetto di installazione associato, esegue la verifica dell'attendibilità sull'oggetto e chiede all'utente l'autorizzazione per l'installazione in Internet Explorer.

Durante l'installazione, nella pagina di rendering viene registrato ed eseguito il controllo. Dopo l'installazione del controllo, gli utenti standard possono eseguire il controllo. Questo semplice meccanismo di distribuzione ed esecuzione fornisce un modo semplice per distribuire i componenti agli utenti dell'applicazione Web. Ma gli utenti con account standard non possono installare direttamente i controlli ActiveX per computer e potrebbero avere bisogno di privilegi di amministratore per completare l'installazione.

## <a name="activex-installer-service-axis"></a>Servizio ActiveX Installer (asse)

Il servizio ActiveX Installer (AXIS) consente di distribuire i controlli ActiveX usando Criteri di gruppo nei computer di un'organizzazione. È possibile configurare l'asse in base a Criteri di gruppo impostazioni, che è possibile modificare usando il Console Gestione Criteri di gruppo (GPMC) o il Editor Criteri di gruppo locali.

Sono disponibili due impostazioni dei criteri per l'asse:

-   L'impostazione dei criteri per i controlli ActiveX dei siti di installazione approvati è costituita da un elenco di siti di installazione approvati utilizzati dall'asse per determinare se è possibile installare un controllo ActiveX.
-   L'impostazione criteri di installazione ActiveX per siti in zone attendibili identifica il modo in cui è possibile usare le zone dei siti attendibili per installare i controlli ActiveX.

Quando un sito Web tenta di installare un controllo ActiveX, l'asse verifica se l'URL del sito Web è elencato nell'elenco dei siti di installazione approvati o come parte dell'area siti attendibili. Se il sito è in uno di questi elenchi, l'asse garantisce che il sito soddisfi i requisiti definiti dal criterio. Se il sito e il controllo ActiveX soddisfano tutti i requisiti del criterio, il controllo viene installato. Per ulteriori informazioni vedere [Amministrazione del servizio ActiveX Installer](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
