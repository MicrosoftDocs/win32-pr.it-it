---
title: Modificare i contesti
description: Modificare i contesti
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- Framework servizi di testo (TSF), modifica contesti
- TSF (Framework dei servizi di testo), modificare i contesti
- Servizi di testo, modifica di contesti
- Applicazioni abilitate per TSF, modifica di contesti
- modificare i contesti
- Framework servizi di testo (TSF), modifica cookie
- TSF (Framework servizi di testo), modifica cookie
- Servizi di testo, modifica cookie
- Applicazioni abilitate per TSF, modifica cookie
- modifica cookie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855942"
---
# <a name="edit-contexts"></a>Modificare i contesti

## <a name="applications"></a>Applicazioni

Per creare un contesto di modifica, un'applicazione chiama [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).

## <a name="text-services"></a>Servizi di testo

Un servizio di testo usa spesso il contesto di modifica attualmente attivo. Il contesto di modifica attualmente attivo è il contesto di modifica nella parte superiore dello stack di gestione documenti attivi. Per ottenere il contesto attualmente attivo, un servizio di testo chiama [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) per ottenere il gestore dei documenti attivi e quindi chiama [ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) per ottenere il contesto di modifica all'inizio dello stack.

In alcuni casi, un servizio di testo richiede un proprio contesto di modifica. Per creare un contesto di modifica, un servizio di testo chiama **ITfDocumentMgr:: CreateContext**.

## <a name="edit-cookies"></a>Modifica cookie

Molti metodi, ad esempio [ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), richiedono un modo per identificare un contesto di modifica con [blocco del documento](document-locks.md)di sola lettura o di lettura/scrittura. Un blocco del documento viene ottenuto tramite una negoziazione tra gestione TSF e l'applicazione. Un servizio di testo non è in grado di eseguire direttamente questa negoziazione. Un servizio di testo può ottenere un blocco solo richiedendo una [sessione di modifica](edit-sessions.md) con un contesto specifico e accesso in sola lettura o in lettura/scrittura. Quando viene concessa la sessione di modifica, il servizio di testo viene fornito con un *cookie di modifica* che identifica il contesto di modifica con l'accesso richiesto. Questo cookie viene quindi passato al metodo per identificare il contesto di modifica con l'accesso appropriato.

**ITfDocumentMgr:: CreateContext** fornisce anche un cookie di modifica all'autore del contesto. Questo cookie ha accesso in sola lettura e non è possibile modificare il livello di accesso. In realtà, il gestore di TSF non negozia un blocco del documento per questo cookie di modifica. Il cookie è contrassegnato internamente come di sola lettura, ma il documento non è effettivamente bloccato. Se, ad esempio, l'autore del contesto chiama [ITfContext:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) con il cookie di modifica restituito da **ITfDocumentMgr:: CreateContext** , si ottiene la chiamata a [ITextStoreACP:: getselectation](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) o [ITextStoreAnchor:: getselect](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) dell'applicazione. Prima di ottenere la selezione, l'applicazione determinerà se è presente un blocco del documento. Poiché non esiste alcun blocco, l'applicazione avrà esito negativo con TS \_ E \_ NOLOCK. Ovvero, se un'applicazione chiama un metodo con questo cookie che comporta la chiamata di uno dei metodi dell'archivio di testo dell'applicazione, deve gestire questo caso internamente perché l'applicazione non avrà effettivamente un blocco del documento.

Se il creatore del contesto richiede un cookie di modifica con accesso in lettura/scrittura, deve stabilire una propria sessione di modifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[Blocchi del documento](document-locks.md)
</dt> <dt>

[Sessioni di modifica](edit-sessions.md)
</dt> <dt>

[ITfContext:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




