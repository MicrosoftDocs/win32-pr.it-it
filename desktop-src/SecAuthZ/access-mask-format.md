---
description: Tutti gli oggetti a protezione diretta dispongono dei diritti di accesso usando il formato della maschera di accesso illustrato nella figura seguente.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Formato maschera di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6c66c99ed93dca399825621dfbd0cc01c2ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882649"
---
# <a name="access-mask-format"></a>Formato maschera di accesso

Tutti gli oggetti a protezione diretta dispongono dei diritti di accesso usando il formato della [*maschera di accesso*](/windows/desktop/SecGloss/a-gly) illustrato nella figura seguente.

![formato maschera di accesso](images/accctrl4.png)

In questo formato, i 16 bit meno significativi sono relativi ai diritti di accesso specifici degli oggetti, gli 8 bit successivi sono per [i diritti di accesso standard](standard-access-rights.md), che si applicano alla maggior parte dei tipi di oggetti e i 4 bit più significativi vengono usati per specificare i [diritti di accesso generici](generic-access-rights.md) a cui ogni tipo di oggetto può eseguire il mapping a un set di diritti standard e specifici dell'oggetto. Il \_ bit di sicurezza del sistema Access \_ corrisponde al [diritto di accedere al SACL dell'oggetto](sacl-access-right.md).

 

 
