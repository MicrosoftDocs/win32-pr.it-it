---
title: Categorie di componenti e funzionamento
description: Categorie di componenti e funzionamento
ms.assetid: efbf4a25-3c73-4d09-a172-6676c6d6501b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddfd5580e12ce3d4a44ca251142e29f6eea8f9f5823cf18999f876a4ef732d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737017"
---
# <a name="component-categories-and-how-they-work"></a>Categorie di componenti e funzionamento

Le categorie di componenti identificano le aree di funzionalità supportate e necessarie da un componente software. Viene usata una voce del Registro di sistema per ogni categoria o area di funzionalità identificata. Ogni categoria di componenti è identificata da un identificatore univoco globale (GUID), quando un controllo viene installato viene registrato come controllo nel Registro di sistema usando l'ID della categoria di componenti per il controllo, vedere Registrazione automatica per i [controlli](self-registration-for-controls.md). All'interno della registrazione automatica dei controlli verranno registrate anche le categorie di componenti implementate e le categorie di componenti che richiede il supporto di un contenitore per ospitare correttamente il controllo.

Quando un contenitore di controlli offre controlli all'utente da inserire, consente solo all'utente di selezionare e creare un'istanza di tali controlli che saranno in grado di funzionare in modo adeguato in tale ambiente. Ad esempio, se il contenitore di controlli non supporta l'associazione dati, il contenitore non consentirà all'utente di selezionare e creare un'istanza dei controlli che dispongono di una voce nel Registro di sistema che indica che è necessaria la categoria del componente di databinding. È disponibile una finestra di dialogo comune per l'inserimento del controllo e le API per gestire le voci del Registro di sistema.

Le categorie di componenti non sono cumulative o esclusive, un controllo può richiedere qualsiasi combinazione di categorie di componenti per il funzionamento. Un controllo che non dispone di voci necessarie per le categorie di componenti potrebbe essere in grado di funzionare in qualsiasi contenitore di controlli e non richiede alcuna funzionalità specifica di un contenitore di controlli per il funzionamento.

Le categorie di componenti seguenti sono identificate qui, se necessario possono essere disponibili specifiche più dettagliate delle categorie.

-   [**Contenimento del controllo ISimpleFrameSite.**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)
-   Databinding semplice tramite [**l'interfaccia IPropertyNotifySink.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)
-   Databinding avanzato (supportato dalle interfacce di databinding aggiuntive di VB4.0).
-   Visual Basic interfacce private - [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat), [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)
-   Controlli che sono in grado di riconoscere Internet.
-   Controlli senza finestra.

Non si tratta di un elenco definitivo di categorie. È probabile che altre categorie siano definite in futuro con l'identificazione di nuovi requisiti. Un elenco aggiornato delle categorie di componenti è disponibile da Microsoft. questo elenco riflette le categorie di componenti identificate da Microsoft e da tutti gli altri fornitori che hanno informato Microsoft.

È importante ricordare che i controlli devono tentare di funzionare nel maggior numero possibile di ambienti. Se possibile, il controllo deve degradare le funzionalità quando viene inserito in un contenitore che non supporta determinate interfacce. Lo scopo delle categorie di componenti è impedire una situazione in cui il controllo viene inserito in un ambiente non idoneo e il controllo non può raggiungere l'attività desiderata. In genere, un controllo deve peggiorare normalmente quando le interfacce non sono presenti, un controllo può scegliere di avvisare l'utente con una finestra di messaggio che alcune funzionalità non sono disponibili o documentare chiaramente le funzionalità richieste da un contenitore di controlli per ottenere prestazioni ottimali.

Si noti che i controlli e i contenitori meno recenti non usano le categorie di componenti e si basano invece sulla parola chiave control presente sul controllo nel Registro di sistema. Per essere riconosciuti dai controlli contenitori meno recenti può voler registrare la parola chiave di controllo nel Registro di sistema, gli sviluppatori di controlli devono verificare che il controllo possa essere ospitato correttamente in tali contenitori prima di eseguire questa operazione. I contenitori che usano categorie di componenti possono usarli correttamente per ospitare i controlli meno recenti, perché la DLL della categoria di componenti gestisce il mapping. Esiste una categoria separata per i controlli meno recenti CATID ControlV1, in modo che un contenitore possa facoltativamente escluderli, \_ se necessario.

Poiché le categorie di componenti vengono identificate dai GUID, i contenitori che offrono funzionalità specifiche possono avere i propri ID categoria, generati usando uno strumento di generazione GUID. Tuttavia, ciò può compromettere il vantaggio dell'interoperabilità di controlli e contenitori, pertanto è preferibile usare, laddove possibile, categorie di componenti esistenti. I fornitori sono invitati a consultare insieme quando si definiscono nuove categorie di componenti per assicurarsi che soddisfino i requisiti comuni del marketplace e seguano lo stesso obiettivo di interoperabilità dei controlli ActiveX componenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

 




