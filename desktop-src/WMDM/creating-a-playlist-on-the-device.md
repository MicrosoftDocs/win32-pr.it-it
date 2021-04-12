---
title: Creazione di una playlist nel dispositivo
description: Creazione di una playlist nel dispositivo
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Media Gestione dispositivi, playlist
- Gestione dispositivi, playlist
- Guida per programmatori, playlist
- applicazioni desktop, playlist
- creazione di applicazioni Windows Media Gestione dispositivi, playlist
- playlist astratte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329463"
---
# <a name="creating-a-playlist-on-the-device"></a>Creazione di una playlist nel dispositivo

Windows Media Gestione dispositivi SDK fornisce i mezzi per un'applicazione MTP per la creazione di una playlist in un dispositivo. Questo tipo di playlist è denominato playlist *astratta* , perché il file creato nel dispositivo non contiene dati multimediali, ma solo i metadati, che contengono i collegamenti ai file multimediali nella playlist.

Altri elementi astratti che possono essere creati nel dispositivo includono album (essenzialmente playlist con proprietà aggiuntive, ad esempio copertina), contatti e messaggi.

**Per creare una playlist**

1.  Acquisire un'interfaccia [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) al dispositivo di destinazione.
2.  Chiamare [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) per ottenere la \_ Proprietà g wszWMDMFormatsSupported.
3.  Se non sono supportati formati della playlist, non consentire l'invio di playlist al dispositivo e ignorare i passaggi seguenti. In caso contrario, scegliere il codice del formato supportato dal dispositivo che corrisponde maggiormente al tipo di oggetto previsto. I codici di \_ formato WMDM FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST e WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST sono i più comunemente supportati.
4.  Ottenere un'interfaccia [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) per l'archiviazione (la radice o una cartella) in cui si desidera creare l'oggetto. Alcuni dispositivi funzionano meglio se l'oggetto playlist viene inserito in una cartella di livello superiore denominata "playlists".
5.  Creare un oggetto di metadati vuoto usando [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).
6.  Utilizzando l'interfaccia **IWMDMMetaData** ottenuta nel passaggio precedente, chiamare [**IWMDMMetaData:: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) per aggiungere il codice di formato scelto (dal passaggio 3) alle proprietà dei metadati di archiviazione.
7.  Ottenere l'interfaccia [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) dall'interfaccia **IWMDMStorage3** .
8.  Chiamare [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) per inserire un nuovo file della playlist nello spazio di archiviazione selezionato. Questo file contiene i metadati rappresentati dall'interfaccia **IWMDMMetaData** creata nel passaggio 5 e passati a **Insert3**. Il metodo restituisce un'interfaccia **IWMDMStorage** per il file della playlist; è possibile eseguire una query per l'interfaccia [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) .
9.  Chiamare [**IWMDMStorage4:: Sereferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) per creare riferimenti alle interfacce **IWMDMStorage** dei file multimediali nella playlist.

Per un esempio di codice, vedere la \_ funzione OnCreatePlaylist nell' [applicazione desktop di esempio](sample-desktop-application.md).

> [!Note]  
> Il provider di servizi MTP fornito da Microsoft consente a un'applicazione di impostare riferimenti nei metadati. Per implementare le playlist, l'applicazione deve comunicare con un dispositivo MTP o usare un provider di servizi personalizzato in grado di gestire gli oggetti astratti. Il provider di servizi CE gestisce gli oggetti playlist e album.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file nel dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




