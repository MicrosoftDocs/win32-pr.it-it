---
title: Panoramica delle linee guida per il controllo e il controllo del contenitore
description: Panoramica delle linee guida per il controllo e il controllo del contenitore
ms.assetid: c4cf2409-0085-43e6-afa2-f9c03cc50565
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd72851775898f4fd140c7d101d72993c34e3eb
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103720047"
---
# <a name="overview-of-control-and-control-container-guidelines"></a>Panoramica delle linee guida per il controllo e il controllo del contenitore

Un controllo ActiveX è essenzialmente un semplice oggetto OLE che supporta l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . In genere supporta più interfacce per offrire funzionalità, ma tutte le interfacce aggiuntive possono essere visualizzate come facoltative e, di conseguenza, un contenitore di controlli non deve basarsi su interfacce aggiuntive supportate. Se non si specificano interfacce aggiuntive che un controllo deve supportare, un controllo può essere utilizzato in modo efficiente per una particolare area di funzionalità senza dover supportare interfacce specifiche per qualificarsi come controllo. Come sempre con OLE, sia che si tratti di un controllo o di un contenitore di controlli, non si deve mai presupporre che un'interfaccia sia disponibile e che le convenzioni standard di controllo restituito debbano sempre essere seguite. È importante che un contenitore di controlli o controlli si riduca normalmente e offra funzionalità alternative se non è disponibile un'interfaccia richiesta.

Un contenitore di controlli ActiveX deve essere in grado di ospitare un controllo ActiveX minimo; supporta inoltre una serie di interfacce aggiuntive, come specificato nei [contenitori](containers.md). Sono disponibili diverse interfacce e metodi che possono essere facoltativamente supportati da un contenitore, raggruppati in aree funzionali note come categorie di *componenti*. Un contenitore può supportare qualsiasi combinazione di categorie di componenti, ad esempio, esiste una categoria di componenti per l'associazione dati e un contenitore può supportare o meno la funzionalità di associazione dati, a seconda delle esigenze di mercato del contenitore. Se per il funzionamento di un controllo è necessario il supporto dell'associazione dati da un contenitore, questo requisito verrà inserito nel registro di sistema. Questo consente a un contenitore di controlli di offrire solo per l'inserimento dei controlli che sa che può ospitare correttamente. È importante notare che le categorie di componenti vengono specificate come parte di OLE e non sono specifiche dei controlli ActiveX, l'architettura dei controlli utilizza le categorie di componenti per identificare le aree di funzionalità che possono essere supportate da un componente OLE. Le categorie di componenti non sono cumulative o esclusive, pertanto un contenitore di controlli può supportare una categoria senza necessariamente supportare un'altra categoria.

È importante per i controlli che richiedono funzionalità facoltative o funzionalità specifiche di un determinato contenitore per essere chiaramente impacchettate e commercializzate con tali requisiti. Analogamente, i contenitori che offrono determinate funzionalità o categorie di componenti devono essere commercializzati e assemblati in modo da offrire i livelli di supporto per l'hosting di controlli ActiveX. Si consiglia di controllare la destinazione e il test con il maggior numero di contenitori possibile e degradare normalmente per offrire funzionalità meno o alternative se le interfacce o i metodi non sono disponibili. In una situazione in cui un controllo non è in grado di eseguire la funzione di processo designata senza il supporto di una categoria di componenti, tale categoria deve essere immessa come requisito nel registro di sistema per impedire l'inserimento del controllo in un contenitore non appropriato.

Queste linee guida definiscono le interfacce e i metodi che un controllo può prevedere di supportare da un contenitore di controllo, anche se sempre un controllo deve controllare i valori restituiti quando si usa [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) o altri metodi per ottenere i puntatori a tali interfacce. Un contenitore non dovrebbe prevedere che un controllo supporti più di quanto l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e queste linee guida identificano le interfacce che un controllo può supportare e il significato della presenza di una particolare interfaccia.

## <a name="why-the-activex-control-and-control-container-guidelines-are-important"></a>Motivi per cui le linee guida per il controllo ActiveX e il controllo del contenitore sono importanti

I controlli ActiveX sono diventati l'architettura principale per lo sviluppo di componenti software programmabili da usare in diversi contenitori, da strumenti di sviluppo software agli strumenti per la produttività degli utenti finali. Affinché un controllo funzioni correttamente in un'ampia gamma di contenitori, il controllo deve essere in grado di assumere un livello minimo di funzionalità su cui può basarsi in tutti i contenitori.

Seguendo queste linee guida, gli sviluppatori di controlli e contenitori rendono i controlli e i contenitori più affidabili e interoperativi e, infine, componenti migliori e più utilizzabili per la creazione di soluzioni basate su componenti.

## <a name="what-to-do-when-an-interface-you-need-is-not-available"></a>Cosa fare quando un'interfaccia necessaria non è disponibile

I programmi OLE devono usare [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per acquisire i puntatori di interfaccia ed è necessario controllare il valore restituito. Le applicazioni OLE non possono presupporre in modo sicuro che **QueryInterface** avrà esito positivo.

Questo requisito si applica a tutte le applicazioni OLE. Se l'interfaccia richiesta non è disponibile (ovvero, [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) restituisce E \_ nointerface), il controllo o il contenitore deve peggiorare normalmente, anche se ciò significa che non è in grado di eseguire la funzione di processo designata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida per il controllo ActiveX e il controllo del contenitore](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




