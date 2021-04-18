---
description: Le informazioni di intestazione ASF vengono archiviate negli oggetti intestazione ASF di un file multimediale.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Recupero di informazioni da oggetti Header ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25155929c9e3ba7e59ee1b5f46ea7c5930c3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305372"
---
# <a name="getting-information-from-asf-header-objects"></a>Recupero di informazioni da oggetti Header ASF

Le informazioni di intestazione ASF vengono archiviate negli oggetti intestazione ASF di un file multimediale. Media Foundation fornisce l' [oggetto ContentInfo ASF](asf-contentinfo-object.md) da usare con l'oggetto intestazione. Un oggetto ContentInfo popolato è necessario affinché l'applicazione legga le informazioni di intestazione di un file esistente. Questa operazione viene eseguita chiamando [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader). Se l'analisi viene completata correttamente, la libreria ASF per il file, gestita internamente da Media Foundation, viene popolata con le informazioni di intestazione di diversi oggetti intestazione. Alcune di queste proprietà sono esposte all'applicazione, che è possibile recuperare tramite gli attributi sul descrittore della presentazione, il descrittore del flusso, il profilo e le proprietà dei metadati.

Per l'elenco completo degli attributi, vedere [Media Foundation attributi per gli oggetti intestazione ASF](media-foundation-attributes-for-asf-header-objects.md).

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a>Recupero delle informazioni di intestazione da un descrittore di presentazione

Un oggetto descrittore di presentazione contiene la descrizione di una particolare origine multimediale, in questo caso l'origine del supporto ASF. Se la chiamata **ParseHeader** viene completata correttamente, le informazioni a livello di file dell'oggetto Header vengono archiviate come attributi nel descrittore di presentazione. Per creare il descrittore della presentazione, chiamare [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Questo metodo restituisce un puntatore a un oggetto descrittore di presentazione popolato contenente questi attributi per il file ASF associato all'oggetto ContentInfo. Per ottenere i valori per attributi specifici, chiamare i metodi **IMFAttributes:: GetXXX** sul descrittore della presentazione e specificare l'attributo **MF \_ PD \_ ASF \_ xxx** .

Il codice di esempio seguente recupera la durata di riproduzione di un file ASF, specificato da un oggetto ContentInfo.


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



Per ulteriori informazioni sui descrittori di presentazione in generale, vedere [descrittori di presentazione](presentation-descriptors.md).

Per il set completo di attributi del descrittore di presentazione, vedere [attributi](presentation-descriptor-attributes.md)del descrittore della presentazione.

## <a name="retrieving-header-information-from-a-stream-descriptor"></a>Recupero delle informazioni di intestazione da un descrittore di flusso

Un oggetto descrittore di flusso espone l'interfaccia [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) e descrive le caratteristiche dei flussi nel file. Il descrittore di presentazione per il contenuto ASF contiene uno o più descrittori di flusso che rappresentano i flussi elencati nell'oggetto intestazione. Dopo che la chiamata a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) è stata completata correttamente, i descrittori di flusso sottostanti vengono popolati con informazioni a livello di flusso dai vari oggetti intestazione. Per ottenere un descrittore di flusso per un flusso ASF, chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) sul descrittore della presentazione generato dall'oggetto ContentInfo.

Alcune delle proprietà del flusso sono impostate come attributi nei descrittori di flusso. Chiamare i metodi **IMFAttributes:: GetXXX** in un descrittore di flusso e specificare l'attributo **MF \_ SD \_ ASF \_ xxx** .

Per il set completo di attributi del descrittore di flusso, vedere gli attributi "descrittore di flusso specifico di ASF" elencati negli [attributi del descrittore di flusso](stream-descriptor-attributes.md)

## <a name="retrieving-header-information-from-the-profile-object"></a>Recupero delle informazioni di intestazione dall'oggetto profilo

Oltre ai descrittori di flusso, l'oggetto profilo ASF descrive anche le proprietà del flusso. Per ottenere il profilo di un file ASF esistente, chiamare [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). L'oggetto profilo ASF restituito da questo metodo non include gli attributi **MF \_ PD \_ ASF \_ xxx** . Questi attributi sono disponibili per l'applicazione solo dopo la chiamata a [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) per generare l'oggetto profilo da un descrittore di presentazione. È possibile usare il profilo per ottenere i puntatori agli oggetti di esclusione reciproca e di assegnazione delle priorità dei flussi.

Per informazioni sull'oggetto profilo, vedere [profilo ASF](asf-profile.md) .

## <a name="retrieving-metadata-from-header-objects"></a>Recupero di metadati da oggetti Header

Un file ASF può contenere diverse proprietà dei metadati impostate durante la codifica dei file. Un'applicazione può enumerare queste proprietà con l'oggetto ContentInfo. Alcune di queste proprietà, ad esempio le informazioni sulla velocità in bit variabile (VBR), sono disponibili per l'applicazione tramite attributi per il descrittore di presentazione, i descrittori di flusso e i tipi di supporto per il file multimediale. Questi attributi vengono impostati nell'oggetto ContentInfo durante l'inizializzazione tramite la chiamata [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto ContentInfo ASF](asf-contentinfo-object.md)
</dt> </dl>

 

 



