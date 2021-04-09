---
description: impostazioni locali \_ SGROUPING
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968759"
---
# <a name="locale_sgrouping"></a>impostazioni locali \_ SGROUPING

Dimensioni di ogni gruppo di cifre a sinistra del separatore decimale. Il numero massimo di caratteri consentiti per questa stringa è dieci, incluso un carattere di terminazione null. Per ogni gruppo sono necessarie dimensioni esplicite e le dimensioni sono separate da punti e virgola. Se l'ultimo valore è 0, il valore precedente viene ripetuto. Per raggruppare le migliaia, ad esempio, specificare 3; 0. Le impostazioni locali indiane raggruppano le prime migliaia e quindi raggruppate per centinaia. Ad esempio, 12, 34, 56789 è rappresentato da 3, 2; 0.

Altri esempi:



| Specifiche | Stringa risultante   |
|---------------|--------------------|
| 3; 0           | 3 mila miliardi  |
| 3; 2; 0         | 30, 00, 00, 00, 00000 |
| 3             | 3 mila miliardi     |
| 3; 2           | 30000000, 00000    |



 

 

 



