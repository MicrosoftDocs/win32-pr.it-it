---
title: Oggetto SpeechInput
description: Oggetto SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955624"
---
# <a name="the-speechinput-object"></a>Oggetto SpeechInput

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

L'oggetto [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) fornisce l'accesso alle proprietà di input vocale gestite dal server agente. Le proprietà sono di sola lettura per le applicazioni client, ma l'utente può modificarle nella finestra delle proprietà di Microsoft Agent. Il server restituisce valori solo se è stato installato e abilitato un motore di riconoscimento vocale compatibile.

Le proprietà [**Engine**](https://www.bing.com/search?q=**Engine**), [**installato**](https://www.bing.com/search?q=**Installed**)e [**Language**](https://www.bing.com/search?q=**Language**) non sono più supportate, ma, per compatibilità con le versioni precedenti, restituiscono valori null in caso di query. Per eseguire una query o impostare la modalità di riconoscimento vocale, utilizzare la proprietà [**SRModeID**](srmodeid-property.md) .

-   [Proprietà di SpeechInput](speechinput-properties.md)

 

 




