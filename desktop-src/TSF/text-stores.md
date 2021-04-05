---
title: Archivi di testo
description: Archivi di testo
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Framework servizi di testo (TSF), archivi di testo
- TSF (Framework di servizi di testo), archivi di testo
- Applicazioni abilitate per TSF, archivi di testo
- archivi di testo
- Framework servizi di testo (TSF), posizione carattere applicazione (ACP)
- TSF (Framework dei servizi di testo), posizione dei caratteri dell'applicazione (ACP)
- Applicazioni abilitate per TSF, posizione del carattere dell'applicazione (ACP)
- Posizione carattere applicazione (ACP)
- ACP (posizione carattere applicazione)
- Framework servizi di testo (TSF), ancoraggi
- TSF (Framework di servizi di testo), ancoraggi
- Applicazioni abilitate per TSF, ancoraggi
- ancoraggi
- Framework servizi di testo (TSF), blocchi di documenti
- TSF (Framework dei servizi di testo), blocchi del documento
- Applicazioni abilitate per TSF, blocchi di documenti
- blocchi del documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046934"
---
# <a name="text-stores"></a>Archivi di testo

## <a name="application-character-position-acp"></a>Posizione carattere applicazione (ACP)

Un ACP è la posizione di un carattere o di caratteri in un flusso di testo espresso come il numero di caratteri dall'inizio del flusso di testo. Poiché il modello ACP è in base zero, il primo carattere di un flusso di testo ha un ACP pari a zero. Ad esempio:


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



Un archivio di testo implementa un oggetto che supporta l'interfaccia [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) , che consente di esprimere il flusso di testo in un ACP. I metodi dell'interfaccia **ITextStoreACP** utilizzano l'intervallo ACP del flusso di testo per modificare il testo.

## <a name="anchor-based-applications"></a>Applicazioni Anchor-Based

Il gestore utilizza i metodi basati su ACP in modo nativo per modificare il testo. Tuttavia, un approccio basato su ancoraggio è disponibile per i client [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) che supportano [ancoraggi](ranges.md), in cui il Manager usa i metodi [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) e [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) per eseguire il wrapping dei metodi [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) .

## <a name="document-access-control"></a>Controllo di accesso ai documenti

L'archivio di testo controlla l'accesso al flusso di testo utilizzando i [blocchi del documento](document-locks.md). Per leggere o modificare l'archivio di testo, il Manager deve innanzitutto installare un sink di notifica che supporta l'interfaccia [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) chiamando il metodo [ITextStoreACP:: adviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) e passando un puntatore a un sink di notifica. Il sink di notifica consente al gestore di ottenere un blocco di documento nell'archivio di testo e ricevere notifiche quando l'archivio di testo viene modificato da un elemento diverso dal gestore, ad esempio l'input dell'utente tramite l'applicazione. I sink di notifica sono descritti più avanti in questo argomento.

## <a name="how-to-initialize-the-text-store"></a>Come inizializzare l'archivio di testo

Un'applicazione Inizializza un archivio di testo completando i passaggi seguenti:

1.  Creare un oggetto gestore thread basato sull'interfaccia [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) chiamando la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con un puntatore a un oggetto gestore thread. Di seguito è riportato un esempio di codice relativo all'implementazione di un oggetto gestore thread.
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  Attivare l'oggetto gestore thread chiamando il metodo [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) . Questo metodo fornisce un puntatore a un [identificatore client](tfclientid.md) utilizzato per creare un oggetto di contesto. Gestione thread viene utilizzato per implementare un oggetto di gestione documenti.
3.  Creare un oggetto di gestione documenti basato sull'interfaccia [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) chiamando il metodo [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) con un puntatore all'oggetto gestione documenti. L'oggetto gestione documenti viene utilizzato per implementare un oggetto di contesto che rappresenta l'archivio di testo.
4.  Creare un oggetto di contesto da gestione documenti chiamando il metodo [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) con il puntatore all'oggetto archivio di testo e un puntatore all'identificatore client dall'attivazione di gestione thread. Di seguito è riportato un esempio di creazione di un oggetto di contesto:
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  Eseguire il push dell'oggetto context nello stack con il metodo [ITfDocumentMgr::P USH](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) . Di seguito è riportato un esempio di push dell'oggetto context nello stack:
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>Come modificare l'archivio di testo

Il metodo **ITfDocumentMgr::P USH** chiama **ITextStoreACP:: adviseSink** con un puntatore all'interfaccia di sink Advise per installare un nuovo sink di notifica o modificare un sink di notifica esistente. Il sink di notifica riceve notifiche quando l'archivio di testo viene modificato da un elemento diverso dal gestore, ad esempio l'input dell'utente per l'applicazione. Le applicazioni devono chiamare il metodo [ITfThreadMgrEventSink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) quando il metodo di input ottiene lo stato attivo. Altre notifiche per gestione thread vengono fornite chiamando i metodi di interfaccia **ITextStoreACPSink** appropriati.

Tuttavia, le applicazioni non devono chiamare i metodi dell'interfaccia **ITextStoreACPSink** in risposta ai metodi dell'interfaccia **ITextStoreACP** . Le applicazioni devono chiamare solo i metodi dell'interfaccia **ITextStoreACPSink** quando l'archivio di testo viene modificato da un elemento diverso dal gestore.

Il contenuto dell'archivio di testo può essere modificato con uno stato di input temporaneo denominato [composizione](compositions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ancoraggi](ranges.md)
</dt> <dt>

[Composizioni](compositions.md)
</dt> <dt>

[Blocchi del documento](document-locks.md)
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

[ITfThreadMgrEventSink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 