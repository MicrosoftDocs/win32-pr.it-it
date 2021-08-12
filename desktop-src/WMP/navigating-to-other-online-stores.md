---
title: Passaggio ad altri negozi online
description: Passaggio ad altri negozi online
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player negozi online, navigazione
- negozi online, navigazione
- tipo 2 negozi online, navigazione
- esplorazione dei negozi online di tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1b2cb120ac161fd92bf8d35826b9dc096c95c37d916f19eb2aeb7362aabe7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574434"
---
# <a name="navigating-to-other-online-stores"></a>Passaggio ad altri negozi online

È possibile creare collegamenti ad altri negozi online di cui si è proprietari o collegarsi a negozi online forniti da altri. A tale scopo, è necessario conoscere il nome della chiave per il negozio online a cui si vuole passare.

Il codice di esempio seguente mostra il codice HTML che crea un collegamento per passare dal negozio online Proseware alla funzionalità "ServiceTask2" dello store online Southridge Video:


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



Quando l'utente fa clic sul collegamento, Windows Media Player chiede all'utente di passare all'archivio Video Southridge. Se l'utente lo consente, il lettore cambia e passa al riquadro attività specificato, aggiungendo i parametri della stringa di query. I parametri della stringa di query illustrati nell'esempio precedente sono parametri personalizzati. Ciò significa che il negozio online a cui si passa deve prevedere questi valori e gestirli. Il negozio online (e qualsiasi negozio a cui si passa) può usare i parametri della stringa di query in qualsiasi modo si sceglie.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Spostamento tra i riquadri attività servizio**](navigating-between-service-task-panes.md)
</dt> <dt>

[**Navigazione per i negozi online di tipo 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




