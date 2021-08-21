---
description: Il servizio di rilevamento della lingua ELS è denominato Microsoft Rilevamento lingua. Questo servizio usa la tecnologia microsoft-patentata per consentire alle applicazioni di rilevare la lingua in cui viene scritto testo specifico.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Microsoft Rilevamento lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c4c4df0484287ef8bebcfdb2f395212b1985b282b7391d6c047dfb98d2ed8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788381"
---
# <a name="microsoft-language-detection"></a>Microsoft Rilevamento lingua

Il servizio di rilevamento della lingua ELS è denominato Microsoft Rilevamento lingua. Questo servizio usa la tecnologia microsoft-patentata per consentire alle applicazioni di rilevare la lingua in cui viene scritto testo specifico.

## <a name="input-to-microsoft-language-detection"></a>Input per Microsoft Rilevamento lingua

L'input per il servizio Rilevamento lingua Microsoft è testo UTF-16 (formato normalizzato C). Il servizio deve determinare la lingua per questo testo.

## <a name="output-of-microsoft-language-detection"></a>Output di Microsoft Rilevamento lingua

Il servizio Microsoft Rilevamento lingua recupera una stringa UTF-16 con terminazione Null doppia in formato Registro di sistema che elenca le lingue, rappresentate dai relativi nomi, separate da delimitatori di caratteri Null. L'elenco è ordinato in base alla pertinenza. Per la maggior parte delle lingue, vengono usati nomi neutri. Tuttavia, per alcuni, ad esempio, sr-Cyrl, sr-Latn, zh-Hant e zh-Hans, vengono usati i nomi completi.

## <a name="microsoft-language-detection-operation"></a>Operazione Rilevamento lingua Microsoft

Il servizio Rilevamento lingua Microsoft controlla lo script Unicode del testo fornito dall'applicazione. Segmenta il testo in base agli script rilevati e quindi determina la lingua in cui viene scritto ogni segmento. Se uno script indica una sola lingua, la lingua sarà sempre presente nell'elenco di output delle lingue. Il servizio usa un algoritmo patentato per determinare la pertinenza di ogni linguaggio supportato.

## <a name="microsoft-language-detection-guid"></a>GUID Rilevamento lingua Microsoft

Il GUID per il servizio Rilevamento lingua Microsoft viene dichiarato in Elssrvc.h, come illustrato nel codice seguente.


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Servizi linguistici estesi](about-extended-linguistic-services.md)
</dt> </dl>

 

 



