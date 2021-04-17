---
description: Le voci XAudio2 possono eseguire conversioni automatiche di frequenza di campionamento se la frequenza di campionamento di input è diversa dalla frequenza di campionamento di input delle voci di output.
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: Conversioni di frequenza di campionamento XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d437a45f9e896826bedc1418382fb257201722d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234056"
---
# <a name="xaudio2-sample-rate-conversions"></a>Conversioni di frequenza di campionamento XAudio2

Le voci XAudio2 possono eseguire conversioni automatiche di frequenza di campionamento se la frequenza di campionamento di input è diversa dalla frequenza di campionamento di input delle voci di output.

Le conversioni di frequenza di campionamento seguono le seguenti regole:

-   La frequenza di campionamento dell'input vocale è fissa.

    Le voci possono gestire solo la frequenza di campionamento di input specificata al momento della creazione. Per le voci di [**Mastering Voices**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) e [**submix**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice), la frequenza di campionamento di input viene specificata con l'argomento *InputSampleRate* per le funzioni [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) e [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice) . Per le voci di origine, la frequenza di campionamento di input della voce viene specificata dall'argomento pSourceFormat per la funzione [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .

-   Tutte le voci di output di una voce devono avere la stessa frequenza di campionamento di input.

    Le voci possono eseguire la conversione dalla frequenza di campionamento di input a qualsiasi frequenza di campionamento di output, ma tutte le voci di output della voce devono avere la stessa frequenza di campionamento di input. Ad esempio, una voce può restituire un numero qualsiasi di voci con una frequenza di campionamento di input pari a 22 kHz. Tuttavia, se la stessa voce aveva diverse voci di output, ognuna con una frequenza di campionamento di input diversa, il grafico audio non sarebbe valido.

-   L'elaborazione della conversione della frequenza di campionamento si verifica solo quando necessario.

    La conversione di dati audio in una frequenza di campionamento diversa comporta un sovraccarico di elaborazione maggiore, che è preferibile evitare. Se la frequenza di campionamento di input di una voce corrisponde alla frequenza di campionamento di input delle voci di output, questa conversione non viene eseguita e il tempo di elaborazione viene abbreviato.

-   La frequenza di campionamento dell'output può variare in base alla durata di una voce.

    La frequenza di campionamento dell'output di una voce non è fissa. Finché tutte le voci di output avranno la stessa frequenza di campionamento di input, il grafico audio sarà valido. Se una voce viene modificata in output in nuove voci con una frequenza di campionamento di input diversa, la voce viene convertita nella frequenza di campionamento di input delle nuove voci.

Esistono alcuni scenari in cui è necessario aggiungere una voce submix per eseguire la conversione della frequenza di campionamento tra le voci. Se una voce deve essere restituita a voci con varie frequenze di campionamento di input, solo una delle voci può essere un output diretto della voce originale. Poiché tutte le voci di output di una voce devono avere la stessa frequenza di campionamento di input, le altre voci ricevono indirettamente l'output. Deve essere presente una voce submix con la frequenza di esempio di input corretta compresa tra la voce originale e la voce di output desiderata.

Si consideri, ad esempio, una voce di origine con una frequenza di campionamento di input pari a 22 kHz, che deve essere restituita a una voce submix con una frequenza di campionamento di input di 11 kHz e una voce Master con una frequenza di campionamento di input pari a 44,1 kHz. Poiché le due voci di output hanno frequenze di campionamento diverse, è necessario inserire più voci submix tra la voce originale e le voci di output desiderate. Per mantenere la fedeltà della voce di origine ed evitare le conversioni costose superflue a frequenze di campionamento più elevate, è necessario inserire due voci submix con frequenza di input di esempio di 22 kHz nel grafico. Una voce submix restituirà a 11 kHz la voce submix con l'effetto del riverbero e l'altra voce submix restituirà alla voce mastering a 44,1 kHz.

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a>Esempi di conversione della frequenza di campionamento nei grafici audio

Tutte le voci hanno la stessa frequenza di input di esempio; nel grafico audio non viene eseguita alcuna conversione della frequenza di campionamento.![nel grafico audio non viene eseguita alcuna conversione della frequenza di campionamento.](images/xaudio2-sample-rate-conversions-1.png)

Tutte le voci hanno lo stesso tasso di input di esempio, tranne la voce di mastering; la conversione della frequenza di campionamento viene eseguita solo sui dati che passano alla voce Master. ![la conversione della frequenza di campionamento viene eseguita solo sui dati che passano alla voce Master.](images/xaudio2-sample-rate-conversions-2.png)

Le voci hanno frequenze di input di esempio diverse e richiedono più voci submix per eseguire conversioni di frequenza di campionamento. la conversione della frequenza di campionamento viene eseguita in più posizioni nel grafico audio. ![la conversione della frequenza di campionamento viene eseguita in più posizioni nel grafico audio.](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Voci](voices.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> </dl>

 

 
