---
title: Oggetti incorporati (Framework servizi di testo)
description: Framework servizi di testo un servizio di testo per incorporare oggetti in un flusso di testo dell'applicazione.
ms.assetid: 44cb22b5-707b-4f21-b986-5258ed273543
keywords:
- Framework servizi di testo (TSF), oggetti incorporati
- TSF (Framework servizi di testo), oggetti incorporati
- Applicazioni abilitate per TSF,oggetti incorporati
- oggetti incorporati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c45c14138df39142f503882c8d735ff1638618e028870af6aa67c25bc1a98b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118879680"
---
# <a name="embedded-objects-text-services-framework"></a>Oggetti incorporati (Framework servizi di testo)

Framework servizi di testo un servizio di testo per incorporare oggetti in un flusso di testo dell'applicazione. Gli oggetti incorporati vengono inseriti nel flusso di testo usando il [valore TS \_ CHAR \_ EMBEDDED](ts-char--constants.md). Questo valore viene risolto nel carattere di sostituzione dell'oggetto Unicode U+fffc, usando la notazione esadecimale. Ad esempio, la figura seguente mostra il rendering di un oggetto incorporato che rappresenta l'ideogramma *giapponese hi*, in combinazione con la sequenza di caratteri Unicode che rappresentano la traduzione inglese di "Sun".

![codifica dei caratteri di un oggetto incorporato](images/emb-obj.gif)

La riga superiore della figura contiene il testo tradotto, costituito dalla parola "Sun" seguita dal carattere giapponese per sun, *hi*. La riga centrale della figura mostra il carattere Unicode. Nel caso di U+fffc, si tratta del carattere di sostituzione dell'oggetto. La riga inferiore della figura mostra il valore esadecimale di ogni carattere.

## <a name="supporting-embedded-objects-in-an-application"></a>Supporto di oggetti incorporati in un'applicazione

Il gestore TSF inserisce un oggetto incorporato nel flusso di testo chiamando [ITextStoreACP::InsertEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) per un'applicazione basata su ACP o [ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) per un'applicazione basata su ancoraggio. Quando viene inserito un oggetto incorporato, l'applicazione deve inserire il valore **TS \_ CHAR \_ EMBEDDED** nella posizione del carattere (o posizione di ancoraggio) in cui è incorporato l'oggetto e archiviare L'oggetto IDataObject associato all'oggetto incorporato. Quando viene chiamato [ITextStoreACP::GetText](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) o [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) e un oggetto incorporato è contenuto nel testo ottenuto, il valore **TS \_ CHAR \_ EMBEDDED** indica la presenza e la posizione dell'oggetto incorporato. Per ottenere l'oggetto incorporato, chiamare [ITextStoreACP::GetEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) con la posizione del carattere dell'oggetto incorporato oppure [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) con la posizione di ancoraggio dell'oggetto incorporato.

L'applicazione in genere non riconosce il contenuto dell'oggetto incorporato. L'applicazione può tentare di ottenere informazioni di visualizzazione dall'oggetto stesso. Se l'oggetto incorporato può fornire dati in un formato riconosciuto dall'applicazione, ad esempio CF UNICODETEXT o CF BITMAP, l'applicazione può visualizzare le informazioni grafiche fornite \_ \_ dall'oggetto .

## <a name="inserting-embedded-objects"></a>Inserimento di oggetti incorporati

Un servizio di testo inserisce un oggetto incorporato in un contesto chiamando [ITfRange::InsertEmbedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) o [ITfInsertAtSelection::InsertEmbeddedAtSelection](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection). Il servizio di testo deve fornire L'oggetto IDataObject incorporato.

 

 
