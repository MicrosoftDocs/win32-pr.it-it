---
title: Composizioni
description: Una composizione è uno stato di input temporaneo che consente a un servizio di testo di specificare sia per l'applicazione sia per l'utente che il testo di input è ancora in uno stato di modifica.
ms.assetid: 3d9da4f2-ceb9-4abc-8979-d3756d948a57
keywords:
- Framework servizi di testo (TSF), composizioni
- TSF (Framework di servizi di testo), composizioni
- Servizi di testo, composizioni
- Applicazioni abilitate per TSF, composizioni
- compositions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b03f3e991f76ee7c6dca3830267796576c7b842
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399499"
---
# <a name="compositions"></a>Composizioni

Una composizione è uno stato di input temporaneo che consente a un servizio di testo di specificare sia per l'applicazione sia per l'utente che il testo di input è ancora in uno stato di modifica. Un'applicazione può e deve ottenere informazioni sugli attributi di visualizzazione sulla composizione e utilizzare queste informazioni per visualizzare lo stato di composizione all'utente.

Un esempio di utilizzo di una composizione è durante l'input vocale. Mentre l'utente sta parlando, il servizio di testo vocale crea una composizione. Questa composizione rimarrà intatta fino al completamento dell'intero input vocale. Al termine della sessione, il servizio di testo vocale termina la composizione.

Un'applicazione utilizza la presenza e l'assenza di una composizione per determinare la modalità di visualizzazione del testo e il tipo di elaborazione da eseguire sul testo. Se, ad esempio, l'utente usa il motore vocale per inserire il testo, l'applicazione non deve eseguire alcun controllo ortografico o grammaticale su qualsiasi testo di composizione. Il testo viene considerato incompleto fino a quando non viene terminata la composizione.

## <a name="text-services"></a>Servizi di testo

Un servizio di testo crea una composizione chiamando [ITfContextComposition:: StartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition). Il servizio di testo può implementare facoltativamente un oggetto [ITfCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcompositionsink) che riceve le notifiche degli eventi di composizione. StartComposition restituisce un oggetto [ITfComposition](/windows/desktop/api/msctf/nn-msctf-itfcomposition) a cui il servizio di testo mantiene un riferimento e utilizza per modificare e terminare la composizione. Il servizio di testo termina la composizione chiamando [ITfComposition:: EndComposition](/windows/desktop/api/msctf/nf-msctf-itfcomposition-endcomposition).

Se un servizio di testo crea composizioni, deve supportare anche gli attributi di visualizzazione per consentire a un'applicazione di visualizzare il testo che fa parte di una composizione in modo diverso rispetto al testo standard. Per ulteriori informazioni, vedere [fornire attributi di visualizzazione](providing-display-attributes.md).

## <a name="applications"></a>Applicazioni

Un'applicazione può monitorare la creazione, la modifica e la chiusura di composizioni installando un sink [ITfContextOwnerCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink) . Quando viene avviata una composizione, viene chiamato [ITfContextOwnerCompositionSink:: OnStartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onstartcomposition) . Analogamente, quando una composizione viene modificata o terminata, [ITfContextOwnerCompositionSink:: OnUpdateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onupdatecomposition) e [ITfContextOwnerCompositionSink:: OnEndComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onendcomposition) verranno chiamati rispettivamente.

Di seguito è riportata una procedura tipica per aggiornare un documento utilizzando una composizione.

1.  [ITextStoreACP:: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection) o [ITextStoreAnchor:: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection) vengono in genere utilizzati per inserire il testo iniziale nella composizione.
2.  La composizione viene avviata con una chiamata a [ITfContextComposition:: StartComposition](/windows/desktop/api/Msctf/nf-msctf-itfcontextcomposition-startcomposition), usando l'intervallo di testo restituito da **InsertTextAtSelection**.
3.  Quando riceve nuovo input, ad esempio voce vocale o voce da tastiera, l'applicazione aggiorna la composizione con [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext) o [ITextStoreAnchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext).
4.  Quando l'applicazione determina che è il momento di terminare la composizione, viene chiamato [ITfComposition:: EndComposition](/windows/desktop/api/Msctf/nf-msctf-itfcomposition-endcomposition).

L'applicazione deve usare gli attributi di visualizzazione forniti dal servizio di testo per modificare la visualizzazione del testo in qualsiasi momento e non solo quando è attiva una composizione. Per ulteriori informazioni, vedere [utilizzo degli attributi di visualizzazione](using-display-attributes.md).

Se necessario, un'applicazione può terminare una composizione chiamando [ITfContextOwnerCompositionServices:: TerminateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionservices-terminatecomposition).

 

 