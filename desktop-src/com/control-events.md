---
title: Eventi di controllo (COM)
description: Oltre a fornire proprietà e metodi, un controllo fornisce anche interfacce in uscita per notificare al client gli eventi.
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1833e1396847e09366d1e06193196cfcf981d330
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047715"
---
# <a name="control-events-com"></a>Eventi di controllo (COM)

Oltre a fornire proprietà e metodi, un controllo fornisce anche interfacce in uscita per notificare al client gli eventi. Il client deve supportare la gestione di questi eventi. Per ulteriori informazioni sul funzionamento degli oggetti collegabili, vedere [eventi in com e oggetti collegabili](events-in-com-and-connectable-objects.md) .

Un controllo può supportare diverse interfacce in uscita per scopi diversi. Tutte le interfacce in uscita sono contrassegnate come interfacce di origine nelle informazioni sul tipo del controllo, ma solo una è contrassegnata come predefinita per indicare che si tratta dell'interfaccia in uscita primaria.

Un contenitore può supportare una o più interfacce in uscita definite da un controllo. Il controllo deve essere preparato per gestire i contenitori che forniscono solo il supporto per alcune delle interfacce in uscita.

I controlli supportano quattro tipi di eventi:

-   Eventi della richiesta. Un controllo richiede l'autorizzazione da parte del client per eseguire un'operazione chiamando un metodo nell'interfaccia in uscita, attivando in tal modo un evento di richiesta. Il client segnala il controllo tramite un valore booleano out-parameter nel metodo chiamato dal controllo. Il client può quindi impedire che il controllo esegua l'azione.
-   Prima degli eventi. Un controllo Invia una notifica al cappello client per eseguire un'operazione chiamando un metodo nell'interfaccia in uscita, attivando così un evento Before. Il client non ha la possibilità di impedire l'azione, ma può eseguire tutti i passaggi necessari in base all'azione che sta per verificarsi.
-   Dopo gli eventi. Un controllo Invia una notifica al client che ha appena fatto qualcosa chiamando un metodo nell'interfaccia in uscita, attivando quindi un evento After. Anche in questo caso, il client non è in grado di annullare questa azione, ma è possibile eseguire le operazioni necessarie in base all'azione eseguita.
-   Eseguire eventi. Un controllo attiva un evento do per consentire al client di eseguire l'override dell'azione del controllo e fornire alcune azioni alternative o supplementari. In genere, il metodo che un controllo chiama per un evento do presenta diversi parametri per negoziare con il client sulle azioni che si verificheranno.

I DISPID seguenti sono definiti per gli eventi standard che i controlli possono supportare: click, DblClick, KeyDown, KeyPress, KeyUp, MouseMove, MouseUp ed Error. Tutti questi eventi standard hanno valori DISPID negativi, che ne indicano lo stato standard.

Il metodo [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) , quando viene chiamato con **true**, indica a un controllo se il contenitore infastidisce la gestione degli eventi dal controllo fino a quando **FreezeEvents** viene chiamato nuovamente con **false**. Durante questo periodo di tempo, il controllo non può dipendere dal contenitore che gestisce effettivamente gli eventi. Se è necessario gestire un evento, il controllo deve accodare l'evento per attivarlo quando **FreezeEvents** viene chiamato con **false**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli ActiveX](activex-controls.md)
</dt> </dl>

 

 




