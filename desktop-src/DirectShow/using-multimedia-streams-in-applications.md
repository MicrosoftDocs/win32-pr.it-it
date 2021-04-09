---
description: Uso di flussi multimediali nelle applicazioni
ms.assetid: 73cfe89b-df46-445a-92c7-2f7323672441
title: Uso di flussi multimediali nelle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30dab204bc7b0bddbdc293708daecbe0558e8f9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968915"
---
# <a name="using-multimedia-streams-in-applications"></a>Uso di flussi multimediali nelle applicazioni

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.

 

Le interfacce di streaming multimediali semplificano notevolmente il processo di manipolazione dei dati multimediali rimuovendo la dipendenza da caratteristiche specifiche dell'hardware o dell'origine software e fornendo supporto per tutti i formati di file multimediali Microsoft DirectX®. I flussi astraggono i dati a un livello molto elevato; le applicazioni possono anche spostare i dati da un flusso all'altro senza conoscere il formato dei dati.

Per creare un flusso multimediale, seguire questa procedura.

1.  Creare il flusso multimediale. Il metodo di creazione e inizializzazione del flusso è specifico dell'architettura. DirectShow supporta l'interfaccia [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) , che viene usata per inizializzare il flusso. Altre implementazioni del server in-process di [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) verranno create e inizializzate con meccanismi diversi.
2.  Dopo l'inizializzazione dell'oggetto flusso multimediale, l'applicazione utilizzerà **QueryInterface** per recuperare l'interfaccia **IMultiMediaStream** per l'oggetto. Usare questa interfaccia per determinare le proprietà del flusso ed enumerare i flussi stessi. È possibile recuperare un flusso specifico chiamando il metodo [**IMultiMediaStream:: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) con un ID scopo specifico. MSPID \_ PrimaryVideo e MSPID \_ PrimaryAudio, che rappresentano i flussi video e audio principali, sono gli ID finalità usati più di frequente.
3.  Chiamare **IUnknown:: QueryInterface** per un'interfaccia specifica del tipo di supporto del flusso. Se si vuole eseguire il rendering di un flusso video, ad esempio, recuperare l'interfaccia [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) . Le interfacce specifiche del supporto definiscono metodi aggiuntivi necessari per sfruttare appieno le funzionalità di un formato.
4.  Creare uno o più esempi dai dati di flusso. Ogni flusso multimediale supporta il metodo [**IMediaStream:: CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) per la creazione di esempi. L'esempio risultante supporta l'interfaccia [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) , che consente di controllare l'esempio e le relative caratteristiche. In genere, il flusso multimediale supporta un metodo specifico del formato per la creazione di esempi più potente rispetto ai metodi **IStreamSample** sopra indicati. **IDirectDrawMediaStream**, ad esempio, può creare esempi collegati a una superficie e un rettangolo di ritaglio di DirectDraw desiderati. In alcune situazioni, tuttavia, è necessario gestire i dati senza conoscere il relativo formato dati. Se si vuole trasmettere i dati indipendentemente dal formato, usare il metodo **IMediaStream:: CreateSharedSample** per creare gli esempi di dati.
5.  Dopo aver creato tutti gli esempi di flusso desiderati, avviare il flusso chiamando il metodo [**IMultiMediaStream:: sestate**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate) e passare il \_ flag di esecuzione STREAMSTATE come parametro.
6.  Chiamare [**IStreamSample:: Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) per aggiornare l'esempio di flusso. Quando il metodo **IStreamSample:: Update** viene chiuso, è possibile accedere ai dati dell'esempio. Se si desidera che un trigger chiami un evento o una funzione specifica quando l'aggiornamento viene restituito, passare i puntatori appropriati al metodo **IStreamSample:: Update** .

Per altre informazioni sulle interfacce di streaming multimediali, vedere [streaming multimediale](multimedia-streaming.md).

 

 



