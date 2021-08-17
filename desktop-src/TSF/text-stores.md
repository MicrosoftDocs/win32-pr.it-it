---
title: Archivi di testo
description: Archivi di testo
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Framework servizi di testo (TSF), archivi di testo
- TSF (Framework servizi di testo),archivi di testo
- applicazioni abilitate per TSF, archivi di testo
- archivi di testo
- Framework servizi di testo (TSF),Application Character Position (ACP)
- TSF (Framework servizi di testo),Application Character Position (ACP)
- Applicazioni abilitate per TSF, posizione dei caratteri dell'applicazione (ACP)
- Posizione dei caratteri dell'applicazione (ACP)
- ACP (posizione del carattere dell'applicazione)
- Framework servizi di testo (TSF), ancoraggi
- TSF (Framework servizi di testo), ancoraggi
- applicazioni abilitate per TSF, ancoraggi
- ancoraggi
- Framework servizi di testo (TSF), blocchi di documenti
- TSF (Framework servizi di testo), blocchi di documenti
- Applicazioni abilitate per TSF, blocchi di documenti
- blocchi di documenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af01edd439dbac23e4dee4b5289101a9bd92ca8180b66b460096b797d32b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950921"
---
# <a name="text-stores"></a>Archivi di testo

## <a name="application-character-position-acp"></a>Posizione dei caratteri dell'applicazione (ACP)

Un ACP è la posizione di un carattere, o caratteri, in un flusso di testo espresso come numero di caratteri dall'inizio del flusso di testo. Poiché il modello ACP è in base zero, il primo carattere in un flusso di testo ha un ACP pari a zero. Esempio:


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



Un archivio di testo implementa un oggetto che supporta [l'interfaccia ITextStoreACP,](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) che consente di esprimere il flusso di testo in un ACP. I **metodi dell'interfaccia ITextStoreACP** usano l'intervallo ACP del flusso di testo per modificare il testo.

## <a name="anchor-based-applications"></a>Anchor-Based applicazioni

Il gestore usa i metodi basati su ACP in modo nativo per modificare il testo. Tuttavia, è disponibile un approccio basato sull'ancoraggio per i client Microsoft Active Accessibility che supportano gli [ancoraggi,](../winauto/microsoft-active-accessibility.md) in cui il gestore usa i metodi [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) e [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) per eseguire il wrapping dei metodi [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreACPSink.](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) [](ranges.md)

## <a name="document-access-control"></a>Controllo di accesso ai documenti

L'archivio di testo controlla l'accesso al flusso di testo tramite [blocchi del documento.](document-locks.md) Per leggere o modificare l'archivio di testo, il gestore deve prima installare un sink di consulenza che supporti l'interfaccia [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) chiamando il metodo [ITextStoreACP::AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) e passando un puntatore a un sink advise. Il sink di avviso consente al gestore di ottenere blocchi di documenti sull'archivio di testo e ricevere notifiche quando l'archivio di testo viene modificato da un elemento diverso dal gestore, ad esempio l'input dell'utente tramite l'applicazione. I sink di consulenza sono descritti più avanti in questo argomento.

## <a name="how-to-initialize-the-text-store"></a>Come inizializzare l'archivio di testo

Un'applicazione inizializza un archivio di testo completando la procedura seguente:

1.  Creare un oggetto di gestione thread basato [sull'interfaccia ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) chiamando la [funzione CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con un puntatore a un oggetto di gestione thread. Di seguito è riportato un esempio di codice di implementazione di un oggetto di gestione thread.
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  Attivare l'oggetto di gestione thread chiamando il [metodo ITfThreadMgr::Activate.](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) Questo metodo fornisce un puntatore a un identificatore [client usato](tfclientid.md) per creare un oggetto contesto. Il gestore di thread viene usato per implementare un oggetto di gestione documenti.
3.  Creare un oggetto di gestione documenti basato [sull'interfaccia ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) chiamando il metodo [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) con un puntatore all'oggetto di gestione documenti. L'oggetto di gestione documenti viene usato per implementare un oggetto contesto che rappresenta l'archivio di testo.
4.  Creare un oggetto contesto dal gestore documenti chiamando il metodo [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) con il puntatore all'oggetto archivio di testo e un puntatore all'identificatore client dall'attivazione del gestore di thread. Di seguito è riportato un esempio di creazione di un oggetto contesto:
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  Eseguire il push dell'oggetto di contesto nello stack con il [metodo ITfDocumentMgr::P ush.](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) Di seguito è riportato un esempio di push dell'oggetto di contesto nello stack:
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>Come modificare l'archivio di testo

Il metodo **ITfDocumentMgr::P ush** chiama **ITextStoreACP::AdviseSink** con un puntatore all'interfaccia sink advise per installare un nuovo sink di consulenza o modificare un sink advise esistente. Il sink di consulenza riceve notifiche quando l'archivio di testo viene modificato da un elemento diverso dal gestore, ad esempio l'input dell'utente per l'applicazione. Le applicazioni devono chiamare il [metodo ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) quando il metodo di input ottiene lo stato attivo. Altre notifiche al gestore di thread vengono fornite chiamando ai metodi di interfaccia **ITextStoreACPSink** appropriati.

Tuttavia, le applicazioni non devono chiamare i **metodi dell'interfaccia ITextStoreACPSink** in risposta ai **metodi dell'interfaccia ITextStoreACP.** Le applicazioni devono chiamare i **metodi dell'interfaccia ITextStoreACPSink** solo quando l'archivio di testo viene modificato da un elemento diverso dal gestore.

Il contenuto dell'archivio di testo può essere modificato con uno stato di input temporaneo denominato [composizione](compositions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ancoraggi](ranges.md)
</dt> <dt>

[Composizioni](compositions.md)
</dt> <dt>

[Blocchi dei documenti](document-locks.md)
</dt> <dt>

[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 