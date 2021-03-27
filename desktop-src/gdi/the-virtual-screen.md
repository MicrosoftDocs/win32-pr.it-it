---
description: Il rettangolo di delimitazione di tutti i monitoraggi è lo schermo virtuale. Il desktop copre lo schermo virtuale invece di un singolo monitor. Nella figura seguente viene illustrata una possibile disposizione di tre monitoraggi.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: Schermata virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4550ab0f849b90523842e6cc4e093c238ff11cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995125"
---
# <a name="the-virtual-screen"></a>Schermata virtuale

Il rettangolo di delimitazione di tutti i monitoraggi è lo *schermo virtuale*. Il desktop copre lo schermo virtuale invece di un singolo monitor. Nella figura seguente viene illustrata una possibile disposizione di tre monitoraggi.

![illustrazione che mostra tre caselle che rappresentano i monitoraggi disposti in una casella che rappresenta lo schermo virtuale](images/multimon-1.png)

Il *monitoraggio primario* contiene l'origine (0,0). Ciò è per la compatibilità con le applicazioni esistenti che prevedono un monitoraggio con un'origine. Il monitoraggio primario, tuttavia, non deve trovarsi nella parte superiore sinistra dello schermo virtuale. Nella figura 1 si trova vicino al centro. Quando il monitoraggio primario non si trova in alto a sinistra dello schermo virtuale, parti dello schermo virtuale presentano coordinate negative. Poiché la disposizione dei monitoraggi è impostata dall'utente, tutte le applicazioni devono essere progettate per funzionare con coordinate negative. Per ulteriori informazioni, vedere [considerazioni su più monitor per i programmi precedenti](multiple-monitor-considerations-for-older-programs.md).

Le coordinate dello schermo virtuale sono rappresentate da un valore a 16 bit con segno a causa dei valori a 16 bit contenuti in molti messaggi esistenti. Quindi, i limiti dello schermo virtuale sono:

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



