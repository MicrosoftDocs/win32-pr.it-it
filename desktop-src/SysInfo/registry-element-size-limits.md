---
description: La tabella seguente identifica i limiti delle dimensioni per i vari elementi del Registro di sistema.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Limiti delle dimensioni degli elementi del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76a11abc80f80a13e0643d7745d211168ecba8bcf06446af9ac842f8351567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885234"
---
# <a name="registry-element-size-limits"></a>Limiti delle dimensioni degli elementi del Registro di sistema

La tabella seguente identifica i limiti delle dimensioni per i vari elementi del Registro di sistema.



| Elemento Registry | Limite dimensione                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome della chiave         | 255 caratteri. Il nome della chiave include il percorso assoluto della chiave nel Registro di sistema, sempre a partire da una chiave di base, ad esempio HKEY \_ LOCAL \_ MACHINE. |
| Nome del valore       | 16.383 caratteri **Windows 2000:** 260 caratteri ANSI o 16.383 caratteri Unicode.<br/>                                                       |
| Valore            | Memoria disponibile (formato più recente)1 MB (formato standard)<br/>                                                                                     |
| Albero             | Un albero del Registro di sistema può avere una profondità di 512 livelli. È possibile creare fino a 32 livelli alla volta tramite una singola chiamata API del Registro di sistema.                                  |



 

I valori lunghi (più di 2.048 byte) devono essere archiviati in un file e il percorso del file deve essere archiviato nel Registro di sistema. Ciò consente al Registro di sistema di eseguire in modo efficiente.

Il percorso del file può essere il nome di un valore o i dati di un valore. Ogni barra rovesciata nella stringa di posizione deve essere preceduta da un'altra barra rovesciata come carattere di escape. Ad esempio, specificare "C: mydir myfile" per archiviare \\ \\ la stringa \\ \\ "C: \\ mydir \\ myfile". Un percorso di file può anche essere il nome di una chiave se rientra nel limite di 255 caratteri per i nomi di chiave e non contiene barre rovesciate, che non sono consentite nei nomi di chiave.

 

 




