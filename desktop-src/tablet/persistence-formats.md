---
description: Un'applicazione deve essere in grado di produrre e utilizzare dati da più formati.
ms.assetid: bf60fab7-866b-4659-8316-653509ac5112
title: Formati di persistenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1853dc316d25395a30a15b02734ea4b7ed901b92379e04faa42f5abe5e768af5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596641"
---
# <a name="persistence-formats"></a>Formati di persistenza

Un'applicazione deve essere in grado di produrre e utilizzare dati da più formati. Questi includono spesso formati binari proprietari e devono includere anche alcuni formati standard, ad esempio RTF (Rich Text Format) o HTML.

Nella tabella seguente sono elencati alcuni formati che possono contenere input penna.



| Formato                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binary<br/>                           | Le applicazioni devono usare il formato ISF (Ink Serialized Format) per codificare l'input penna nei formati binari.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| HTML<br/>                             | Un formato HTML è altamente consigliato per la rappresentazione di contenuto eterogeneo. Le applicazioni devono usare Graphics Interchange Format (GIF) per codificare l'input penna nei documenti HTML. Per altre informazioni sulle GIF fortificate, vedere [Blocchi predefiniti.](building-blocks.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Immagine<br/>                            | Per le applicazioni per le quali non sono presenti altre intersezioni di compatibilità, un'applicazione abilitata per l'input penna deve spostare immagini bitmap e metafile formattate negli Appunti.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Ink Serialized Format (ISF)<br/>      | ISF è la rappresentazione permanente più compatta dell'input penna. Sebbene contenga spesso solo dati di input penna, ISF è estendibile. Le applicazioni possono impostare attributi personalizzati (identificati da un identificatore univoco globale (GUID) su un [**oggetto Ink,**](inkdisp-class.md) un tratto input penna o un punto input penna. In questo modo è possibile archiviare qualsiasi tipo di dati o metadati come attributo in un flusso ISF. Per l'interoperabilità degli Appunti, l'input penna può essere inserito in uno slot degli Appunti standard per ISF definito nei file di intestazione del Software Development Kit (SDK).<br/> ISF è un formato specifico della tecnologia Microsoft Tablet [](inkdisp-class.md) PC ed è supportato solo nei metodi [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) e [**Save**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save) dell'oggetto Ink.<br/> |
| RTF<br/>                              | È possibile generare un formato DEGLI Appunti RTF e codificare l'input penna nel formato RTF come oggetti OLE. Ciò consente di incollare l'input penna in un contenitore OLE, ad esempio Microsoft Word un'applicazione basata su RichEdit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Extensible Markup Language (XML)<br/> | Le applicazioni possono usare uno dei formati di input penna codificati in base 64 per archiviare l'input penna in un formato di file XML. Un formato XML è utile per l'immissione di contenuto input penna in un database, come nel caso di un campo di firma o anche come formato di file primario delle applicazioni. In questo modo si attenua la necessità di scrivere un parser.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

 

 




