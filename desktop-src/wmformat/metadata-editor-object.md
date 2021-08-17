---
title: Oggetto Metadata Editor
description: Oggetto Metadata Editor
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows Media Format SDK, oggetti dell'editor di metadati
- Advanced Systems Format (ASF), oggetti dell'editor di metadati
- ASF (Advanced Systems Format), oggetti editor di metadati
- oggetti, oggetti dell'editor di metadati
- oggetti dell'editor di metadati, informazioni
- metadati,oggetti editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8e78aaf6ada96a9cefa1a9ec6f4aa5708c7382539bc3b75493734c18d600b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027449"
---
# <a name="metadata-editor-object"></a>Oggetto Metadata Editor

L'oggetto editor di metadati viene usato per modificare le informazioni archiviate nella sezione di intestazione dei file ASF. Gli elementi più comuni manipolati da questo oggetto sono gli attributi dei metadati. Inoltre, l'editor di metadati gestisce [*marcatori e*](wmformat-glossary.md) comandi script. L'unica volta che è necessario usare l'editor dei metadati è quando si vuole modificare l'intestazione di un file esistente senza riproducerlo.

L'oggetto editor di metadati viene creato dalla funzione [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), che imposta un puntatore a **un'interfaccia IWMMetadataEditor.** Le altre interfacce dell'oggetto editor di metadati possono essere ottenute chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate dall'oggetto editor di metadati.



| Interfaccia                                        | Descrizione                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | Consente alle applicazioni di modifica di esaminare [*le proprietà DRM*](wmformat-glossary.md) di un file ASF senza avere diritti per riprodurre il contenuto protetto. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | Modifica attributi, marcatori e comandi script nell'intestazione.                                                                                                                                    |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | Recupera le informazioni sul codec. Eredita tutti i metodi di **IWMHeaderInfo.**                                                                                                                         |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | Fornisce supporto avanzato per gli attributi, inclusi attributi di grandi dimensioni, più linguaggi e nomi di attributi duplicati. Eredita tutti i metodi di **IWMHeaderInfo** e **IWMHeaderInfo2.**      |
| [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | Apre, chiude e salva le modifiche apportate all'intestazione di un file ASF.                                                                                                                                         |
| [**IWMMetadataEditor2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | Apre un file ASF per la modifica dell'intestazione con più opzioni di condivisione e accesso ai file. Eredita tutti i metodi di **IWMMetadataEditor.**                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Marcatori**](markers.md)
</dt> <dt>

[**Metadati**](metadata.md)
</dt> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Comandi script**](script-commands.md)
</dt> <dt>

[**Uso dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




