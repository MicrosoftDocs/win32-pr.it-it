---
title: Matrici di caratteri conteggiate
description: L'attributo \ size \_ is \ indica il limite superiore della matrice mentre l'attributo \ length \_ indica il numero di elementi della matrice da trasmettere.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473646"
---
# <a name="counted-character-arrays"></a>Matrici di caratteri conteggiate

L' \[ [attributo \_ size](/windows/desktop/Midl/size-is) \] indica il limite superiore della matrice mentre l' \[ attributo [length \_ ](/windows/desktop/Midl/length-is) \] indica il numero di elementi della matrice da trasmettere. Oltre alla matrice, il prototipo di procedura remota deve includere tutte le variabili che rappresentano la lunghezza o la dimensione che determinano gli elementi di matrice trasmessi (possono essere parametri separati o aggregati con la stringa in una struttura). Questi attributi possono essere usati con matrici di caratteri wide o a byte singolo come se fossero con matrici di altri tipi.

Le informazioni contenute in questa sezione descrivono i prototipi di parametri di procedura remota per le matrici di caratteri. È divisa negli argomenti seguenti:

-   [\[in, out, dimensioni \_ è un \] prototipo](-in-out-size-is-prototype.md)
-   [\[in, Size \_ is e out, Size \_ è \] Prototype](-in-size-is-and-out-size-is-prototype.md)

 

 