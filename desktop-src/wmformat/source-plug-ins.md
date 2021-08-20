---
title: Plug-in di origine
description: Plug-in di origine
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows MEDIA Format SDK, plug-in di origine
- Advanced Systems Format (ASF), plug-in di origine
- ASF (Advanced Systems Format), plug-in di origine
- plug-in di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f16d0edc82423a43e50591fa07e14623adc23b94234a28985afca8a496822a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845805"
---
# <a name="source-plug-ins"></a>Plug-in di origine

Un plug-in di origine è un'opzione disponibile per gli sviluppatori che vogliono implementare il proprio sistema di archiviazione per Windows file ® multimediali. Un plug-in di origine consente questa operazione tramite l'implementazione di un'interfaccia COM denominata **IStream,** che è un'interfaccia standard per la fornitura di dati.

Il plug-in di origine deve essere scritto come dll e la sua presenza viene resa nota all'SDK tramite una voce del Registro di sistema. In questo modo può essere implementato un numero qualsiasi di plug-in di origine. Il plug-in di origine deve esportare la [**funzione WMCreateStreamForURL.**](wmcreatestreamforurl.md)

Per registrare un plug-in di origine, è necessario aggiungere la voce del Registro di sistema seguente:

HKEY \_ LOCAL MACHINE Software Microsoft Windows origini \_ \\ \\ \\ \\ WMSDK \\ multimediali

Name = "any unique name"

Valore = percorso della DLL del plug-in di origine

Dopo aver registrato la DLL, l'applicazione può usare il metodo **IWMReader::Open** (con l'URL appropriato come parametro) per accedere ai dati del flusso, che possono essere archiviati in file o contenitori di dati definiti dall'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> <dt>

[**WMCreateStreamForURL**](wmcreatestreamforurl.md)
</dt> </dl>

 

 




