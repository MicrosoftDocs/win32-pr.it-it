---
title: Enumerazione di sink
description: Enumerazione di sink
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- Advanced Systems Format (ASF), enumerazione dei sink
- ASF (Advanced Systems Format), enumerazione dei sink
- Advanced Systems Format (ASF), sink
- ASF (Advanced Systems Format), sink
- sink, enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b51b46f3efdf95902b1ca5b359227da845292c4b0f23dbf0bd52039fba151cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029072"
---
# <a name="enumerating-sinks"></a>Enumerazione di sink

Al writer possono essere associati molti sink. È possibile enumerare i sink aggiunti al writer usando [**IWMWriterAdvanced::GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) e [**IWMWriterAdvanced::GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).

Il codice di esempio in Recupero [di messaggi di errore da un sink illustra](getting-error-messages-from-a-sink.md) l'enumerazione del sink.

> [!Note]  
> Durante l'enumerazione dei sink, il sink di file predefinito creato in risposta a una chiamata a [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) verrà enumerato insieme a tutti gli altri sink aggiunti. Se si usa solo il sink di file predefinito, è possibile accedervi chiamando **GetSink** per l'indice sink 0.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Uso dei sink del writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




