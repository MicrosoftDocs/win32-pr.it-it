---
description: Gli esempi seguenti illustrano alcune espressioni regolari per la grafia che è possibile creare.
ms.assetid: b4954e05-64d0-434a-96fd-6185671252d0
title: Esempi di espressioni regolari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1f3ac4428058a2c74b0285cd52c13a265b92c3379cef1f2ae8b2f35e19fbff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934691"
---
# <a name="regular-expression-examples"></a>Esempi di espressioni regolari

Gli esempi seguenti illustrano alcune espressioni regolari per la grafia che è possibile creare.



| Expression                                                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                               | Corrispondenze                                                                          | Non corrispondenze                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-------------------------------------------|
| s(!IS \_ ONECHAR)+p<br/>                                                                                                                                                                                                                                                                | Trova la corrispondenza con qualsiasi parola che inizia con lettere minuscole "s", contiene uno o più caratteri (come definito dall'ambito di input IS ONECHAR) e termina con una \_ "p" minuscola.<br/> | stop<br/> soup<br/> Fatica<br/> s234p<br/>               | Interrompere<br/> sp<br/>             |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)<br/>                                                                                                                                                                                                                                                   | Corrisponde a qualsiasi cifra singola, da 1 a 9.<br/>                                                                                                                         | 1<br/> 6<br/> 0<br/>                                           | 42<br/> Uno<br/>              |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9 \| , \| -)+<br/>                                                                                                                                                                                                                                            | Corrisponde a una o più cifre singole, virgole o trattini. Utile per limitare l'input a un intervallo o a un set di numeri, ad esempio un intervallo di pagine da stampare.<br/>               | 1<br/> 1-6<br/> 2,4,7<br/> 2-6,9,135<br/> ,,,<br/> | Tre<br/> Da 7 a 9<br/>   |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| \| 8 9)-(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| 4 5 \| 6 \| 7 \| 8 \| 9)-(0 \| 1 \| 2 \| 3 \| 4 \| \| 5 \| 6 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| \| 8 \| 9)<br/> | Numero di previdenza sociale. Il formato di un numero di previdenza sociale *è nnn*  -  *nn*  -  *nnnn*.<br/>                                                                     | 123-45-6789<br/>                                                           | 12-123-12<br/> 12-2-3456<br/> |



 

 

 




