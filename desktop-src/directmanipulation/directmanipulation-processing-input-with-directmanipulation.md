---
description: In questa sezione viene fornita una panoramica del modello di threading con manipolazione diretta, della modalità di elaborazione dei messaggi della finestra tramite manipolazione diretta e del modo in cui viene modificato lo stato di un viewport quando viene eseguito il mapping dell'input ai movimenti di output.
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: Elaborazione dell'input con DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 284a0a1866a2082e2c34c65de347b0dcdfab3a64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303940"
---
# <a name="processing-input-with-directmanipulation"></a>Elaborazione dell'input con DirectManipulation

In questa sezione viene fornita una panoramica del modello di threading con [manipolazione diretta](direct-manipulation-portal.md) , della modalità di elaborazione dei messaggi della finestra tramite manipolazione diretta e del modo in cui viene modificato lo stato di un viewport quando viene eseguito il mapping dell'input ai movimenti di output.

- [Flusso di input](#input-flow)
- [Osservazioni:](#remarks)

La [manipolazione diretta](direct-manipulation-portal.md) usa due thread per coordinare le operazioni asincrone:

*Thread UI* : il thread proprietario dell'elemento **HWND** associato all'input. Questo thread è proprietario dell'inizializzazione della [manipolazione diretta](direct-manipulation-portal.md). L'elaborazione dell'input da tastiera e mouse si verifica anche sul thread dell'interfaccia utente.

*Thread delegato* : thread creato e di proprietà della [manipolazione diretta](direct-manipulation-portal.md). L'elaborazione dell'input tocco viene eseguita nel thread delegato.

## <a name="input-flow"></a>Flusso di input

In una configurazione tipica in cui l'hit testing viene eseguito sul thread dell'interfaccia utente, i messaggi della finestra vengono elaborati tramite [manipolazione diretta](direct-manipulation-portal.md) nell'ordine seguente:

![diagramma che illustra l'ordine in cui vengono elaborati i messaggi.](images/inputprocessing.png)

Per un viewport inattivo:

1. Una serie di messaggi finestra raggiunge il thread delegato.
2. [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) i messaggi vengono inviati dal thread delegato al thread di hit test indipendente (IHT).
3. Se il metodo [**secontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) viene chiamato dal thread IHT, i messaggi potrebbero essere inviati al thread dell'interfaccia utente dal thread delegato, a seconda del valore [**del \_ \_ tipo di DIRECTMANIPULATION HITTEST**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type) quando è stato chiamato [**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget) .
4. Se [**secontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) non viene chiamato dal thread IHT, i messaggi vengono sempre inviati dal thread delegato al thread dell'interfaccia utente.
5. Il client può chiamare [**secontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) dal thread UI per consentire alla [manipolazione diretta](direct-manipulation-portal.md) di rilevare una manipolazione.
6. Se viene rilevata una manipolazione, la [manipolazione diretta](direct-manipulation-portal.md) Invia un messaggio [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) per notificare al client che l'input è gestito da manipolazione diretta. Lo stato del viewport è impostato su **in esecuzione** e la trasformazione di output verrà aggiornata.
7. Se viene rilevata un'interazione diversa da una manipolazione, la [manipolazione diretta](direct-manipulation-portal.md) invia messaggi rimanenti al thread dell'interfaccia utente.

Per un viewport in movimento (con stato in esecuzione o inerzia), il messaggio di finestra raggiunge prima il thread del delegato, in cui l'hit test della [manipolazione diretta](direct-manipulation-portal.md) viene eseguito su tutti i viewport in esecuzione. La manipolazione diretta assegna automaticamente il contatto ai viewport appropriati identificati dall'hit testing. Lo stato del viewport è in esecuzione e la trasformazione di output verrà aggiornata.

In alcuni casi, un thread dell'interfaccia utente dell'applicazione può essere troppo lento per rispondere all'hit testing. È possibile usare un thread di hit test ([**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)) per consentire al client di spostare i messaggi [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) in un thread specifico per consentire l'hit testing.

## <a name="remarks"></a>Commenti

In genere, la [manipolazione diretta](direct-manipulation-portal.md) invia al thread dell'interfaccia utente solo i messaggi [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) , trattenendo i messaggi successivi in attesa di una risposta dal client. Se il client chiama [**secontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact), gli unici messaggi ricevuti dal thread UI quando viene rilevata una manipolazione sono [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md)e il [messaggio WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md).

È possibile che il client [**non chiami il**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) callback durante l'elaborazione di messaggi [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) . In questo caso, la [manipolazione diretta](direct-manipulation-portal.md) Invia tutti i messaggi al thread dell'interfaccia utente senza analizzare i messaggi per verificare se è presente una manipolazione. Il client può quindi scegliere qualsiasi punto per chiamare il **secontatto** e fare in modo che la manipolazione diretta inizi a rilevare le manipolazioni e inviare messaggi di [messaggio WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) quando ne viene rilevata una.

**Windows 10 e versioni successive:** È possibile decidere quali manipolazioni si desidera gestire chiamando [**DeferContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact) prima di chiamare il [**secontatto**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) in un messaggio [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) o [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) . **DeferContact** garantisce che tutti i messaggi successivi vengano inviati al thread dell'interfaccia utente per il periodo di tempo specificato.
