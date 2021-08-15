---
title: Oggetto SpeechInput
description: Oggetto SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d96dd52d5847b3fbaa81bbc21d4015698655fba1fe2523aaddc065e6d2ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975521"
---
# <a name="the-speechinput-object"></a>Oggetto SpeechInput

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

[**L'oggetto SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) fornisce l'accesso alle proprietà di input vocale gestite dal server Agent. Le proprietà sono di sola lettura per le applicazioni client, ma l'utente può modificarle nella finestra delle proprietà di Microsoft Agent. Il server restituisce valori solo se è stato installato e abilitato un motore di riconoscimento vocale compatibile.

Le [**proprietà Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**)e [**Language**](https://www.bing.com/search?q=**Language**) non sono più supportate, ma (per compatibilità con le versioni precedenti) restituiscono valori Null se viene eseguita una query. Per eseguire query o impostare la modalità di riconoscimento vocale, usare la [**proprietà SRModeID.**](srmodeid-property.md)

-   [Proprietà speechInput](speechinput-properties.md)

 

 




