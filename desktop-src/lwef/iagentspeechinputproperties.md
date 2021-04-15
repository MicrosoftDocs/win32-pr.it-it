---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395227"
---
# <a name="iagentspeechinputproperties"></a>IAgentSpeechInputProperties

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

IAgentSpeechInputProperties consente di accedere alle proprietà di input vocale gestite dal server. La maggior parte delle proprietà è di sola lettura per le applicazioni client, ma l'utente può modificarle nella finestra delle proprietà di Microsoft Agent. Il server Microsoft Agent restituisce i valori solo se è stato installato un motore di riconoscimento vocale compatibile ed è abilitato. L'esecuzione di query su queste proprietà tenta di avviare il motore di riconoscimento vocale.

**Metodi nell'ordine Vtable**



| Metodi IAgentSpeechInputProperties                                     | Descrizione                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**GetEnabled**](iagentspeechinputproperties--getenabled.md)           | Restituisce un valore che indica se il motore di riconoscimento vocale è abilitato. |
| [**GetHotKey**](iagentspeechinputproperties--gethotkey.md)             | Restituisce l'assegnazione di chiave corrente del tasto di attesa.  |
| [**GetListeningTip**](iagentspeechinputproperties--getlisteningtip.md) | Restituisce un valore che indica se il suggerimento di ascolto è abilitato.             |



 

I metodi [**Getinstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLcid**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)e [**semotore**](https://www.bing.com/search?q=**SetEngine**) (supportati nelle versioni precedenti di Microsoft Agent) sono ancora supportati per la compatibilità con le versioni precedenti. Tuttavia, i metodi non vengono sottoposti a Stub e non restituiscono valori utili. Usare [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) e [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) per eseguire una query e impostare il motore di riconoscimento vocale da usare con il carattere. Tenere presente che il motore deve corrispondere all'impostazione della lingua corrente del carattere.

 

 




