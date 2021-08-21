---
description: Le informazioni sull'intestazione ASF vengono archiviate negli oggetti intestazione ASF di un file multimediale.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Recupero di informazioni da oggetti intestazione ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346e57721137fd6064e4d6b9fd21080d96c10e740bb7f7ed45bf3fef4cc92722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974440"
---
# <a name="getting-information-from-asf-header-objects"></a>Recupero di informazioni da oggetti intestazione ASF

Le informazioni sull'intestazione ASF vengono archiviate negli oggetti intestazione ASF di un file multimediale. Media Foundation fornisce [l'oggetto ContentInfo asf](asf-contentinfo-object.md) da usare con l'oggetto Header. Per consentire all'applicazione di leggere le informazioni di intestazione di un file esistente, è necessario un oggetto ContentInfo popolato. A tale scopo, chiamare [**IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader). Se l'analisi viene completata correttamente, la libreria ASF per il file, gestita internamente da Media Foundation, viene popolata con le informazioni di intestazione di vari oggetti intestazione. Alcune di queste proprietà sono esposte all'applicazione, che può recuperare tramite attributi nel descrittore di presentazione, nel descrittore di flusso, nel profilo e nelle proprietà dei metadati.

Per l'elenco completo degli attributi, vedere [Media Foundation attributi per gli oggetti intestazione ASF.](media-foundation-attributes-for-asf-header-objects.md)

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a>Recupero di informazioni di intestazione da un descrittore di presentazione

Un oggetto descrittore di presentazione contiene la descrizione di una determinata origine multimediale, in questo caso l'origine multimediale ASF. Se la **chiamata ParseHeader** viene completata correttamente, le informazioni a livello di file dell'oggetto Header vengono archiviate come attributi nel descrittore di presentazione. Per creare il descrittore di presentazione, chiamare [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Questo metodo restituisce un puntatore a un oggetto descrittore di presentazione popolato che contiene questi attributi per il file ASF associato all'oggetto ContentInfo. Per ottenere valori per attributi specifici, chiamare i metodi **IMFAttributes::Getxxx** sul descrittore di presentazione e specificare l'attributo **MF \_ PD \_ ASF \_ xxx.**

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



Per altre informazioni sui descrittori di presentazione in generale, vedere [Descrittori di presentazione](presentation-descriptors.md).

Per il set completo di attributi del descrittore di presentazione, vedere [Attributi del descrittore di presentazione](presentation-descriptor-attributes.md).

## <a name="retrieving-header-information-from-a-stream-descriptor"></a>Recupero di informazioni di intestazione da un descrittore di flusso

Un oggetto descrittore di flusso espone [**l'interfaccia IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) e descrive le caratteristiche dei flussi nel file. Il descrittore di presentazione per il contenuto asf contiene uno o più descrittori di flusso che rappresentano i flussi elencati nell'oggetto Intestazione. Al termine della chiamata a [**IMFASFContentInfo::GeneratePresentationDescriptor,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) i descrittori di flusso sottostanti vengono popolati con informazioni a livello di flusso dai vari oggetti Header. Per ottenere un descrittore di flusso per un flusso ASF, chiamare [**IMFPresentationDescriptor::GetStreamDescriptorByIndex sul**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) descrittore di presentazione generato dall'oggetto ContentInfo.

Alcune delle proprietà del flusso vengono impostate come attributi nei descrittori di flusso. Chiamare **i metodi IMFAttributes::Getxxx** su un descrittore di flusso e specificare l'attributo **MF \_ SD \_ ASF \_ xxx.**

Per il set completo di attributi del descrittore di flusso, vedere gli attributi "Descrittore di flusso specifico di ASF" elencati in [Attributi del descrittore di flusso](stream-descriptor-attributes.md).

## <a name="retrieving-header-information-from-the-profile-object"></a>Recupero di informazioni di intestazione dall'oggetto profilo

Oltre ai descrittori di flusso, l'oggetto profilo ASF descrive anche le proprietà del flusso. Per ottenere il profilo di un file ASF esistente, chiamare [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). L'oggetto profilo ASF restituito da questo metodo non include nessuno degli attributi **MF \_ PD \_ ASF \_ xxx.** Questi attributi sono disponibili per l'applicazione solo dopo aver chiamato [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) per generare l'oggetto profilo da un descrittore di presentazione. È possibile usare il profilo per ottenere puntatori agli oggetti di esclusione reciproca e priorità del flusso.

Per informazioni sull'oggetto profilo, vedere [Profilo ASF.](asf-profile.md)

## <a name="retrieving-metadata-from-header-objects"></a>Recupero di metadati da oggetti intestazione

Un file ASF può contenere diverse proprietà di metadati impostate durante la codifica del file. Un'applicazione può enumerare queste proprietà con l'oggetto ContentInfo. Alcune di queste proprietà, ad esempio le informazioni sulla velocità in bit variabile (VBR), sono disponibili per l'applicazione tramite attributi nel descrittore di presentazione, nei descrittori di flusso e nei tipi di supporti per il file multimediale. Questi attributi vengono impostati sull'oggetto ContentInfo durante l'inizializzazione tramite [**la chiamata ParseHeader.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto ContentInfo di ASF](asf-contentinfo-object.md)
</dt> </dl>

 

 



