---
description: Un'applicazione deve essere in grado di produrre e utilizzare dati da più formati.
ms.assetid: bf60fab7-866b-4659-8316-653509ac5112
title: Formati di persistenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8edd88a4b170d2299832a205d80dc6704aea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316819"
---
# <a name="persistence-formats"></a>Formati di persistenza

Un'applicazione deve essere in grado di produrre e utilizzare dati da più formati. Questi includono spesso formati binari proprietari e devono includere anche alcuni formati standard, ad esempio RTF (Rich Text Format) o HTML.

Nella tabella seguente sono elencati alcuni formati che possono contenere input penna.



| Formato                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binary<br/>                           | Per codificare l'input penna nei propri formati binari, le applicazioni devono utilizzare il formato ISF (Ink Serialized Format).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| HTML<br/>                             | È consigliabile usare un formato HTML per la rappresentazione di contenuto eterogeneo. Le applicazioni devono usare la Graphics Interchange Format fortificata (GIF) per codificare l'input penna nei documenti HTML. Per altre informazioni sulle gif fortificate, vedere la pagina relativa ai [blocchi predefiniti](building-blocks.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Immagine<br/>                            | Per le applicazioni per cui non esistono altre intersezioni di compatibilità, un'applicazione abilitata per l'input penna deve spostare negli Appunti le immagini formattate bitmap e metafile.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Ink Serialized Format (ISF)<br/>      | ISF è la rappresentazione permanente più compatta dell'input penna. Anche se contiene spesso solo dati di input penna, ISF è estensibile. Le applicazioni possono impostare attributi personalizzati, identificati da un identificatore univoco globale (GUID), su un oggetto [**Ink**](inkdisp-class.md) , un tratto di input penna o un punto di input penna. In questo modo è possibile archiviare qualsiasi tipo di dati o metadati come attributo in un flusso ISF. Per l'interoperabilità degli Appunti, è possibile inserire l'input penna in uno slot degli Appunti standard per ISF definito nei file di intestazione Software Development Kit (SDK).<br/> ISF è un formato specifico per la tecnologia Microsoft Tablet PC ed è supportato solo nei metodi [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) e [**Save**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save) dell'oggetto [**Ink**](inkdisp-class.md) .<br/> |
| RTF<br/>                              | È possibile generare un formato degli Appunti RTF e codificare l'input penna nel formato RTF come oggetti OLE. Ciò consente di incollare l'input penna in un contenitore OLE, ad esempio Microsoft Word o un'applicazione basata su RichEdit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Extensible Markup Language (XML)<br/> | Le applicazioni possono utilizzare uno dei formati di input penna con codifica base 64 per archiviare l'input penna in un formato di file XML. Un formato XML è utile per l'immissione di contenuto input penna in un database, come nel caso di un campo di firma o anche come formato di file primario di applicazioni. Questa operazione riduce la necessità di scrivere un parser.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

 

 




