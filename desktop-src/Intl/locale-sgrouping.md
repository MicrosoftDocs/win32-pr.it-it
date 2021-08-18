---
description: '\_SGROUPING DELLE IMPOSTAZIONI LOCALI'
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476fa80a22e55791ca7b5636237540c457480ff0bd9c808b99ef3c6e46a17dce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106211"
---
# <a name="locale_sgrouping"></a>\_SGROUPING DELLE IMPOSTAZIONI LOCALI

Dimensioni per ogni gruppo di cifre a sinistra del separatore decimale. Il numero massimo di caratteri consentiti per questa stringa è dieci, incluso un carattere Null di terminazione. È necessaria una dimensione esplicita per ogni gruppo e le dimensioni sono separate da punti e virgola. Se l'ultimo valore è 0, il valore precedente viene ripetuto. Ad esempio, per raggruppare migliaia, specificare 3;0. Le impostazioni locali indic raggruppano le prime migliaia e quindi le centinaia. Ad esempio, 12.34.56.789 è rappresentato da 3;2;0.

Altri esempi:



| Specifiche | Stringa risultante   |
|---------------|--------------------|
| 3;0           | 3,000,000,000,000  |
| 3;2;0         | 30,00,00,00,00,000 |
| 3             | 3000000000,000     |
| 3;2           | 30000000,00,000    |



 

 

 



