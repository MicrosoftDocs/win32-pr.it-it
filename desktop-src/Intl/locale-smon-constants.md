---
description: Costanti smon delle impostazioni locali \_ \*
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: Costanti LOCALE_SMON *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309500"
---
# <a name="locale_smon-constants"></a>Costanti smon delle impostazioni locali \_ \*

In questo argomento vengono definite le \_ costanti smon delle impostazioni locali \* utilizzate da NLS per la rappresentazione dei valori monetari.



| Valore                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| impostazioni locali \_ SMONDECIMALSEP  | Caratteri utilizzati come separatore decimale monetario. Il numero massimo di caratteri consentiti per questa stringa è quattro, incluso un carattere di terminazione null. Se, ad esempio, un importo monetario viene visualizzato come "$3,40", nel Stati Uniti viene visualizzato "tre dollari e 40 centesimi", quindi il separatore decimale è ".".                                                                                                                                             |
| impostazioni locali \_ SMONGROUPING    | Dimensioni di ogni gruppo di cifre monetarie a sinistra del separatore decimale. Il numero massimo di caratteri consentiti per questa stringa è dieci, incluso un carattere di terminazione null. Per ogni gruppo sono necessarie dimensioni esplicite e le dimensioni sono separate da punti e virgola. Se l'ultimo valore è 0, il valore precedente viene ripetuto. Per raggruppare le migliaia, ad esempio, specificare 3; 0. Lingue indiane raggruppate le prime migliaia e quindi raggruppate per centinaia. Ad esempio, 12, 34, 56789 è rappresentato da 3, 2; 0. |
| impostazioni locali \_ SMONTHOUSANDSEP | Caratteri utilizzati come separatore monetario tra i gruppi di cifre a sinistra del separatore decimale. Il numero massimo di caratteri consentiti per questa stringa è quattro, incluso un carattere di terminazione null. In genere, i gruppi rappresentano migliaia. Tuttavia, a seconda del valore specificato per le impostazioni locali \_ SMONGROUPING, possono rappresentare qualcos'altro.                                                                                                                                 |



 

 

 



