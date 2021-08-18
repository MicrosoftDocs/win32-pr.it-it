---
description: Correzione dei problemi ActiveX di compatibilità dell'installazione per gli utenti standard
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: Correzione dei problemi ActiveX di compatibilità dell'installazione per gli utenti standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31dbcf8dfddd7e35a8a446f4b73dd1e5324cbe4695590511fa1cb220700b2c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994771"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>Correzione dei problemi ActiveX di compatibilità dell'installazione per gli utenti standard

Per sviluppare un ambiente desktop sicuro, è necessario mitigare le minacce da controlli ActiveX dannosi e fornire un livello appropriato di compatibilità delle applicazioni nell'ambiente. Un *ActiveX* controllo è una parte di codice eseguibile (in genere un file OCX in pacchetto all'interno di un file cab) che viene installato ed eseguito tramite Windows Internet Explorer. È possibile creare ActiveX per aggiungere funzionalità alle applicazioni Web che non è possibile ottenere facilmente usando codice HTML standard o uno script semplice.

L'installazione dei controlli ActiveX diventa un problema di compatibilità quando la migrazione a Windows 7 include una transizione per gli utenti standard. Questo tipo di transizione è una procedura consigliata comune in cui i professionisti IT spostano il proprio ambiente in un [account utente standard.](https://support.microsoft.com/hub/4338813/windows-help) Questa transizione non è un requisito per la distribuzione Windows Internet Explorer 8.

## <a name="activex-control-installation"></a>ActiveX Controllare l'installazione

ActiveX controlli hanno un modello di distribuzione di download ed esecuzione semplice. ActiveX i controlli vengono installati ed eseguiti tramite l'elemento **oggetto** HTML. **L'attributo CODEBASE** in questo elemento indica Internet Explorer (usando un URL) dove ottenere il controllo se non è già installato nel computer dell'utente. In tal caso, Internet Explorer il pacchetto di installazione associato, esegue la verifica dell'attendibilità sull'oggetto e richiede all'utente l'autorizzazione di installazione Internet Explorer.

Durante l'installazione, la pagina di rendering registra ed esegue il controllo . Dopo l'installazione del controllo, tutti gli utenti standard possono eseguire il controllo. Questo semplice meccanismo di distribuzione ed esecuzione offre un modo semplice per distribuire i componenti agli utenti dell'applicazione Web. Gli utenti dell'account standard non possono tuttavia installare direttamente i controlli ActiveX computer e potrebbero essere necessari privilegi di amministratore per completare l'installazione.

## <a name="activex-installer-service-axis"></a>ActiveX Servizio di installazione (AXIS)

Il ActiveX Installer Service (AXIS) consente di distribuire ActiveX controlli usando Criteri di gruppo nei computer di un'organizzazione. È possibile configurare AXIS Criteri di gruppo impostazioni, che è possibile modificare usando Console Gestione Criteri di gruppo (GPMC) o Editor Criteri di gruppo locali.

Per AXIS sono disponibili due impostazioni dei criteri:

-   L'impostazione dei criteri Siti di installazione approvati per i controlli ActiveX è costituita da un elenco di siti di installazione approvati, che l'ASSE usa per determinare se è possibile installare un ActiveX controllo.
-   L ActiveX'impostazione dei criteri di installazione dei siti nelle aree attendibili identifica come è possibile usare le aree siti attendibili per installare i ActiveX attendibili.

Quando un sito Web tenta di installare un controllo ActiveX, l'ASSE verifica se l'URL del sito Web è elencato nell'elenco dei siti di installazione approvati o come parte dell'area siti attendibili. Se il sito si trova in uno di questi elenchi, AXIS verifica che il sito soddisfi i requisiti definiti dal criterio. Se il sito e il controllo ActiveX soddisfano tutti i requisiti del criterio, il controllo viene installato. Per ulteriori informazioni vedere [Amministrazione del servizio ActiveX Installer](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
