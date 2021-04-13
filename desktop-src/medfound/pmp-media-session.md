---
description: .
ms.assetid: CF3A427D-31D2-45FF-BE87-F192B758204E
title: Sessione multimediale PMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0e14d9e403620d273bb4aeb3347cba523f304b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351176"
---
# <a name="pmp-media-session"></a>Sessione multimediale PMP

Un'applicazione può creare la [sessione multimediale](media-session.md) in un processo separato denominato processo PMP ( [Protected Media Path](protected-media-path.md) ). Lo scopo principale del processo PMP è quello di abilitare la riproduzione dei contenuti protetti usando Digital Rights Management (DRM). Per impostazione predefinita, il processo PMP viene creato all'interno di un ambiente protetto (PE). Solo i componenti trusted e firmati possono essere caricati all'interno di un PE. Un vantaggio secondario del processo PMP è che isola il processo dell'applicazione dalla pipeline multimediale. Per ulteriori informazioni sul processo PMP, vedere [percorso multimediale protetto](protected-media-path.md).

Per creare la sessione multimediale all'interno del processo PMP, chiamare la funzione [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) . Facoltativamente, è possibile passare il flag **di \_ \_ processo MFPMPSESSION non protetto** . Se questo flag è impostato, il processo PMP viene creato all'interno di un processo non protetto e non di un processo PE. Il processo non protetto non può essere usato per la riproduzione DRM, ma offre i vantaggi dell'isolamento dei processi.

La funzione [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) restituisce un puntatore a un oggetto proxy per la sessione multimediale. L'applicazione comunica con la sessione multimediale tramite il proxy.

![illustrazione della sessione multimediale all'interno del processo PMP](images/pmp01.png)

Per impostazione predefinita, quando l'applicazione crea una topologia, l'origine multimediale viene creata all'interno del processo dell'applicazione. Un proxy per l'origine multimediale viene creato all'interno del processo PMP. L'origine multimediale può creare oggetti all'interno del processo PMP usando l'interfaccia [**IMFPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) . Per supportare DRM, ad esempio, un'origine multimediale crea un oggetto denominato *autorità di attendibilità di input* (ITA). Il ITA deve essere creato all'interno del processo PMP. Per ulteriori informazioni su ITAs, vedere [percorso multimediale protetto](protected-media-path.md). Per usare l'interfaccia [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) , eseguire le operazioni seguenti:

1.  L'origine multimediale deve implementare l'interfaccia [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient) .
2.  Durante la risoluzione della topologia, il proxy della sessione multimediale chiama il metodo [**IMFPMPClient:: SetPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) sull'origine multimediale.
3.  L'origine multimediale chiama [**IMFPMPHost:: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) per creare l'oggetto all'interno del processo PMP. L'oggetto deve avere un CLSID registrato. Inoltre, per il caricamento all'interno del PE, l'oggetto deve essere attendibile e firmato digitalmente. Per informazioni sui componenti multimediali protetti per la firma del codice, vedere la white paper [firma del codice per i componenti multimediali protetti in Windows Vista](/windows-hardware/test/hlk/)

Nella figura seguente viene illustrata l'origine multimediale creata nel processo dell'applicazione.

![illustrazione di un'origine multimediale nel processo dell'applicazione.](images/pmp02.png)

Un'altra alternativa consiste nel creare l'origine multimediale all'interno della sessione PMP.

1.  Impostare l'attributo [**MF \_ Session \_ Remote \_ source \_ mode**](mf-session-remote-source-mode-attribute.md) quando si crea la sessione multimediale. Gli attributi di configurazione sono specificati nel parametro *pConfiguration* della funzione [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .
2.  Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) nella sessione multimediale per ottenere un puntatore all'interfaccia [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) . L'identificatore del servizio è il **\_ \_ servizio MF PMP**.
3.  Chiamare [**IMFPMPHost:: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) con l'identificatore di classe **CLSID \_ MFSourceResolver** per creare il resolver di origine all'interno del processo PMP. Il metodo restituisce un puntatore a un proxy per il resolver di origine.
4.  Chiamare [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) o [**IMFSourceResolver:: BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) per creare l'origine multimediale.
    > [!Note]  
    > In questo caso, è necessario usare le versioni asincrone di questi metodi, perché le versioni sincrone non sono utilizzabili in remoto.

     

La figura seguente mostra l'origine multimediale creata nel processo PMP.

![illustrazione di un'origine multimediale nel processo PMP.](images/pmp03.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come riprodurre file multimediali protetti](how-to-play-protected-media-files.md)
</dt> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Percorso supporto protetto](protected-media-path.md)
</dt> </dl>

 

 
