---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660848eae85465ea322bcb08a218c6ee463eb384d3a4766cacf6a86038662386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609331"
---
# <a name="iagentspeechinputproperties"></a>IAgentSpeechInputProperties

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

IAgentSpeechInputProperties fornisce l'accesso alle proprietà di input vocale gestite dal server. La maggior parte delle proprietà è di sola lettura per le applicazioni client, ma l'utente può modificarle nella finestra delle proprietà di Microsoft Agent. Il server Microsoft Agent restituisce valori solo se è stato installato e abilitato un motore di riconoscimento vocale compatibile. L'esecuzione di query su queste proprietà tenta di avviare il motore di riconoscimento vocale.

**Metodi nell'ordine Vtable**



| Metodi IAgentSpeechInputProperties                                     | Descrizione                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Getenabled**](iagentspeechinputproperties--getenabled.md)           | Restituisce un valore che indica se il motore di riconoscimento vocale è abilitato. |
| [**GetHotKey**](iagentspeechinputproperties--gethotkey.md)             | Restituisce l'assegnazione di chiave corrente della chiave di ascolto.  |
| [**GetListeningTip**](iagentspeechinputproperties--getlisteningtip.md) | Restituisce un valore che indica se il suggerimento in ascolto è abilitato.             |



 

[**I metodi GetInstalled,**](https://www.bing.com/search?q=**GetInstalled**) [**GetLCID,**](https://www.bing.com/search?q=**GetLCID**) [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)e [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) (supportati nelle versioni precedenti di Microsoft Agent) sono ancora supportati per la compatibilità con le versioni precedenti. Tuttavia, i metodi non vengono stub e non restituiscono valori utili. Usare [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) e [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) per eseguire query e impostare il motore di riconoscimento vocale da usare con il carattere. Tenere presente che il motore deve corrispondere all'impostazione della lingua corrente del carattere.

 

 




