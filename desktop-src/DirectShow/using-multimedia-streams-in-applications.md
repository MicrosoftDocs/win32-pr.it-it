---
description: Uso di Flussi multimediali nelle applicazioni
ms.assetid: 73cfe89b-df46-445a-92c7-2f7323672441
title: Uso di Flussi multimediali nelle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faadcf755019291ae394d03aac5fb16aa632605b5e1c5bc2a8a457de55343757
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525961"
---
# <a name="using-multimedia-streams-in-applications"></a>Uso di Flussi multimediali nelle applicazioni

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il [**filtro Grabber**](sample-grabber-filter.md) di esempio o implementare un filtro personalizzato per ottenere dati da un DirectShow di filtro.

 

Le interfacce di streaming multimediale semplificano notevolmente il processo di modifica dei dati multimediali rimuovendo la dipendenza dalle caratteristiche specifiche dell'origine hardware o software e fornendo il supporto per tutti i formati multimediali Microsoft DirectX®. Flussi astrarre i dati a un livello molto elevato; Le applicazioni possono anche spostare i dati da un flusso a un altro senza conoscere il formato dei dati.

Seguire questa procedura per creare un flusso multimediale.

1.  Creare il flusso multimediale. Il metodo di creazione e inizializzazione del flusso è specifico dell'architettura. DirectShow supporta [**l'interfaccia IAMMultiMediaStream,**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) usata per inizializzare il flusso. Altre implementazioni server in-process [**di IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) verranno create e inizializzate usando meccanismi diversi.
2.  Dopo l'inizializzazione dell'oggetto flusso multimediale, l'applicazione userà **QueryInterface** per recuperare **l'interfaccia IMultiMediaStream** per l'oggetto. Usare questa interfaccia per determinare le proprietà del flusso ed enumerare i flussi stessi. È possibile recuperare un flusso specifico chiamando il [**metodo IMultiMediaStream::GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) con un ID scopo specifico. MSPID \_ PrimaryVideo e MSPID PrimaryAudio, che rappresentano i flussi audio e video primari, sono gli ID di scopo usati più \_ comunemente.
3.  Chiamare **IUnknown::QueryInterface** per un'interfaccia specifica del tipo di supporto del flusso. Se si vuole eseguire il rendering di un flusso video, ad esempio, recuperare la relativa [**interfaccia IDirectDrawMediaStream.**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) Le interfacce specifiche dei supporti definiscono metodi aggiuntivi necessari per sfruttare appieno le funzionalità di un formato.
4.  Creare uno o più esempi dai dati del flusso. Ogni flusso multimediale supporta il [**metodo IMediaStream::CreateSharedSample per**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) la creazione di esempi. L'esempio risultante supporta [**l'interfaccia IStreamSample,**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) che fornisce il controllo sull'esempio e sulle relative caratteristiche. In genere, il flusso multimediale supporta un metodo specifico del formato per la creazione di un esempio più potente rispetto ai metodi **IStreamSample** descritti in questo esempio. **IDirectDrawMediaStream,** ad esempio, può creare esempi collegati a una superficie DirectDraw desiderata e a un rettangolo di ritaglio. In alcune situazioni, tuttavia, è necessario gestire i dati senza conoscerne il formato. Se si vuole trasmettere dati indipendentemente dal formato, usare il metodo **IMediaStream::CreateSharedSample** per creare gli esempi di dati.
5.  Dopo aver creato tutti gli esempi di flusso desiderati, avviare il flusso chiamando il metodo [**IMultiMediaStream::SetState**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate) e passare il flag STREAMSTATE \_ RUN come parametro.
6.  Chiamare [**IStreamSample::Update per**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) aggiornare l'esempio di flusso. Quando il **metodo IStreamSample::Update** viene chiuso, è possibile accedere ai dati dell'esempio. Se si vuole attivare un evento o una chiamata di funzione specifica al termine dell'aggiornamento, passare i puntatori appropriati al **metodo IStreamSample::Update.**

Per altre informazioni sulle interfacce di streaming multimediale, vedere [Streaming multimediale](multimedia-streaming.md).

 

 



