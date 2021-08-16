---
description: Di seguito sono elencati i requisiti generali per l'implementazione del terminale collegabile.
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: Implementazione di terminali collegabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a75dd7b085377c8474c9a89d74a297c3ca66c6740c01c7428e7b6f250e16c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762903"
---
# <a name="implementing-pluggable-terminals"></a>Implementazione di terminali collegabili

I requisiti generali per l'implementazione del terminale collegabile sono:

-   Il codice di streaming sottostante di un terminale collegabile deve corrispondere alle funzionalità degli MSP desiderati.
-   Il terminale deve usare DirectShow per funzionare con la maggior parte dei msp (si presuppone che da qui in avanti).
-   I terminali audio devono supportare PCM mono lineare a 8 kHz a 16 bit per la maggior parte dei PCP.
-   Il terminale deve abilitare il marshalling a thread libero implementando [**IMarshal.**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) Il terminale può eseguire questa operazione chiamando l'API COM [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) e aggregando **IMarshal** al puntatore restituito. Il distruttore dell'oggetto terminale deve chiamare [**IMarshal->Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
-   Il terminale deve implementare o aggregare eventuali interfacce aggiuntive specifiche del terminale appropriate.
-   L'implementazione del terminale deve essere thread-safe.
-   L'implementazione \# del terminale deve includere Termmgr.h per la definizione di [**ITTerminalControl.**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) Oltre alle consuete librerie include e , necessarie per le applicazioni TAPI 3 o TAPI 3 in Windows 2000 SP1.

Note sull'implementazione di interfacce e metodi:

Il terminale deve [**implementare ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (dual interface-vtable + [**IDispatch).**](/windows/win32/api/oaidl/nn-oaidl-idispatch)

[**ITTerminal::get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

Il terminale deve restituire **una rappresentazione BSTR** di un GUID selezionato che identifica il tipo di terminale. Allocare **BSTR** tramite [**SysAllocString.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) Per eseguire la conversione da GUID a **BSTR,** [**chiamare StringFromCLSID,**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) **SysAllocString** e [**CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

[**ITTerminal::get \_ TerminalType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

Il terminale deve in genere restituire TT \_ DYNAMIC se un'applicazione implementa il terminale. Anche la restituzione di TT STATIC funzionerà e la restituzione di questo valore potrebbe essere appropriata se il terminale corrisponde a un dispositivo hardware. Tuttavia, questa operazione potrebbe confondere gli utenti perché un terminale statico non sarà presente nell'enumerazione del terminale statico del \_ msp.

[**ITTerminal::get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

Se l'implementazione del terminale non limita arbitrariamente il numero di flussi a cui il terminale può essere connesso contemporaneamente, il terminale deve sempre restituire \_ TS NOTINUSE.

In caso contrario, l'implementazione del terminale limita arbitrariamente il numero di flussi a cui il terminale può essere connesso alla volta. In questo caso, il terminale deve mantenere un conteggio del numero di flussi a cui è connesso. Il terminale deve incrementare questo conteggio interno su una chiamata [**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) riuscita e decrementarlo in caso di esito positivo di una chiamata [**ITTerminalControl::D isconnectTerminal.**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) In [**ITTerminal::get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)deve restituire TS INUSE se questo conteggio è uguale al numero massimo di flussi su cui è possibile selezionare il terminale alla volta. In caso contrario, deve restituire \_ TS \_ NOTINUSE. Si noti che se il limite è uno, il conteggio può essere semplicemente un valore booleano o TERMINAL \_ STATE.

[**ITTerminal::get \_ Name**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

Il terminale deve restituire un **nome BSTR** a scelta, allocato tramite [**SysAllocString.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) Questo nome deve essere significativo per l'utente e deve essere localizzato.

[**ITTerminal::get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

Il terminale deve restituire il tipo di supporto, TAPIMEDIATYPE \_ AUDIO o TAPIMEDIATYPE \_ VIDEO.

[**ITTerminal::get \_ Direction**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

Il terminale restituisce il \_ valore di enumerazione TERMINAL DIRECTION che indica la direzione del terminale. Se il terminale è bidirezionale (ad esempio, un bridge), deve restituire TD \_ BIDIRECTIONAL.

Il terminale deve [**implementare ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (solo vtable).

[**ITTerminalControl::get \_ AddressHandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

Un terminale fornito dall'applicazione deve sempre restituire **NULL** come handle di indirizzo. Ciò indica al msp che il terminale non è stato creato in un oggetto indirizzo MSP specifico.

[**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

In questa chiamata, il terminale aggiungerà i relativi filtri al grafico specificato e li connetterà tra loro, se applicabile. Il terminale restituirà quindi i segnaposto esposti dal terminale per la direzione del flusso specificata.

Un terminale che non supporta la connessione simultanea a più flussi imposta una variabile interna su TS INUSE al completamento \_ corretto di questo metodo.

Il terminale può usare *il parametro dwTerminalDirection* da questa chiamata per determinare la direzione del flusso a cui è connesso. Questa operazione è necessaria per i terminali bidirezionali.

> [!Note]  
> In genere (nelle classi di base MSP e in tutti i msp noti), il codice del flusso MSP non riuscirà a stabilire la connessione se il terminale restituisce più di un pin da una singola [**chiamata ConnectTerminal.**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) Ciò è corretto, perché un terminale che restituisce più pin durante la connessione richiede che il msp abbia una conoscenza speciale del terminale per usare in modo efficace i pin aggiuntivi.

 

[**ITTerminalControl::CompleteConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

Il terminale dovrebbe restituire solo S \_ OK. Il terminale può anche eseguire l'inizializzazione post-connessione, se necessario.

[**ITTerminalControl::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

Il terminale deve eseguire qualsiasi operazione necessaria per disconnettere il terminale dal resto del grafico. In genere ciò comporta la rimozione di tutti i filtri dei terminali dal grafico e l'impostazione dello stato del terminale su TS \_ NOTINUSE.

[**ITTerminalControl::RunRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

Il terminale dovrebbe restituire solo E \_ NOTIMPL.

[**ITTerminalControl::StopRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

Il terminale dovrebbe restituire solo E \_ NOTIMPL.

 

 
