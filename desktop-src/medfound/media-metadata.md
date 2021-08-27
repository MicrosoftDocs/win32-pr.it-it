---
description: Metadati multimediali
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Metadati multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef9f8a852bbce2dfb8d38a5883acc219cde8019
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477086"
---
# <a name="media-metadata"></a>Metadati multimediali

I file multimediali contengono proprietà che descrivono il contenuto del file. In Microsoft Media Foundation, queste proprietà possono essere categorizzate nel modo seguente:

-   **Gli attributi di tipo multimediale** specificano i parametri di codifica, ad esempio l'algoritmo di codifica (sottotipo multimediale), le dimensioni dei fotogrammi video, la frequenza dei fotogrammi video, la velocità in bit audio e la frequenza di campionamento audio. Per altre informazioni sugli attributi del tipo di supporto, vedere [Tipi di supporti.](media-types.md)
-   **I** metadati contengono informazioni descrittive per il contenuto multimediale, ad esempio titolo, artista, compositore e genere. I metadati possono anche descrivere i parametri di codifica. L'accesso a queste informazioni tramite i metadati può essere più veloce rispetto agli attributi del tipo di supporto.
-   **Le proprietà DRM** contengono informazioni sulle restrizioni di utilizzo. Attualmente Media Foundation non supporta le proprietà DRM tramite metadati, ad eccezione della proprietà **\_ \_ IsProtected DRM PKEY.**

Esistono due modi per leggere i metadati in Media Foundation:

-   [**L'interfaccia IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (Media Foundation metadati della versione 1).
-   Interfaccia Windows [**shell IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) (metadati della shell).

I metadati della shell riguardano non solo i file multimediali, ma anche una gamma molto più ampia di file nel sistema.

La tabella seguente confronta le funzionalità e le limitazioni di ogni API dei metadati.




| metadati Media Foundation v1 | Metadati della shell | 
|------------------------------|----------------|
| Richiede Windows Vista o versione successiva. | Richiede Windows 7.<blockquote>[!Note]<br />I metadati della shell in generale non richiedono Windows 7, ma Media Foundation non supportano i metadati della shell prima Windows 7.</blockquote><br /> | 
| Le proprietà non sono compatibili con il sistema di proprietà shell. | Le proprietà sono compatibili con il sistema di proprietà shell. | 
| Le proprietà possono essere applicate all'intero file o a livello di flusso. | Sono supportate solo le proprietà a livello di file. Le proprietà a livello di flusso non sono supportate. | 
| Le proprietà possono avere valori in più lingue. | I valori in più lingue non sono supportati. | 
| Le chiavi di proprietà sono stringhe a caratteri wide. | Le chiavi di proprietà <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>sono valori PROPERTYKEY.</strong></a> | 
| I valori delle proprietà <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>sono valori PROPVARIANT.</strong></a> | I valori delle proprietà <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>sono valori PROPVARIANT.</strong></a> | 




 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Provider di metadati della shell](shell-metadata-providers.md)<br/>                       | A partire Windows 7, Media Foundation i metadati tramite [**l'interfaccia IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)<br/> |
| [Proprietà dei metadati dei file multimediali](metadata-properties-for-media-files.md)<br/> | In questo argomento vengono elencate le proprietà dei metadati più comuni per i file multimediali.<br/>                                                           |
| [Provider di metadati in Windows Vista](metadata-providers-in-windows-vista.md)<br/> | In Windows Vista, Media Foundation i metadati tramite [**l'interfaccia IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)<br/>                   |



 

Se si implementa un'origine multimediale personalizzata e si vogliono esporre i metadati della shell, vedere [Provider di metadati personalizzati per file multimediali.](custom-metadata-providers-for-media-files.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation per programmatori](media-foundation-programming-guide.md)
</dt> </dl>

 

 
