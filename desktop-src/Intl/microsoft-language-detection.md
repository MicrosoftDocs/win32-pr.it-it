---
description: Il servizio di rilevamento del linguaggio ELS è denominato Microsoft Rilevamento lingua. Questo servizio usa la tecnologia Microsoft brevettata per consentire alle applicazioni di rilevare la lingua in cui viene scritto un testo specifico.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Rilevamento lingua Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308696"
---
# <a name="microsoft-language-detection"></a>Rilevamento lingua Microsoft

Il servizio di rilevamento del linguaggio ELS è denominato Microsoft Rilevamento lingua. Questo servizio usa la tecnologia Microsoft brevettata per consentire alle applicazioni di rilevare la lingua in cui viene scritto un testo specifico.

## <a name="input-to-microsoft-language-detection"></a>Input per Microsoft Rilevamento lingua

L'input per il servizio Microsoft Rilevamento lingua è un testo UTF-16 (formato normalizzato C). Il servizio deve determinare la lingua del testo.

## <a name="output-of-microsoft-language-detection"></a>Output di Microsoft Rilevamento lingua

Il servizio Microsoft Rilevamento lingua recupera un elenco di stringhe UTF-16 con terminazione del registro di sistema e con terminazione null, rappresentate dai rispettivi nomi, separate da delimitatori di carattere null. L'elenco è ordinato in base alla pertinenza. Per la maggior parte delle lingue vengono usati nomi neutri. Tuttavia, per alcuni, ad esempio Sr-Cyrl, Sr-Latn, zh-Hant e zh-Hans, vengono usati nomi completi.

## <a name="microsoft-language-detection-operation"></a>Operazione di Microsoft Rilevamento lingua

Il servizio Microsoft Rilevamento lingua controlla lo script Unicode del testo fornito dall'applicazione. Suddivide il testo in base agli script che rileva e quindi determina la lingua in cui viene scritto ogni segmento. Se uno script indica una sola lingua, è garantita la presenza della lingua nell'elenco di lingue di output. Il servizio usa un algoritmo brevettato per determinare la pertinenza di ogni lingua supportata.

## <a name="microsoft-language-detection-guid"></a>GUID di Microsoft Rilevamento lingua

Il GUID per il servizio Microsoft Rilevamento lingua viene dichiarato in Elssrvc. h, come illustrato nel codice seguente.


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui servizi linguistici estesi](about-extended-linguistic-services.md)
</dt> </dl>

 

 



