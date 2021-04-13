---
title: Spostamento in altri archivi online
description: Spostamento in altri archivi online
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player Online Stores, spostamento
- negozi online, esplorazione
- digitare 2 archivi online, spostamento
- spostamento nei negozi online di tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328292"
---
# <a name="navigating-to-other-online-stores"></a>Spostamento in altri archivi online

È possibile creare collegamenti ad altri negozi online di cui si è proprietari o a un collegamento incrociato a negozi online forniti da altri utenti. A tale scopo, è necessario individuare il nome della chiave per lo Store online in cui si desidera spostarsi.

Il codice di esempio seguente mostra il codice HTML che consente di creare un collegamento per passare da Proseware Online Store alla funzionalità "ServiceTask2" di Southridge Video Online Store:


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



Quando l'utente fa clic sul collegamento, Windows Media Player chiede all'utente di passare all'archivio video Southridge. Se l'utente lo consente, il lettore passa a archivia e passa al riquadro attività specificato, aggiungendo i parametri della stringa di query. I parametri della stringa di query illustrati nell'esempio precedente sono parametri personalizzati. Ciò significa che il negozio online a cui si passa deve aspettarsi questi valori e gestirli. L'archivio online (e qualsiasi archivio a cui si passa) può usare i parametri della stringa di query nel modo scelto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Spostamento tra i riquadri attività del servizio**](navigating-between-service-task-panes.md)
</dt> <dt>

[**Navigazione per i negozi di tipo 2 online**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




