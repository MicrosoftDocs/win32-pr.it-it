---
description: La tabella seguente identifica i limiti delle dimensioni per i vari elementi del registro di sistema.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Limiti delle dimensioni degli elementi del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 262609a64e60536dcfc41f29e5d94ea499158861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313267"
---
# <a name="registry-element-size-limits"></a>Limiti delle dimensioni degli elementi del registro di sistema

La tabella seguente identifica i limiti delle dimensioni per i vari elementi del registro di sistema.



| Elemento Registry | Limite dimensione                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome della chiave         | 255 caratteri. Il nome della chiave include il percorso assoluto della chiave nel registro di sistema, iniziando sempre con una chiave di base, ad esempio \_ HKEY \_ macchina locale. |
| Nome del valore       | 16.383 caratteri **Windows 2000:** 260 caratteri ANSI o 16.383 caratteri Unicode.<br/>                                                       |
| Valore            | Memoria disponibile (formato più recente) 1 MB (formato standard)<br/>                                                                                     |
| Albero             | Un albero del registro di sistema può avere una profondità di 512 livelli. È possibile creare fino a 32 livelli alla volta tramite una singola chiamata API del registro di sistema.                                  |



 

I valori Long (più di 2.048 byte) devono essere archiviati in un file e il percorso del file deve essere archiviato nel registro di sistema. Ciò consente di eseguire in modo efficiente il registro di sistema.

Il percorso del file può corrispondere al nome di un valore o ai dati di un valore. Ogni barra rovesciata nella stringa di posizione deve essere preceduta da un'altra barra rovesciata come carattere di escape. Ad esempio, specificare "C: \\ \\ mydir \\ \\ MyFile" per archiviare la stringa "c: \\ mydir \\ MyFile". Un percorso di file può essere anche il nome di una chiave se è entro il limite di 255 caratteri per i nomi delle chiavi e non contiene barre rovesciate, che non sono consentite nei nomi di chiave.

 

 




