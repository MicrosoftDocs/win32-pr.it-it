---
description: Il rettangolo di delimitazione di tutti i monitor è lo schermo virtuale. Il desktop copre lo schermo virtuale anziché un singolo monitor. Nella figura seguente viene illustrata una possibile disposizione di tre monitoraggi.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: Schermata virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5516ef0cb5d99124200ab7810e484ea79027cf832a0e8da74833bf709ce5cc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037519"
---
# <a name="the-virtual-screen"></a>Schermata virtuale

Il rettangolo di delimitazione di tutti i monitor è lo *schermo virtuale*. Il desktop copre lo schermo virtuale anziché un singolo monitor. Nella figura seguente viene illustrata una possibile disposizione di tre monitoraggi.

![illustrazione che mostra tre caselle che rappresentano i monitor disposti all'interno di una casella che rappresenta lo schermo virtuale](images/multimon-1.png)

Il *monitoraggio primario* contiene l'origine (0,0). Questo è per la compatibilità con le applicazioni esistenti che prevedono un monitoraggio con un'origine. Tuttavia, il monitor principale non deve essere in alto a sinistra nello schermo virtuale. Nella figura 1 è vicino al centro. Quando il monitor principale non si trova nell'angolo superiore sinistro dello schermo virtuale, parti dello schermo virtuale hanno coordinate negative. Poiché la disposizione dei monitoraggi è impostata dall'utente, tutte le applicazioni devono essere progettate per funzionare con coordinate negative. Per altre informazioni, vedere [Multiple Monitor Considerations for Older Programs](multiple-monitor-considerations-for-older-programs.md).

Le coordinate dello schermo virtuale sono rappresentate da un valore a 16 bit con segno a causa dei valori a 16 bit contenuti in molti messaggi esistenti. Di conseguenza, i limiti dello schermo virtuale sono:

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



