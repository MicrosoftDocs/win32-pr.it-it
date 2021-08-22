---
description: Tutti gli oggetti a protezione diretta dispongono i diritti di accesso usando il formato maschera di accesso illustrato nella figura seguente.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Formato maschera di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86187f5ef69eb115bc880d2bc4df07e8b1a1f791976da2a8d24b6a0f9d7293c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914532"
---
# <a name="access-mask-format"></a>Formato maschera di accesso

Tutti gli oggetti a protezione diretta dispongono i diritti di accesso usando il formato [*maschera*](/windows/desktop/SecGloss/a-gly) di accesso illustrato nella figura seguente.

![formato maschera di accesso](images/accctrl4.png)

In questo formato, i 16 bit meno importanti sono per i diritti di accesso specifici dell'oggetto, i successivi 8 bit sono per i diritti di accesso [standard,](standard-access-rights.md)che si applicano alla maggior parte dei tipi di oggetti, e i 4 bit di ordine elevato vengono usati per specificare diritti di accesso [generici](generic-access-rights.md) di cui ogni tipo di oggetto può eseguire il mapping a un set di diritti standard e specifici dell'oggetto. Il bit ACCESS \_ SYSTEM SECURITY corrisponde al diritto di accedere \_ [all'elenco SACL dell'oggetto.](sacl-access-right.md)

 

 
