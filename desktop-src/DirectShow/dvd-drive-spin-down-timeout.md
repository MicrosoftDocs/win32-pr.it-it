---
description: Timeout della rotazione dell'unità DVD
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Timeout della rotazione dell'unità DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876834"
---
# <a name="dvd-drive-spin-down-timeout"></a>Timeout della rotazione dell'unità DVD

Nei computer portatili, per preservare la durata della batteria può essere opportuno ridurre il tempo di esecuzione di un'unità DVD dopo che l'utente ha sospeso la riproduzione. Per impostazione predefinita, il navigatore DVD mantiene la rotazione del disco per due minuti. Questo valore può essere modificato nel registro di sistema di Windows in questa chiave:


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



dove


```
Sec
```



tempo di inattività in secondi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Appendici](appendixes.md)
</dt> </dl>

 

 



