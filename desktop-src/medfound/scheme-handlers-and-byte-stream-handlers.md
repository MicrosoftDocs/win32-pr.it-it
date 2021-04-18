---
description: Questo argomento descrive i dettagli interni sul modo in cui il resolver di origine crea un'origine multimediale.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Gestori di schemi e gestori di Byte-Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54976f45c7f07e12b6f095297231d306d0644704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309010"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a>Gestori di schemi e gestori di Byte-Stream

Questo argomento descrive i dettagli interni sul modo in cui il resolver di origine crea un'origine multimediale. Leggere questo argomento se si sta implementando un'origine multimediale personalizzata per Media Foundation e si vuole che l'origine del supporto sia disponibile per le applicazioni tramite il resolver di origine.

Il resolver di origine può creare un'origine multimediale da un URL o da un flusso di byte (ovvero un puntatore [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) ). A tale scopo, vengono utilizzati gli oggetti di supporto chiamati *gestori*. Per gli URL, il resolver di origine usa i *gestori dello schema*. Per i flussi di byte, USA i *gestori del flusso di byte*.

Un gestore dello schema accetta come input un URL e crea un'origine multimediale o un flusso di byte. Se viene creato un flusso di byte, il resolver di origine lo passerà a un gestore del flusso di byte, che consente di creare l'origine multimediale. Questo processo è illustrato nella figura seguente.

![diagramma che illustra il processo di risoluzione del codice sorgente](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>Gestori dello schema

I gestori dello schema vengono usati quando l'applicazione chiama [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) o il relativo equivalente asincrono, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).

Il resolver di origine cerca i gestori dello schema nel registro di sistema. I gestori dello schema sono elencati in base allo schema URL, con le chiavi seguenti:

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

dove *<scheme>* è lo schema URL che il gestore è progettato per l'analisi. Lo schema include il carattere ":" finale; ad esempio, "http:".

Per registrare un nuovo gestore dello schema, aggiungere una voce il cui nome è il CLSID del gestore dello schema, in formato stringa canonico: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Il valore della voce è una stringa (REG \_ SZ) contenente una breve descrizione del gestore, ad esempio "gestore dello schema personale". La parte importante della voce è il CLSID. Il resolver di origine crea il gestore chiamando **CoCreateInstance** con il CLSID.

I gestori dello schema espongono l'interfaccia [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) . Se il resolver di origine trova un gestore dello schema corrispondente allo schema URL, il resolver di origine chiama [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passando l'URL originale. Il gestore dello schema apre l'URL e tenta di analizzare il contenuto. A questo punto, il gestore dello schema ha due opzioni:

-   Creare un'origine multimediale.
-   Creare un flusso di byte.

Se crea un'origine multimediale, il resolver di origine restituisce l'origine del supporto all'applicazione. Se viene creato un flusso di byte, il resolver di origine tenta di trovare un gestore del flusso di byte appropriato, come descritto nella sezione successiva.

## <a name="byte-stream-handlers"></a>Gestori di Byte-Stream

I gestori del flusso di byte vengono usati quando l'applicazione chiama [**IMFSourceResolver:: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) o il relativo equivalente asincrono, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream). Vengono inoltre utilizzate quando un gestore dello schema restituisce un flusso di byte, come descritto in precedenza.

Come per i gestori dello schema, i gestori del flusso di byte sono elencati nel registro di sistema. Sono elencate in base all'estensione del nome di file o al tipo MIME (o entrambi), con le chiavi seguenti:

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

dove *<ExtensionOrMimeType>* è l'estensione del nome file o il tipo MIME. Le estensioni di file includono il carattere ' .' iniziale; ad esempio, ". wmv".

L'estensione del nome file fa parte dell'URL, fornito dall'applicazione. Il tipo MIME potrebbe essere disponibile tramite l'attributo del [**\_ tipo di \_ contenuto \_ MF BYTESTREAM**](mf-bytestream-content-type-attribute.md) nel flusso di byte.

Per registrare un nuovo gestore del flusso di byte, aggiungere una voce il cui nome è il CLSID del gestore, in formato stringa canonico. Il valore della voce è una stringa (REG \_ SZ) contenente una breve descrizione del gestore, ad esempio "gestore Byte-Stream." Il resolver di origine chiama **CoCreateInstance** per creare il gestore dal CLSID. È possibile registrare lo stesso gestore in più di un'estensione o di un tipo MIME.

I gestori del flusso di byte espongono l'interfaccia [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) . Se il resolver di origine trova un gestore del flusso di byte corrispondente, viene chiamato [**IMFByteStreamHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). L'input per questo metodo è un puntatore al flusso di byte, più l'URL originale, se disponibile. Il gestore del flusso di byte legge dal flusso di byte fino a quando non viene analizzato un numero sufficiente di dati per creare l'origine multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 



