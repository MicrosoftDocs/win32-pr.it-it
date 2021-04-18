---
description: Di seguito sono elencati i requisiti generali per l'implementazione del terminale collegabile.
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: Implementazione di terminali collegabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 494b2f6bc5ccb214bc7101f570a4db3037fd8cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313258"
---
# <a name="implementing-pluggable-terminals"></a>Implementazione di terminali collegabili

I requisiti generali per l'implementazione del terminale modulare sono:

-   Il codice di streaming sottostante di un terminale collegabile deve corrispondere alle funzionalità del MSPs desiderato.
-   Il terminale deve usare i filtri DirectShow per lavorare con la maggior parte dei MSPs (questa operazione si presuppone da qui in poi).
-   Per la maggior parte dei MSPs, i terminali audio devono supportare un PCM lineare mono da 8 kHz a 16 bit.
-   Il terminale deve abilitare il marshalling a thread libero mediante l'implementazione di [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). Il terminale può eseguire questa operazione chiamando l'API COM [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) e aggregando **IMarshal** al puntatore restituito. Il distruttore dell'oggetto terminale deve chiamare [**IMarshal->versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).
-   Il terminale deve implementare o aggregare eventuali interfacce aggiuntive specifiche del terminale appropriate.
-   L'implementazione del terminale deve essere thread-safe.
-   L'implementazione del terminale deve \# includere termmgr. h per la definizione di [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol). Si tratta di un'aggiunta alle librerie usuali e alle librerie necessarie per le applicazioni TAPI 3 o TAPI 3 in Windows 2000 SP1.

Note sull'implementazione del metodo e dell'interfaccia:

Il terminale deve implementare [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (Dual Interface-vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)).

[**ITTerminal:: Get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

Il terminale deve restituire una rappresentazione **BSTR** di un GUID selezionato che identifica il tipo di terminale. Allocare **BSTR** tramite [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring). Per eseguire la conversione da GUID a **BSTR**, chiamare [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid), **SysAllocString** e [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

[**ITTerminal:: Get \_ TerminalType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

Il terminale dovrebbe in genere restituire \_ la dinamica TT se un'applicazione implementa il terminale. Il ripristino \_ della staticità TT funziona anche e la restituzione di questo valore può essere appropriata se il terminale corrisponde a un dispositivo hardware. Tuttavia, questa operazione può generare confusione per gli utenti perché un terminale statico non sarà presente nell'enumerazione del terminale statico di msp.

[**Stato ITTerminal:: Get \_**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

Se l'implementazione del terminale non limita arbitrariamente il numero di flussi a cui il terminale può essere connesso contemporaneamente, il terminale deve sempre restituire NOTINUSE di Servizi terminal \_ .

In caso contrario, l'implementazione del terminale limita arbitrariamente il numero di flussi a cui è possibile connettere il terminale alla volta. In questo caso, il terminale deve tenere un conteggio del numero di flussi a cui è connesso. Il terminale deve incrementare il conteggio interno in una chiamata [**ITTerminalControl:: ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) riuscita e decrementare la chiamata a [**ITTerminalControl::D isconnectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) . Nello [**\_ stato ITTerminal:: Get**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)deve restituire \_ InUse di Servizi terminal se il conteggio è uguale al numero massimo di flussi in cui è possibile selezionare il terminale alla volta; in caso contrario, deve restituire NOTINUSE Servizi terminal \_ . Si noti che se il limite è uno, il conteggio può essere semplicemente un valore booleano o un \_ valore dello stato del terminale.

[**ITTerminal:: Get \_ nome**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

Il terminale deve restituire un nome **BSTR** di propria scelta, allocato tramite [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring). Questo nome deve essere significativo per l'utente e deve essere localizzato.

[**ITTerminal:: Get \_ mediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

Il terminale deve restituire il tipo di supporto, ovvero TAPIMEDIATYPE \_ audio o TAPIMEDIATYPE \_ video.

[**Direzione di ITTerminal:: Get \_**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

Il terminale restituisce il \_ valore enum della direzione del terminale che indica la direzione del terminale. Se il terminale è bidirezionale (ad esempio, un Bridge), deve restituire TD \_ bidirezionale.

Il terminale deve implementare [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (solo vtable).

[**ITTerminalControl:: Get \_ AddressHandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

Un terminale fornito dall'applicazione deve sempre restituire **null** come handle di indirizzo. Indica al MSP che questo terminale non è stato creato in un oggetto specifico di un indirizzo MSP.

[**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

In questa chiamata il terminale aggiunge i filtri al grafico specificato e li connette tra loro, se applicabile. Il terminale deve quindi restituire i pin esposti dal terminale per la direzione del flusso specificata.

Un terminale che non supporta la connessione simultanea a più flussi potrebbe impostare una variabile interna su INUSE di Servizi terminal al \_ completamento del metodo.

Il terminale può usare il parametro *dwTerminalDirection* della chiamata per determinare la direzione del flusso a cui è connessa. Questa operazione è necessaria per i terminali bidirezionali.

> [!Note]  
> In genere, nelle classi base MSP e in tutti i MSPs noti, il codice del flusso MSP non riuscirà a connettersi se il terminale restituisce più di un pin da una singola chiamata [**ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) . Questo è corretto, perché un terminale che restituisce più di un PIN durante la connessione richiede che il MSP abbia una conoscenza speciale del terminale per poter usare i pin aggiuntivi in modo efficace.

 

[**ITTerminalControl::CompleteConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

Il terminale dovrebbe solo restituire S \_ OK. Il terminale può inoltre eseguire l'inizializzazione post-connessione, se necessario.

[**ITTerminalControl::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

Il terminale deve eseguire tutte le operazioni necessarie per disconnettere il terminale dal resto del grafo. Questa operazione comporta in genere la rimozione di tutti i filtri dei terminali dal grafico e l'impostazione dello stato finale su Servizi terminal \_ NOTINUSE.

[**ITTerminalControl::RunRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

Il terminale dovrebbe solo restituire E \_ NOTIMPL.

[**ITTerminalControl::StopRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

Il terminale dovrebbe solo restituire E \_ NOTIMPL.

 

 
