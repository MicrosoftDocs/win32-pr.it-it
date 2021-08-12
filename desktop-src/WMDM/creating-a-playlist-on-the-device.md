---
title: Creazione di una playlist nel dispositivo
description: Creazione di una playlist nel dispositivo
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Gestione dispositivi multimediali, playlist
- Gestione dispositivi, playlist
- guida per programmatori, playlist
- applicazioni desktop, playlist
- creazione Windows applicazioni di Gestione dispositivi multimediali,playlist
- playlist astratte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a61d45c234f1cdbe03a713e4d10568fa45c83bdd90227b815c85b0f544d2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585864"
---
# <a name="creating-a-playlist-on-the-device"></a>Creazione di una playlist nel dispositivo

L Windows SDK di Gestione dispositivi multimediali consente a un'applicazione MTP di creare una playlist in un dispositivo. Questo tipo di playlist è detto *playlist* astratta, perché il file creato nel dispositivo non contiene dati multimediali, ma solo metadati, che contengono i collegamenti ai file multimediali nella playlist.

Altri elementi astratti che possono essere creati nel dispositivo includono album (essenzialmente playlist con proprietà aggiuntive come la copertina), contatti e messaggi.

**Per creare una playlist**

1.  Acquisire [**un'interfaccia IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) nel dispositivo di destinazione.
2.  Chiamare [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) per ottenere la proprietà \_ g wszWMDMFormatsSupported.
3.  Se non sono supportati formati di playlist, non consentire l'invio di playlist al dispositivo e ignorare i passaggi seguenti. In caso contrario, scegliere il codice di formato supportato dal dispositivo che corrisponde maggiormente al tipo di oggetto desiderato. I codici di formato WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST e WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST sono i più comunemente supportati.
4.  Ottenere [**un'interfaccia IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) per l'archiviazione (radice o cartella) in cui si vuole creare l'oggetto. Alcuni dispositivi funzionano meglio se l'oggetto playlist viene inserito in una cartella di primo livello denominata "Playlist".
5.  Creare un oggetto metadati vuoto usando [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).
6.  Usando **l'interfaccia IWMDMMetaData** ottenuta nel passaggio precedente, chiamare [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) per aggiungere il codice di formato scelto (dal passaggio 3) alle proprietà dei metadati di archiviazione.
7.  Ottenere [**l'interfaccia IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) **dall'interfaccia IWMDMStorage3.**
8.  Chiamare [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) per inserire un nuovo file di playlist nell'archiviazione selezionata. Questo file contiene i metadati rappresentati **dall'interfaccia IWMDMMetaData** creata nel passaggio 5 e passata a **Insert3.** Il metodo restituisce **un'interfaccia IWMDMStorage** per il file della playlist. è possibile eseguire una query per [**l'interfaccia IWMDMStorage4.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)
9.  Chiamare [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) per creare riferimenti alle interfacce **IWMDMStorage** dei file multimediali nella playlist.

Per codice di esempio, vedere la \_ funzione OnCreatePlaylist [nell'applicazione desktop di esempio](sample-desktop-application.md).

> [!Note]  
> Il provider di servizi MTP fornito da Microsoft consente a un'applicazione di impostare riferimenti nei metadati. Per implementare playlist, l'applicazione deve comunicare con un dispositivo MTP o usare un provider di servizi personalizzato in grado di gestire oggetti astratti. Il provider di servizi CE gestisce gli oggetti playlist e album.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file nel dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




