---
description: Questa sezione offre una panoramica del modello di threading Manipolazione diretta, del modo in cui i messaggi della finestra vengono elaborati dalla manipolazione diretta e del modo in cui lo stato di un viewport cambia quando l'input viene mappato ai movimenti di output.
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: Elaborazione dell'input con DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 49b72f88da8978192af402c8b810655c102395d5aad273f34340ed57e2703008
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094656"
---
# <a name="processing-input-with-directmanipulation"></a>Elaborazione dell'input con DirectManipulation

Questa sezione offre una panoramica del modello di [threading](direct-manipulation-portal.md) Manipolazione diretta, del modo in cui i messaggi della finestra vengono elaborati dalla manipolazione diretta e del modo in cui lo stato di un viewport cambia quando l'input viene mappato ai movimenti di output.

- [Flusso di input](#input-flow)
- [Osservazioni:](#remarks)

[La manipolazione diretta](direct-manipulation-portal.md) usa due thread per coordinare le operazioni asincrone:

*Thread dell'interfaccia* utente: thread proprietario **dell'oggetto HWND** associato all'input. Questo thread è proprietario dell'inizializzazione [della manipolazione diretta.](direct-manipulation-portal.md) L'elaborazione dell'input tramite mouse e tastiera viene eseguita anche nel thread dell'interfaccia utente.

*Thread delegato:* il thread creato e di proprietà di [Direct Manipulation.](direct-manipulation-portal.md) L'elaborazione dell'input tocco viene eseguita nel thread delegato.

## <a name="input-flow"></a>Flusso di input

In una configurazione tipica in cui l'hit testing viene [](direct-manipulation-portal.md) eseguito sul thread dell'interfaccia utente, i messaggi della finestra vengono elaborati dalla manipolazione diretta nell'ordine seguente:

![Diagramma che illustra l'ordine di elaborazione dei messaggi.](images/inputprocessing.png)

Per un viewport in stato di inquieto:

1. Una serie di messaggi finestra raggiunge il thread delegato.
2. [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) messaggi vengono inviati dal thread delegato al thread IHT (Independent Hit Test).
3. Se [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) viene chiamato dal thread IHT, i messaggi potrebbero essere inviati al thread dell'interfaccia utente dal thread delegato, a seconda del valore di [**DIRECTMANIPULATION \_ HITTEST \_ TYPE**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type) quando è stato chiamato [**RegisterHitTestTarget.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)
4. Se [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) non viene chiamato dal thread IHT, i messaggi vengono sempre inviati dal thread delegato al thread dell'interfaccia utente.
5. Il client può chiamare [**SetContact dal**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) thread dell'interfaccia utente per consentire alla [manipolazione diretta di](direct-manipulation-portal.md) rilevare una manipolazione.
6. Se viene rilevata una manipolazione, [la](direct-manipulation-portal.md) manipolazione diretta invia un messaggio [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) per notificare al client che l'input viene gestito dalla manipolazione diretta. Lo stato del viewport è impostato su **RUNNING e** la trasformazione di output verrà aggiornata.
7. Se viene rilevata un'interazione diversa da una manipolazione, [la manipolazione](direct-manipulation-portal.md) diretta invia i messaggi rimanenti al thread dell'interfaccia utente.

Per un viewport in movimento (con stato RUNNING o INERTIA), il messaggio della finestra raggiunge prima il thread delegato, dove [la](direct-manipulation-portal.md) manipolazione diretta esegue l'hit test su tutti i viewport in esecuzione. La manipolazione diretta assegna automaticamente il contatto ai viewport appropriati identificati dall'hit testing. Lo stato del viewport è RUNNING e la trasformazione di output verrà aggiornata.

In alcuni casi, un thread dell'interfaccia utente dell'applicazione potrebbe essere troppo lento per rispondere all'hit testing. È possibile usare un thread di hit test ([**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)) per consentire al client di spostare i messaggi [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST in](../inputmsg/dm-pointerhittest.md) un thread specifico per consentire l'hit testing.

## <a name="remarks"></a>Commenti

In genere, [la](direct-manipulation-portal.md) manipolazione diretta invia solo messaggi [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) al thread dell'interfaccia utente, mantenendo i messaggi successivi in attesa di una risposta dal client. Se il client chiama [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact), gli unici messaggi che il thread dell'interfaccia utente riceve quando viene rilevata una manipolazione sono [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md)e [WM/_POINTERCAPTURECHANGED messaggio](../inputmsg/wm-pointercapturechanged.md).

Il client potrebbe non chiamare [**SetContact durante**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) l'elaborazione di [messaggi WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) [e DM/_POINTERHITTEST.](../inputmsg/dm-pointerhittest.md) In questo caso, [la manipolazione](direct-manipulation-portal.md) diretta invia tutti i messaggi al thread dell'interfaccia utente senza analizzare i messaggi per verificare se è presente una manipolazione. Il client può quindi scegliere qualsiasi punto per chiamare **SetContact** e fare in modo che la manipolazione diretta inizi a rilevare le modifiche e inviare messaggi di messaggio [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) quando ne viene rilevata una.

**Windows 10 e versioni successive:** Puoi decidere quali modifiche vuoi gestire chiamando [**DeferContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact) prima di chiamare [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) in un messaggio [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) o [DM/_POINTERHITTEST.](../inputmsg/dm-pointerhittest.md) **DeferContact garantisce** che tutti i messaggi successivi vengono inviati al thread dell'interfaccia utente per il periodo di tempo specificato.
