---
description: Questo argomento descrive i dettagli interni del modo in cui il sistema di risoluzione di origine crea un'origine multimediale.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Gestori di schemi e Byte-Stream di schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5cbb2ee0af93e456e86b6eab16ff44705f5380
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881774"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a>Gestori di schemi e Byte-Stream di schema

Questo argomento descrive i dettagli interni del modo in cui il sistema di risoluzione di origine crea un'origine multimediale. Leggere questo argomento se si implementa un'origine multimediale personalizzata per Media Foundation e si vuole che l'origine multimediale sia disponibile per le applicazioni tramite il sistema di risoluzione di origine.

Il sistema di risoluzione di origine può creare un'origine multimediale da un URL o da un flusso di byte, ovvero un [**puntatore IMFByteStream.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) A tale scopo, usa oggetti helper denominati *gestori*. Per gli URL, il sistema di risoluzione di origine usa *i gestori di schemi*. Per i flussi di byte, usa gestori *di flussi di byte*.

Un gestore di schema accetta un URL come input e crea un'origine multimediale o un flusso di byte. Se crea un flusso di byte, il sistema di risoluzione di origine lo passerà a un gestore del flusso di byte, che crea l'origine multimediale. L'immagine seguente illustra questo processo.

![Diagramma che mostra il processo di risoluzione dell'origine](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>Gestori di schemi

I gestori di schema vengono usati quando l'applicazione chiama [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) o il relativo equivalente [**asincrono, BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).

Il sistema di risoluzione di origine cerca i gestori di schemi nel Registro di sistema. I gestori di schema sono elencati in base a uno schema URL, nelle chiavi seguenti:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

dove *&lt; schema &gt;* è lo schema URL che il gestore è progettato per l'analisi. Lo schema include il carattere ':' finale. ad esempio "http:".

Per registrare un nuovo gestore di schema, aggiungere una voce il cui nome è il CLSID del gestore dello schema, in formato stringa canonica: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Il valore della voce è una stringa (REG SZ) contenente una breve descrizione del gestore, ad esempio \_ "My Scheme Handler". La parte importante della voce è il CLSID. Il sistema di risoluzione di origine crea il gestore chiamando **CoCreateInstance** con questo CLSID.

I gestori di schema espongono [**l'interfaccia IMFSchemeHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) Se il sistema di risoluzione di origine trova un gestore di schema che corrisponde a quello dello schema URL, il sistema di risoluzione di origine chiama [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passando l'URL originale. Il gestore dello schema aprirà l'URL e tenterà di analizzare il contenuto. A questo punto, il gestore dello schema ha due opzioni:

-   Creare un'origine multimediale.
-   Creare un flusso di byte.

Se crea un'origine multimediale, il sistema di risoluzione di origine restituisce l'origine multimediale all'applicazione. Se crea un flusso di byte, il sistema di risoluzione di origine tenta di trovare un gestore del flusso di byte appropriato, come descritto nella sezione successiva.

## <a name="byte-stream-handlers"></a>Byte-Stream gestori

I gestori del flusso di byte vengono usati quando l'applicazione chiama [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) o il relativo equivalente asincrono, [**BeginCreateObjectFromByteStream.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) Vengono usati anche quando un gestore dello schema restituisce un flusso di byte, come descritto in precedenza.

Come per i gestori di schemi, i gestori di flussi di byte sono elencati nel Registro di sistema. Sono elencati in base all'estensione del nome file o al tipo MIME (o a entrambi), nelle chiavi seguenti:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

dove *&lt; ExtensionOrMimeType &gt;* è l'estensione del nome file o il tipo MIME. Le estensioni di file includono il carattere iniziale '.'. ad esempio ".wmv".

L'estensione del nome file fa parte dell'URL fornito dall'applicazione. Il tipo MIME potrebbe essere disponibile tramite [**l'attributo \_ MF BYTESTREAM \_ CONTENT \_ TYPE**](mf-bytestream-content-type-attribute.md) nel flusso di byte.

Per registrare un nuovo gestore del flusso di byte, aggiungere una voce il cui nome è il CLSID del gestore, in formato stringa canonico. Il valore della voce è una stringa (REG SZ) contenente una breve descrizione del gestore, ad esempio \_ "My Byte-Stream Handler". Il sistema di risoluzione di origine **chiama CoCreateInstance** per creare il gestore dal CLSID. È possibile registrare lo stesso gestore in più estensioni o tipi MIME.

I gestori di flussi di byte espongono [**l'interfaccia IMFByteStreamHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) Se il sistema di risoluzione di origine trova un gestore del flusso di byte corrispondente, chiama [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). L'input per questo metodo è un puntatore al flusso di byte, oltre all'URL originale, se disponibile. Il gestore del flusso di byte legge dal flusso di byte fino a quando non analizza dati sufficienti per creare l'origine multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 



