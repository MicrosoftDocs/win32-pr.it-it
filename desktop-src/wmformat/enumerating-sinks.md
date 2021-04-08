---
title: Enumerazione dei sink
description: Enumerazione dei sink
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- ASF (Advanced Systems Format), enumerazione di sink
- ASF (formato avanzato dei sistemi), enumerazione di sink
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- sink, enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724029"
---
# <a name="enumerating-sinks"></a>Enumerazione dei sink

Il writer può avere molti sink associati. È possibile enumerare i sink aggiunti al writer usando [**IWMWriterAdvanced:: GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) e [**IWMWriterAdvanced:: getsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).

Il codice di esempio presente nei [messaggi di errore ottenuti da un sink](getting-error-messages-from-a-sink.md) illustra l'enumerazione sink.

> [!Note]  
> Quando si enumerano i sink, il sink di file predefinito creato in risposta a una chiamata a [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) verrà enumerato insieme a tutti gli altri sink aggiunti. Se si usa solo il sink di file predefinito, è possibile accedervi chiamando **getsink** per l'indice di sink 0.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Utilizzo dei sink di writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




