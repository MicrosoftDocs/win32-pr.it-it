---
description: Le voci XAudio2 possono eseguire conversioni automatiche della frequenza di campionamento se la frequenza di campionamento di input è diversa dalla frequenza di campionamento di input delle voci di output.
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: Conversioni della frequenza di campionamento XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82983d1d9307551e516f1b8b60676b4b250450da65f416c340446c5a906f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962535"
---
# <a name="xaudio2-sample-rate-conversions"></a>Conversioni della frequenza di campionamento XAudio2

Le voci XAudio2 possono eseguire conversioni automatiche della frequenza di campionamento se la frequenza di campionamento di input è diversa dalla frequenza di campionamento di input delle voci di output.

Le conversioni della frequenza di campionamento seguono queste regole:

-   La frequenza di campionamento dell'input vocale è fissa.

    Le voci possono gestire solo la frequenza di campionamento di input specificata al momento della creazione. Per [**la mastering**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) di voci e [**voci submix,**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)la frequenza di campionamento di input viene specificata con l'argomento *InputSampleRate* per le funzioni [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) e [**IXAudio2::CreateSubmixVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice) Per le voci di origine, la frequenza di campionamento di input della voce viene specificata dall'argomento pSourceFormat per la [**funzione IXAudio2::CreateSourceVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)

-   Tutte le voci di output di una voce devono avere la stessa frequenza di campionamento di input.

    Le voci possono eseguire la conversione dalla frequenza di campionamento di input a qualsiasi frequenza di campionamento di output, ma tutte le voci di output della voce devono avere la stessa frequenza di campionamento di input. Ad esempio, una voce può essere restituita a qualsiasi numero di voci con una frequenza di campionamento di input di 22 kHz. Tuttavia, se la stessa voce avesse diverse voci di output, ognuna delle quali aveva una frequenza di campionamento di input diversa, il grafico audio non sarebbe valido.

-   L'elaborazione della conversione della frequenza di campionamento si verifica solo quando necessario.

    La conversione dei dati audio in una frequenza di campionamento diversa comporta un maggiore sovraccarico di elaborazione, che è preferibile evitare. Se la frequenza di campionamento di input di una voce corrisponde alla frequenza di campionamento di input delle voci di output, questa conversione non viene eseguita e il tempo di elaborazione viene ridotto.

-   La frequenza di campionamento dell'output può variare nel corso della durata di una voce.

    La frequenza di campionamento dell'output di una voce non è fissa. Finché tutte le voci di output hanno la stessa frequenza di campionamento di input, il grafico audio sarà valido. Se una voce viene modificata in output in nuove voci con una frequenza di campionamento di input diversa, la voce verrà convertita nella frequenza di campionamento di input delle nuove voci.

Esistono alcuni scenari in cui è necessario aggiungere una voce submix per eseguire la conversione della frequenza di campionamento tra le voci. Se una voce deve eseguire l'output in voci con diverse frequenze di campionamento di input, solo una delle voci può essere un output diretto della voce originale. Poiché tutte le voci di output di una voce devono avere la stessa frequenza di campionamento di input, le altre voci ricevono l'output indirettamente. Deve essere presente una voce submix con la frequenza di campionamento di input corretta compresa tra la voce originale e la voce di output prevista.

Si consideri ad esempio una voce di origine con una frequenza di campionamento di input di 22 kHz, che deve essere restituita a una voce submix con una frequenza di campionamento di input di 11 kHz e una voce mastering con una frequenza di campionamento di input di 44,1 kHz. Poiché le due voci di output hanno frequenze di campionamento di input diverse, è necessario inserire più voci submix tra la voce originale e le voci di output destinate. Per mantenere la fedeltà della voce di origine ed evitare inutili conversioni costose a frequenze di campionamento più elevate, è necessario inserire due voci submix con frequenze di input di esempio di 22 khz nel grafico. Una voce submix genera un output a 11 khz alla voce submix con l'effetto riverbero e l'altra voce submix restituisce alla voce mastering a 44,1 khz.

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a>Esempi di conversione della frequenza di campionamento nei grafici audio

Tutte le voci hanno la stessa frequenza di input di esempio. nel grafico audio non viene eseguita alcuna conversione della frequenza di campionamento.![nel grafico audio non viene eseguita alcuna conversione della frequenza di campionamento.](images/xaudio2-sample-rate-conversions-1.png)

Tutte le voci hanno la stessa frequenza di input di esempio, ad eccezione della voce mastering. La conversione della frequenza di campionamento viene eseguita solo sui dati che vengono alla voce di mastering. ![La conversione della frequenza di campionamento viene eseguita solo sui dati che vengono alla voce di mastering.](images/xaudio2-sample-rate-conversions-2.png)

Le voci hanno frequenze di input di esempio diverse e richiedono più voci submix per eseguire conversioni della frequenza di campionamento; La conversione della frequenza di campionamento viene eseguita in più posizioni nel grafico audio. ![La conversione della frequenza di campionamento viene eseguita in più posizioni nel grafico audio.](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Voci](voices.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> </dl>

 

 
