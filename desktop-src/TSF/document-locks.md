---
title: Blocchi del documento
description: Blocchi del documento
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- Framework servizi di testo (TSF), blocchi di documenti
- TSF (Framework dei servizi di testo), blocchi del documento
- Applicazioni abilitate per TSF, blocchi di documenti
- blocchi del documento
- Framework servizi di testo (TSF), posizione carattere applicazione (ACP)
- TSF (Framework dei servizi di testo), posizione dei caratteri dell'applicazione (ACP)
- Applicazioni abilitate per TSF, posizione del carattere dell'applicazione (ACP)
- Posizione carattere applicazione (ACP)
- ACP (posizione carattere applicazione)
- Framework servizi di testo (TSF), ancoraggi
- TSF (Framework di servizi di testo), ancoraggi
- Applicazioni abilitate per TSF, ancoraggi
- ancoraggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221184"
---
# <a name="document-locks"></a>Blocchi del documento

## <a name="the-document-lock-protocol"></a>Protocollo di blocco del documento

Per richiedere un blocco del documento per le applicazioni basate su ACP, il gestore di TSF chiama [ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock). Per le applicazioni basate su ancoraggio, il gestore di TSF chiama [ITextStoreAnchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock). L'applicazione concede il blocco del documento chiamando [ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (applicazioni basate su ACP) o [ITextStoreAnchorSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (applicazioni basate su ancoraggio) all'interno di **RequestLock**. Il blocco è valido solo durante la chiamata **OnLockGranted** . Quando **OnLockGranted** restituisce, il documento viene considerato sbloccato.

## <a name="types-of-document-locks"></a>Tipi di blocchi di documenti

Esistono due tipi di blocchi di documento, di sola lettura e di lettura/scrittura. Un blocco di sola lettura consente al gestore di leggere il testo, ma non di modificare o inserire testo. Un blocco di lettura/scrittura consente al gestore di leggere, modificare e inserire testo. È necessario un blocco di sola lettura specificando TS \_ LF \_ Read in *dwFlags*. È necessario un blocco di lettura/scrittura specificando TS \_ LF \_ ReadWrite in *dwFlags*.

## <a name="asynchronous-and-synchronous-requests"></a>Richieste asincrone e sincrone

Una richiesta di blocco può essere sincrona o asincrona. Il gestore richiede un blocco sincrono tramite il flag di sincronizzazione di TS \_ LF \_ in *dwFlags*. Se questo flag non è presente, la richiesta è asincrona.

## <a name="granting-the-lock"></a>Concessione del blocco

Quando viene chiamato **RequestLock** , l'applicazione deve determinare se il documento è attualmente bloccato. Se il documento non è bloccato e non esistono altri motivi per negare il blocco, l'applicazione deve impostare *phrSession* su S \_ OK e restituire s \_ OK.

Se il documento è bloccato e la richiesta di blocco è sincrona, l'applicazione deve impostare *phrSession* su TS e \_ \_ sincrono e restituire S \_ OK. Indica che non è possibile concedere una richiesta sincrona.

Se il documento è bloccato e la richiesta di blocco è asincrona, l'applicazione deve accodare la richiesta, impostare *phrSession* su TS \_ S \_ Async e restituire s \_ OK. Quando il documento diventa disponibile, l'applicazione deve rimuovere la richiesta dalla coda e chiamare **OnLockGranted**. Questo Accodamento di richieste di blocco è facoltativo. esiste uno scenario che un'applicazione deve supportare. Se il documento ha un blocco di sola lettura, la nuova richiesta di blocco è di lettura/scrittura e la richiesta è asincrona, l'applicazione ha chiamato in **OnLockGranted** , che ha causato una chiamata rientrante a **RequestLock**. L'applicazione deve impostare *phrSession* su TS \_ s \_ Async e restituire s \_ OK. Dopo che la chiamata a **OnLockGranted** restituisce, l'applicazione deve elaborare la richiesta di aggiornamento chiamando di nuovo **OnLockGranted** con TS \_ LF \_ ReadWrite.

## <a name="lock-enforcement"></a>Imposizione del blocco

Prima di consentire l'accesso al documento, l'applicazione deve verificare che sia presente il tipo di blocco appropriato. Ad esempio, l'applicazione deve verificare che un documento disponga di almeno un blocco di sola lettura prima di consentire a [ITextStoreACP:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) o [ITextStoreAnchor:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) di continuare. Se il blocco appropriato non esiste, l'applicazione deve restituire TF \_ E \_ NOLOCK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Archivi di testo](text-stores.md)
</dt> <dt>

[ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreACP:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[ITextStoreAnchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[ITextStoreAnchorSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[ITextStoreAnchor:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




