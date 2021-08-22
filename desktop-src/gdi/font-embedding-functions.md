---
description: Le funzioni seguenti vengono usate con i tipi di carattere Microsoft OpenType incorporati.
ms.assetid: 8f47d7a5-db45-4a41-8af2-9fc6b373a531
title: Funzioni di incorporamento dei tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe820c8b9e6a17f148705599d77ea08bbc4b3f8d52821c171c9e86ca13e2ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761184"
---
# <a name="font-embedding-functions"></a>Funzioni di incorporamento dei tipi di carattere

Le funzioni seguenti vengono usate con i tipi di carattere Microsoft OpenType incorporati.



| Funzione                                                                   | Descrizione                                                                                                                                              |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*CFP \_ ALLOCPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_allocproc)                                      | Funzione di allocazione della memoria fornita dall'applicazione per CreateFontPackage e MergeFontPackage.                                                              |
| [*CFP \_ FREEPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_freeproc)                                        | Funzione di deallocazione della memoria fornita dall'applicazione per CreateFontPackage e MergeFontPackage.                                                            |
| [*CFP \_ REALLOCPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_reallocproc)                                  | Funzione di riallocazione della memoria fornita dall'applicazione per CreateFontPackage e MergeFontPackage.                                                            |
| [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage)                             | Crea una versione più compatta di un tipo di carattere TrueType specificato, per passarla a una stampante. Il tipo di carattere risultante può essere in subset, compresso o entrambi. |
| [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage)                               | Unisce i tipi di carattere di subset creati da CreateFontPackage.                                                                                                        |
| [*READEMBEDPROC*](/previous-versions//dd162894(v=vs.85))                                       | Funzione di callback fornita dal client per leggere il contenuto del flusso da un buffer.                                                                                 |
| [**TTCharToUnicode**](/windows/desktop/api/T2embapi/nf-t2embapi-ttchartounicode)                                 | Converte una matrice di valori di codice carattere a 8 bit in valori Unicode a 16 bit.                                                                               |
| [**TTDeleteEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttdeleteembeddedfont)                       | Rilascia la memoria utilizzata da un tipo di carattere incorporato.                                                                                                                |
| [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)                                         | Crea una struttura del tipo di carattere contenente un tipo di carattere wide in subset (16 bit), usando un contesto di dispositivo come origine delle informazioni di incorporamento del tipo di carattere.           |
| [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex)                                     | Crea una struttura del tipo di carattere contenente il tipo di carattere carattere UCS-4 (32 bit) in subset, usando un contesto di dispositivo come origine delle informazioni di incorporamento del tipo di carattere.        |
| [**TTEmbedFontFromFileA**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea)                       | Crea una struttura del tipo di carattere contenente un tipo di carattere a caratteri wide (16 bit) in subset, usando un file come origine delle informazioni di incorporamento del tipo di carattere.                     |
| [**TTEnableEmbeddingForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttenableembeddingforfacename)       | Aggiunge o rimuove i nomi dei caratteri dall'elenco di esclusione dei caratteri tipografici.                                                                                              |
| [**TTGetEmbeddedFontInfo**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddedfontinfo)                     | Recupera informazioni su un tipo di carattere incorporato.                                                                                                            |
| [**TTGetEmbeddingType**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddingtype)                           | Restituisce i privilegi di incorporamento di un tipo di carattere.                                                                                                                  |
| [**TTGetNewFontName**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetnewfontname)                               | Crea un nuovo nome per un tipo di carattere incorporato installato.                                                                                                       |
| [**TTIsEmbeddingEnabled**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabled)                       | Determina se l'elenco di esclusione dei caratteri tipografici contiene un tipo di carattere specificato.                                                                                     |
| [**TTIsEmbeddingEnabledForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabledforfacename) | Determina se l'incorporamento è abilitato per un tipo di carattere specificato.                                                                                            |
| [**TTLoadEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttloadembeddedfont)                           | Legge il tipo di carattere incorporato dal flusso del documento e lo installa. Consente inoltre a un client di limitare ulteriormente i privilegi di incorporamento del tipo di carattere.             |
| [**TTRunValidationTests**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtests)                       | Convalida i dati di parte o di tutti i glifi di un tipo di carattere a caratteri wide (16 bit), nell'intervallo di dimensioni specificato.                                                         |
| [**TTRunValidationTestsEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtestsex)                   | Versione UCS-4 di TTRunValidationTests.                                                                                                                   |
| [*WRITEEMBEDPROC*](/previous-versions//dd145225(v=vs.85))                                     | Funzione di callback fornita dal client per scrivere il contenuto del flusso in un buffer.                                                                                  |



 

 

 
