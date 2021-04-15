---
title: Oggetti incorporati (Framework di servizi di testo)
description: Il Framework di servizi di testo consente a un servizio di testo di incorporare oggetti in un flusso di testo dell'applicazione.
ms.assetid: 44cb22b5-707b-4f21-b986-5258ed273543
keywords:
- Framework servizi di testo (TSF), oggetti incorporati
- TSF (Framework di servizi di testo), oggetti incorporati
- Applicazioni abilitate per TSF, oggetti incorporati
- oggetti incorporati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e4f819e6f42cc4e8d2ed81e47c79efe5ff7407
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104555997"
---
# <a name="embedded-objects-text-services-framework"></a>Oggetti incorporati (Framework di servizi di testo)

Il Framework di servizi di testo consente a un servizio di testo di incorporare oggetti in un flusso di testo dell'applicazione. Gli oggetti incorporati vengono inseriti nel flusso di testo usando il valore di [TS \_ char \_ Embedded](ts-char--constants.md). Questo valore viene risolto nel carattere di sostituzione dell'oggetto Unicode U + FFFC, usando la notazione esadecimale. Nella figura seguente, ad esempio, viene illustrato il rendering di un oggetto incorporato che rappresenta l'esempio *di ideogrammi giapponese*, in combinazione con la sequenza di caratteri Unicode che rappresentano la traduzione in inglese di "Sun".

![codifica dei caratteri di un oggetto incorporato](images/emb-obj.gif)

La prima riga della figura contiene il testo tradotto, composto dalla parola "Sun" seguito dal carattere giapponese per Sun, *Hi*. La riga centrale della figura mostra il carattere Unicode. Nel caso di U + FFFC, questo è il carattere di sostituzione dell'oggetto. La riga inferiore della figura mostra il valore esadecimale di ogni carattere.

## <a name="supporting-embedded-objects-in-an-application"></a>Supporto di oggetti incorporati in un'applicazione

Gestione TSF inserisce un oggetto incorporato nel flusso di testo chiamando [ITextStoreACP:: InsertEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) per un'applicazione basata su ACP o [ITextStoreAnchor:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) per un'applicazione basata su ancoraggio. Quando si inserisce un oggetto incorporato, l'applicazione deve inserire il **valore \_ \_ incorporato char di Servizi terminal** nella posizione del carattere (o nella posizione di ancoraggio) in cui l'oggetto è incorporato e archiviare il IDataObject associato all'oggetto incorporato. Quando viene chiamato [ITextStoreACP:: GetText](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) o [ITextStoreAnchor:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) e un oggetto incorporato è contenuto all'interno del testo ottenuto, il valore **\_ \_ incorporato di TS char** indica la presenza e la posizione dell'oggetto incorporato. Per ottenere l'oggetto incorporato, chiamare [ITextStoreACP:: Getembedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) con la posizione del carattere dell'oggetto incorporato oppure [ITextStoreAnchor:: getembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) con la posizione di ancoraggio dell'oggetto incorporato.

L'applicazione in genere non riconosce il contenuto dell'oggetto incorporato. L'applicazione può tentare di ottenere informazioni di visualizzazione dall'oggetto stesso. Se l'oggetto incorporato è in grado di fornire dati in un formato riconosciuto dall'applicazione, ad esempio CF \_ UNICODETEXT o la \_ bitmap CF, l'applicazione può visualizzare le informazioni grafiche fornite dall'oggetto.

## <a name="inserting-embedded-objects"></a>Inserimento di oggetti incorporati

Un servizio di testo inserisce un oggetto incorporato in un contesto chiamando [ITfRange:: InsertEmbedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) o [ITfInsertAtSelection:: InsertEmbeddedAtSelection](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection). Il servizio di testo deve fornire il IDataObject incorporato.

 

 
