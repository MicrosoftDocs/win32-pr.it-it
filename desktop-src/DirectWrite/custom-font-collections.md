---
title: Raccolte di tipi di carattere personalizzati (Windows 7/8)
description: DirectWrite consente di accedere alla raccolta dei tipi di carattere del sistema tramite il metodo GetSystemFontCollection di IDWriteFactory archiviata nei.
ms.assetid: ec892904-6778-4fbd-93b4-62d0db5b82ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa764330f27b72051ef682c6ce5f1176c42c7d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728682"
---
# <a name="custom-font-collections-windows-78"></a>Raccolte di tipi di carattere personalizzati (Windows 7/8)

[DirectWrite](direct-write-portal.md) consente di accedere alla raccolta dei tipi di carattere del sistema tramite il metodo [**IDWriteFactory archiviata nei:: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Si tratta della raccolta di tipi di carattere utilizzata più di frequente. Tuttavia, alcune applicazioni devono usare i tipi di carattere non installati nel sistema, ad esempio i file del tipo di carattere o i file dei tipi di carattere incorporati nell'applicazione.

Se i tipi di carattere desiderati non sono inclusi nella raccolta di tipi di carattere del sistema, è possibile creare una raccolta di tipi di carattere personalizzata derivata da [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection).

Questa panoramica è costituita dalle parti seguenti:

-   [Registrazione e annullamento della registrazione di un caricatore della raccolta dei tipi di carattere](#registering-and-unregistering-a-font-collection-loader)
-   [IDWriteFontCollectionLoader](#idwritefontcollectionloader)
-   [IDWriteFontFileEnumerator](#idwritefontfileenumerator)
-   [CreateCustomFontFileReference](#createcustomfontfilereference)
-   [IDWriteFontFileLoader](#idwritefontfileloader)
-   [IDWriteFontFileStream](#idwritefontfilestream)

## <a name="registering-and-unregistering-a-font-collection-loader"></a>Registrazione e annullamento della registrazione di un caricatore della raccolta dei tipi di carattere

Per registrare un caricatore della raccolta di tipi di carattere, usare il metodo [**IDWriteFactory archiviata nei:: RegisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader) e passargli un'interfaccia [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implementata dall'applicazione come oggetto singleton. Questo oggetto caricherà i tipi di carattere quando viene richiesta la raccolta personalizzata. La raccolta di tipi di carattere del sistema e le raccolte di tipi di carattere personalizzati vengono memorizzate nella cache, quindi i tipi di carattere vengono caricati una sola

Il caricatore della raccolta dei tipi di carattere deve essere scaricato alla fine usando [**IDWriteFactory archiviata nei:: UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader).

> [!Note]  
> La registrazione del caricatore della raccolta dei tipi di carattere aggiunge al conteggio dei riferimenti. non chiamare [**UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader) dall'interno del distruttore o non verrà mai annullata la registrazione dell'oggetto caricatore della raccolta.

 

## <a name="idwritefontcollectionloader"></a>IDWriteFontCollectionLoader

Per creare un oggetto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) , usare [**IDWriteFactory archiviata nei:: CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) e passargli una chiave definita dall'applicazione. La chiave è un puntatore void e il tipo di dati, il formato e il significato sono definiti dall'applicazione e sono opachi per il sistema di tipi di carattere.

Mentre la chiave può essere qualsiasi, [DirectWrite](direct-write-portal.md) richiede che ogni chiave sia:

-   Univoco per una singola raccolta di tipi di carattere nell'ambito del caricatore.
-   Valido fino a quando non viene annullata la registrazione del caricatore tramite la factory.

Quando viene chiamato il metodo [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) , [DirectWrite](direct-write-portal.md) richiama un'interfaccia [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implementata come oggetto Singleton dall'applicazione. Il metodo di callback [**IDWriteFontCollectionLoader:: CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) viene usato da DirectWrite per recuperare un oggetto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) implementato dall'applicazione. L'oggetto [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) utilizzato per creare la raccolta viene passato a questo metodo e deve essere utilizzato dall'enumeratore del file del tipo di carattere per creare gli oggetti [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) da includere nella raccolta.

La chiave passata a questo metodo identifica la raccolta di tipi di carattere ed è la stessa chiave passata a [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection).

## <a name="idwritefontfileenumerator"></a>IDWriteFontFileEnumerator

L'oggetto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) definito dall'applicazione creato dal metodo [**CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) viene usato per enumerare i file del tipo di carattere in una raccolta, creando un oggetto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) per ogni file. Il metodo [**IDWriteFontFileEnumerator:: MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) modifica la posizione nel file del tipo di carattere successivo. Se è presente un file nella posizione, il *hasCurrentFile* verrà impostato su **true**. In caso contrario, verrà impostato su **false** e il metodo restituirà **S \_ OK**.

> [!Note]  
> L'enumeratore del file del tipo di carattere deve iniziare a posizionarsi prima del primo elemento ed essere avanzato in corrispondenza della prima chiamata a [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext).

 

Un oggetto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) viene restituito dal metodo [**IDWriteFontFileEnumerator:: GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) . Se non è presente alcun file del tipo di carattere nella posizione corrente, perché [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) non è ancora stato chiamato o hasCurrentFile è stato impostato su **false**, **GetCurrentFontFile** restituirà **E avrà \_ esito negativo**.

## <a name="createcustomfontfilereference"></a>CreateCustomFontFileReference

È possibile creare l'oggetto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) restituito da [**GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) chiamando [**IDWriteFactory archiviata nei:: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference). La chiave di riferimento del file del tipo di carattere identifica un riferimento a un file del tipo di carattere specifico e deve essere univoco all'interno del caricatore di file del tipo di carattere che caricherà

## <a name="idwritefontfileloader"></a>IDWriteFontFileLoader

Il metodo [**CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) accetta un oggetto [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) implementato dall'applicazione utilizzata per caricare il tipo di carattere. Al metodo di callback [**IDWriteFontFileLoader:: CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) viene passata la chiave e viene restituito un oggetto [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) .

## <a name="idwritefontfilestream"></a>IDWriteFontFileStream

L'oggetto [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) implementato dall'applicazione fornisce i dati del file del tipo di carattere per un riferimento al file del tipo di carattere da un caricatore di file del tipo di carattere Insieme alla dimensione del file e all'ora dell'ultima scrittura, fornisce un metodo ([**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)) per il recupero dei frammenti di file che devono essere compilati in un oggetto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) .

> [!Note]  
> Le implementazioni [**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment) devono restituire un errore se il frammento richiesto non rientra nei limiti del file.

 

Un [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) può ottenere il contenuto del file del tipo di carattere da qualsiasi posizione, ad esempio l'unità disco rigido locale o le risorse incorporate.

 

 