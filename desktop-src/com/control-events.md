---
title: Eventi di controllo (COM)
description: Oltre a fornire proprietà e metodi, un controllo fornisce anche interfacce in uscita per notificare al client gli eventi.
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b987202cb4e4e635a947ed60e9f947cc428f0aaaacb3d27c27d60ad536b636
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119243631"
---
# <a name="control-events-com"></a>Eventi di controllo (COM)

Oltre a fornire proprietà e metodi, un controllo fornisce anche interfacce in uscita per notificare al client gli eventi. Il client deve supportare la gestione di questi eventi. Per [altre informazioni sul funzionamento degli oggetti collegabili,](events-in-com-and-connectable-objects.md) vedere Eventi in COM e oggetti collegabili.

Un controllo può supportare diverse interfacce in uscita per scopi diversi. Tutte le interfacce in uscita sono contrassegnate come interfacce di origine nelle informazioni sul tipo del controllo, ma solo una è contrassegnata come predefinita per indicare che è l'interfaccia in uscita primaria.

Un contenitore può supportare una o più interfacce in uscita definite da un controllo . Il controllo deve essere preparato per gestire i contenitori che forniscono solo il supporto per alcune delle interfacce in uscita.

I controlli supportano quattro tipi di eventi:

-   Richiedere eventi. Un controllo richiede l'autorizzazione al client per eseguire un'operazione chiamando un metodo nell'interfaccia in uscita, attivando così un evento di richiesta. Il client segnala il controllo tramite un parametro booleano out nel metodo chiamato dal controllo. Il client può quindi impedire al controllo di eseguire l'azione.
-   Prima degli eventi. Un controllo notifica al proprio client che sta per eseguire un'operazione chiamando un metodo nell'interfaccia in uscita, attivando così un evento before. Il client non ha la possibilità di impedire l'azione, ma può eseguire tutti i passaggi necessari in base all'azione che sta per verificarsi.
-   Dopo gli eventi. Un controllo notifica al client che ha appena eseguito un'operazione chiamando un metodo nell'interfaccia in uscita, attivando così un evento after. Anche in questo caso, il client non può annullare questa azione, ma può eseguire i passaggi necessari in base all'azione che si è verificata.
-   Eseguire eventi. Un controllo attiva un evento do per consentire al client di eseguire l'override dell'azione del controllo e fornire azioni alternative o supplementari. In genere, il metodo che un controllo chiama per un evento do ha diversi parametri per negoziare con il client le azioni che si verificheranno.

I dispid seguenti sono definiti per gli eventi standard che i controlli possono supportare: Click, DblClick, KeyDown, KeyPress, KeyUp, MouseMove, MouseUp ed Error. Tutti questi eventi standard hanno valori DISPID negativi, che ne indicano lo stato standard.

Il [**metodo IOleControl::FreezeEvents,**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) quando viene chiamato con **TRUE,** indica a un controllo se il contenitore non gestirà gli eventi dal controllo fino a quando non viene chiamato nuovamente **FreezeEvents** con **FALSE**. Durante questo periodo di tempo il controllo non può dipendere dal contenitore che gestisce effettivamente gli eventi. Se un evento deve essere gestito, il controllo deve accodare l'evento per generarlo quando **FreezeEvents** viene chiamato con **FALSE.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ActiveX Controlli](activex-controls.md)
</dt> </dl>

 

 




