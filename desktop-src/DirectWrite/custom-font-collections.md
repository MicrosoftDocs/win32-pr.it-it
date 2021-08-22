---
title: Raccolte di tipi di carattere personalizzati (Windows 7/8)
description: DirectWrite l'accesso alla raccolta di tipi di carattere di sistema tramite il metodo IDWriteFactory GetSystemFontCollection.
ms.assetid: ec892904-6778-4fbd-93b4-62d0db5b82ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc76214dda067b43c27c8e04e4419f147d0e33b7566b4dedc5ac3255a1c1dc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290761"
---
# <a name="custom-font-collections-windows-78"></a>Raccolte di tipi di carattere personalizzati (Windows 7/8)

[DirectWrite](direct-write-portal.md) l'accesso alla raccolta di tipi di carattere di sistema usando il [**metodo IDWriteFactory::GetSystemFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) Si tratta della raccolta di tipi di carattere usata più di frequente. Tuttavia, alcune applicazioni devono usare tipi di carattere non installati nel sistema, ad esempio da file dei tipi di carattere inclusi o file dei tipi di carattere incorporati nell'applicazione.

Se i tipi di carattere desiderati non sono presenti nella raccolta di tipi di carattere di sistema, è possibile creare una raccolta di tipi di carattere personalizzata derivata da [**IDWriteFontCollection.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)

Questa panoramica è costituita dalle parti seguenti:

-   [Registrazione e annullamento della registrazione di un caricatore di raccolta di tipi di carattere](#registering-and-unregistering-a-font-collection-loader)
-   [IDWriteFontCollectionLoader](#idwritefontcollectionloader)
-   [IDWriteFontFileEnumerator](#idwritefontfileenumerator)
-   [CreateCustomFontFileReference](#createcustomfontfilereference)
-   [IDWriteFontFileLoader](#idwritefontfileloader)
-   [IDWriteFontFileStream](#idwritefontfilestream)

## <a name="registering-and-unregistering-a-font-collection-loader"></a>Registrazione e annullamento della registrazione di un caricatore di raccolta di tipi di carattere

Per registrare un caricatore della raccolta di tipi di carattere, usare il metodo [**IDWriteFactory::RegisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader) e passarvi [**un'interfaccia IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implementata dall'applicazione come oggetto singleton. Questo oggetto carica i tipi di carattere quando viene richiesta la raccolta personalizzata. Sia la raccolta di tipi di carattere di sistema che le raccolte di tipi di carattere personalizzati vengono memorizzate nella cache, quindi i tipi di carattere vengono caricati una sola volta.

Il caricatore della raccolta di tipi di carattere deve essere scaricato alla fine usando [**IDWriteFactory::UnregisterFontCollectionLoader.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader)

> [!Note]  
> La registrazione del caricatore della raccolta di tipi di carattere aggiunge al conteggio dei riferimenti. non chiamare [**UnregisterFontCollectionLoader dall'interno**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader) del distruttore oppure la registrazione dell'oggetto caricatore di raccolta non verrà mai annullata.

 

## <a name="idwritefontcollectionloader"></a>IDWriteFontCollectionLoader

Per creare un [**oggetto IDWriteFontFileEnumerator,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) usare [**IDWriteFactory::CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) e passarvi una chiave definita dall'applicazione. La chiave è un puntatore void e il tipo di dati, il formato e il significato sono definiti dall'applicazione e sono opachi per il sistema di tipi di carattere.

Mentre la chiave può essere qualsiasi elemento, [DirectWrite](direct-write-portal.md) che ogni chiave sia:

-   Univoco per una singola raccolta di tipi di carattere all'interno dell'ambito del caricatore.
-   Valido fino a quando non viene annullata la registrazione del caricatore usando la factory.

Quando viene chiamato il metodo [**CreateCustomFontCollection,**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) DirectWrite richiama [un'interfaccia](direct-write-portal.md) [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implementata come oggetto singleton dall'applicazione. Il metodo di callback [**IDWriteFontCollectionLoader::CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) viene usato da DirectWrite per recuperare un oggetto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) implementato dall'applicazione. [**L'oggetto IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) usato per creare la raccolta viene passato a questo metodo e deve essere usato dall'enumeratore del file del tipo di carattere per creare gli oggetti [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) da includere nella raccolta.

La chiave passata a questo metodo identifica la raccolta di tipi di carattere ed è la stessa chiave passata [**a CreateCustomFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection)

## <a name="idwritefontfileenumerator"></a>IDWriteFontFileEnumerator

L'oggetto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) definito dall'applicazione creato dal metodo [**CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) viene usato per enumerare i file dei tipi di carattere in una raccolta, creando un oggetto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) per ogni file. Il [**metodo IDWriteFontFileEnumerator::MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) modifica la posizione del file del tipo di carattere successivo. Se è presente un file nella posizione , imposta *hasCurrentFile* su **TRUE.** In caso contrario, verrà impostato su **FALSE** e il metodo restituirà **S \_ OK.**

> [!Note]  
> L'enumeratore del file del tipo di carattere deve iniziare posizionato prima del primo elemento ed essere avanzato alla prima chiamata a [**MoveNext.**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext)

 

Un [**oggetto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) viene restituito dal [**metodo IDWriteFontFileEnumerator::GetCurrentFontFile.**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) Se non è presente alcun file del tipo di carattere nella posizione corrente, perché [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) non è stato ancora chiamato o hasCurrentFile è stato impostato su **FALSE,** **GetCurrentFontFile** restituirà **E \_ FAIL**.

## <a name="createcustomfontfilereference"></a>CreateCustomFontFileReference

[**L'output dell'oggetto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) [**di GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) può essere creato chiamando [**IDWriteFactory::CreateCustomFontFileReference.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) La chiave di riferimento del file del tipo di carattere identifica un riferimento al file del tipo di carattere specifico e deve essere univoca all'interno del caricatore del file del tipo di carattere che carica il file.

## <a name="idwritefontfileloader"></a>IDWriteFontFileLoader

Il [**metodo CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) accetta un [**oggetto IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) implementato dall'applicazione usata per caricare il tipo di carattere. Al metodo di callback [**IDWriteFontFileLoader::CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) viene passata la chiave e viene restituito un [**oggetto IDWriteFontFileStream.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)

## <a name="idwritefontfilestream"></a>IDWriteFontFileStream

L'oggetto [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) implementato dall'applicazione fornisce i dati del file del tipo di carattere per un riferimento al file del tipo di carattere da un caricatore di file del tipo di carattere personalizzato. Insieme alle dimensioni del file e all'ora dell'ultima scrittura, fornisce un metodo ([**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)) per il recupero di frammenti di file da compilare in un [**oggetto IDWriteFontFile.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)

> [!Note]  
> [**Le implementazioni readFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment) devono restituire un errore se il frammento richiesto non rientra nei limiti del file.

 

[**IDWriteFontFileStream può**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) ottenere il contenuto del file del tipo di carattere da qualsiasi posizione, ad esempio l'unità disco rigido locale o le risorse incorporate.

 

 