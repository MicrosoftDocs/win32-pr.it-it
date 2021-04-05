---
title: Oggetto Metadata Editor
description: Oggetto Metadata Editor
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows Media Format SDK, oggetti dell'editor di metadati
- ASF (Advanced Systems Format), oggetti dell'editor di metadati
- ASF (Advanced Systems Format), oggetti dell'editor di metadati
- oggetti, oggetti dell'editor di metadati
- oggetti dell'editor di metadati, informazioni
- metadati, oggetti Editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724100"
---
# <a name="metadata-editor-object"></a>Oggetto Metadata Editor

L'oggetto dell'editor di metadati viene utilizzato per modificare le informazioni archiviate nella sezione dell'intestazione dei file ASF. Gli elementi più comuni modificati da questo oggetto sono gli attributi dei metadati. Inoltre, l'editor di metadati gestisce i [*marcatori*](wmformat-glossary.md) e i comandi di script. L'unico caso in cui è necessario utilizzare l'editor di metadati è quando si desidera modificare l'intestazione di un file esistente senza riprodurlo.

L'oggetto dell'editor di metadati viene creato dalla funzione [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), che imposta un puntatore a un'interfaccia **IWMMetadataEditor** . Le altre interfacce dell'oggetto dell'editor di metadati possono essere ottenute chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate dall'oggetto dell'editor di metadati.



| Interfaccia                                        | Descrizione                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | Consente di modificare le applicazioni per esaminare le proprietà [*DRM*](wmformat-glossary.md) di un file ASF senza avere alcun diritto di riprodurre il contenuto protetto. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | Modifica gli attributi, i marcatori e i comandi di script nell'intestazione.                                                                                                                                    |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | Recupera le informazioni sul codec. Eredita tutti i metodi di **IWMHeaderInfo**.                                                                                                                         |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | Fornisce supporto avanzato per attributi, inclusi attributi di grandi dimensioni, più linguaggi e nomi di attributi duplicati. Eredita tutti i metodi di **IWMHeaderInfo** e **IWMHeaderInfo2**.      |
| [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | Apre, chiude e salva le modifiche apportate all'intestazione di un file ASF.                                                                                                                                         |
| [**IWMMetadataEditor2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | Apre un file ASF per la modifica dell'intestazione con più opzioni di accesso e condivisione file. Eredita tutti i metodi di **IWMMetadataEditor**.                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Indicatori**](markers.md)
</dt> <dt>

[**Metadati**](metadata.md)
</dt> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Comandi script**](script-commands.md)
</dt> <dt>

[**Utilizzo dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




