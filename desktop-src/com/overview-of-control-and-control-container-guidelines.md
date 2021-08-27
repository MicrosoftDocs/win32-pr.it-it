---
title: Panoramica delle linee guida per i contenitori di controlli e controlli
description: Panoramica delle linee guida per i contenitori di controlli e controlli
ms.assetid: c4cf2409-0085-43e6-afa2-f9c03cc50565
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2658c691e13b0a78da82fa006ed22142082e2f7eb8b04d78992943a024487a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120461"
---
# <a name="overview-of-control-and-control-container-guidelines"></a>Panoramica delle linee guida per i contenitori di controlli e controlli

Un ActiveX è essenzialmente un semplice oggetto OLE che supporta [**l'interfaccia IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) In genere supporterà più interfacce per offrire funzionalità, ma tutte le interfacce aggiuntive possono essere visualizzate come facoltative e, di conseguenza, un contenitore di controlli non deve basarsi sulle interfacce aggiuntive supportate. Se non si specificano interfacce aggiuntive che un controllo deve supportare, un controllo può avere come destinazione in modo efficiente una particolare area di funzionalità senza dover supportare interfacce specifiche per qualificarsi come controllo. Come sempre con OLE, sia in un controllo che in un contenitore di controlli, non si deve mai presunzioni che un'interfaccia sia disponibile e che siano sempre seguite le convenzioni standard di controllo dei valori restituiti. È importante che un controllo o un contenitore di controlli si degradi correttamente e offrire funzionalità alternative se non è disponibile un'interfaccia necessaria.

Un ActiveX contenitore di controlli deve essere in grado di ospitare un controllo ActiveX controllo. supporterà anche una serie di interfacce aggiuntive, come specificato in [Contenitori](containers.md). Esistono diverse interfacce e metodi che un contenitore può facoltativamente supportare, raggruppati in aree funzionali note come *categorie di componenti.* Un contenitore può supportare qualsiasi combinazione di categorie di componenti, ad esempio una categoria di componenti esiste per il data binding e un contenitore può o meno supportare la funzionalità di data binding, a seconda delle esigenze di mercato del contenitore. Se un controllo richiede il supporto dell'associazione dati da un contenitore per funzionare, immette questo requisito nel registro. In questo modo un contenitore di controlli può offrire solo i controlli che può ospitare correttamente. È importante notare che le categorie di componenti vengono specificate come parte di OLE e non sono specifiche dei controlli ActiveX. L'architettura dei controlli usa le categorie di componenti per identificare le aree di funzionalità che un componente OLE può supportare. Le categorie di componenti non sono cumulative o esclusive, quindi un contenitore di controlli può supportare una categoria senza necessariamente supportarne un'altra.

È importante che i controlli che richiedono funzionalità facoltative o funzionalità specifiche di un determinato contenitore siano chiaramente in pacchetto e in commercio con tali requisiti. Allo stesso modo, i contenitori che offrono determinate funzionalità o categorie di componenti devono essere offerti e in pacchetto per offrire tali livelli di supporto durante l'hosting di ActiveX personalizzati. È consigliabile che i controlli siano di destinazione e di test con il maggior numero possibile di contenitori e si degradino normalmente per offrire funzionalità meno o alternative se non sono disponibili interfacce o metodi. In una situazione in cui un controllo non può eseguire la funzione del processo designata senza il supporto di una categoria di componenti, tale categoria deve essere immessa come requisito nel Registro di sistema per impedire l'inserimento del controllo in un contenitore non appropriato.

Queste linee guida definiscono le interfacce e i metodi che un controllo può aspettarsi che un contenitore di controlli supporti, anche se come sempre un controllo deve controllare i valori restituiti quando si usa [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) o altri metodi per ottenere puntatori a queste interfacce. Un contenitore non deve aspettarsi che un controllo supporti qualcosa di più dell'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e queste linee guida identificano le interfacce che un controllo può supportare e il significato della presenza di una determinata interfaccia.

## <a name="why-the-activex-control-and-control-container-guidelines-are-important"></a>Perché le linee guida ActiveX controllo e contenitore di controlli sono importanti

ActiveX I controlli sono diventati l'architettura principale per lo sviluppo di componenti software programmabili da usare in un'ampia gamma di contenitori diversi, dagli strumenti di sviluppo software agli strumenti di produttività degli utenti finali. Per un corretto funzionamento di un controllo in un'ampia gamma di contenitori, il controllo deve essere in grado di presupporre un livello minimo di funzionalità su cui può basarsi in tutti i contenitori.

Seguendo queste linee guida, gli sviluppatori di controlli e contenitori rendono i controlli e i contenitori più affidabili e interoperativi e, in ultima analisi, componenti migliori e più utilizzabili per la creazione di soluzioni basate su componenti.

## <a name="what-to-do-when-an-interface-you-need-is-not-available"></a>Cosa fare quando un'interfaccia necessaria non è disponibile

I programmi OLE devono usare [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per acquisire puntatori a interfaccia e devono controllare il valore restituito. Le applicazioni OLE non possono presupporre che **QueryInterface avrà** esito positivo.

Questo requisito si applica a tutte le applicazioni OLE. Se l'interfaccia richiesta non è disponibile,ovvero [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) restituisce E NOINTERFACE, il controllo o il contenitore deve peggiorare normalmente, anche se ciò significa che non può eseguire la funzione del processo \_ designata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ActiveX Linee guida per i contenitori di controlli e controlli](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




