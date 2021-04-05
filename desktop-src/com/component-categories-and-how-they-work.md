---
title: Categorie di componenti e modalità di funzionamento
description: Categorie di componenti e modalità di funzionamento
ms.assetid: efbf4a25-3c73-4d09-a172-6676c6d6501b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf8065584ae2dc83e470428b7345eb2d9321d32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955164"
---
# <a name="component-categories-and-how-they-work"></a>Categorie di componenti e modalità di funzionamento

Le categorie di componenti identificano le aree di funzionalità supportate e richieste da un componente software, viene utilizzata una voce del registro di sistema per ogni categoria o area di funzionalità identificata. Ogni categoria di componenti è identificata da un identificatore univoco globale (GUID). quando un controllo viene installato, viene registrato come controllo nel registro di sistema usando l'ID di categoria del componente per il controllo, vedere [registrazione automatica per i controlli](self-registration-for-controls.md). All'interno dei controlli registrazione automatica verranno registrate anche le categorie di componenti implementate e le categorie di componenti necessarie per il supporto di un contenitore per ospitare correttamente il controllo.

Quando un contenitore di controlli offre controlli all'utente da inserire, consente solo all'utente di selezionare e creare un'istanza dei controlli che saranno in grado di funzionare in modo adeguato in tale ambiente. Se, ad esempio, il contenitore di controlli non supporta l'associazione dati, il contenitore non consentirà all'utente di selezionare e creare un'istanza dei controlli che hanno una voce nel registro di sistema per indicare che richiedono la categoria del componente DataBinding. È disponibile una finestra di dialogo comune per l'inserimento di controlli e le API per gestire le voci del registro di sistema.

Le categorie di componenti non sono cumulative o esclusive, un controllo può richiedere qualsiasi combinazione di categorie di componenti per funzionare. È possibile che un controllo senza voci obbligatorie per le categorie di componenti sia in grado di funzionare in qualsiasi contenitore di controlli e che non richieda una funzionalità specifica di un contenitore di controlli per funzionare.

Le categorie di componenti seguenti sono indicate qui, in cui è possibile che siano disponibili specifiche più dettagliate delle categorie.

-   Contenimento del controllo [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) .
-   DataBinding semplice tramite l'interfaccia [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) .
-   Associazione dati avanzata (supportata dalle interfacce di associazione dati aggiuntive di VB 4.0).
-   Interfacce private Visual Basic- [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat), [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)
-   Controlli compatibili con Internet.
-   Controlli privi di finestra.

Non si tratta di un elenco di categorie definitivo. è probabile che altre categorie vengano definite in futuro quando vengono identificati nuovi requisiti. Un elenco aggiornato delle categorie di componenti è disponibile da Microsoft; in questo elenco sono riportate le categorie di componenti identificate da Microsoft e tutte le altre che hanno informato Microsoft.

È importante ricordare che i controlli devono provare a lavorare nel maggior numero possibile di ambienti. Se possibile, il controllo dovrebbe peggiorare la funzionalità quando viene inserito in un contenitore che non supporta determinate interfacce. Lo scopo delle categorie di componenti è impedire una situazione in cui il controllo viene inserito in un ambiente non idoneo e il controllo non è in grado di raggiungere l'attività desiderata. In genere, un controllo dovrebbe peggiorare correttamente quando le interfacce non sono presenti, un controllo può scegliere di consigliare all'utente una finestra di messaggio che alcune funzionalità non sono disponibili o documentare chiaramente la funzionalità richiesta da un contenitore di controlli per ottenere prestazioni ottimali.

Si noti che i controlli e i contenitori precedenti non usano le categorie di componenti e si basano invece sulla parola chiave del controllo presente sul controllo nel registro di sistema. Per essere riconosciuti dai controlli dei contenitori meno recenti può voler registrare la parola chiave Control nel registro di sistema, gli sviluppatori di controlli devono verificare che il controllo possa essere ospitato correttamente in questi contenitori prima di eseguire questa operazione. I contenitori che usano le categorie di componenti possono usarli correttamente per ospitare i controlli precedenti perché la DLL di categoria Components gestisce il mapping, esiste una categoria separata per i controlli precedenti CATId ControlV1, in \_ modo che un contenitore possa eventualmente escluderli se necessario.

Poiché le categorie di componenti sono identificate da GUID, è possibile che i contenitori che offrono una particolare funzionalità specifica abbiano ID di categoria personalizzati, generati usando uno strumento di generazione GUID. Questo può tuttavia compromettere il vantaggio dell'interoperabilità dei controlli e dei contenitori, in modo che sia preferibile che, laddove possibile, vengano utilizzate le categorie di componenti esistenti. I fornitori sono invitati a consultare insieme quando definiscono nuove categorie di componenti per assicurarsi che soddisfino i requisiti comuni del Marketplace e seguano lo spirito di interoperabilità dei controlli ActiveX.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

 




