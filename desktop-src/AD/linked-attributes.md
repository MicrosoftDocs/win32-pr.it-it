---
title: Attributi collegati (AD DS)
description: Gli attributi collegati sono coppie di attributi in cui il sistema calcola i valori di un attributo (il collegamento indietro) in base ai valori impostati sull'altro attributo (il collegamento in avanti) in tutta la foresta.
ms.assetid: 31b7e8f5-e46d-4aff-9b17-c8dec7f19bae
ms.tgt_platform: multiple
keywords:
- AD degli attributi collegati
- Attributi AD, collegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0e3f6706c797497fb1bb25ea82805385f9897e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104398831"
---
# <a name="linked-attributes-ad-ds"></a>Attributi collegati (AD DS)

Gli attributi collegati sono coppie di attributi in cui il sistema calcola i valori di un attributo (il collegamento indietro) in base ai valori impostati sull'altro attributo (il collegamento in avanti) in tutta la foresta. Un valore di back-link in qualsiasi istanza di oggetto è costituito dal DNs di tutti gli oggetti il cui DN dell'oggetto è impostato nel collegamento in avanti corrispondente. Ad esempio, "Manager" e "Reports" sono una coppia di attributi collegati, dove Manager è il collegamento in diretta e report è il collegamento indietro. Si supponga ora che Bill sia il responsabile di Joe. Se si archivia il DN dell'oggetto utente di Bill nell'attributo "Manager" dell'oggetto utente di Joe, il nome distinto dell'oggetto utente di Joe verrà visualizzato nell'attributo "Reports" dell'oggetto utente della fattura.

Una coppia di collegamenti a collegamento diretto/indietro viene identificata dai valori [**LinkId**](/windows/desktop/ADSchema/a-linkid) di due definizioni [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Il **LinkId** del collegamento diretto è un valore pari, positivo, diverso da zero e il **LinkId** del collegamento indietro associato è il **LinkId** successivo più uno. Il **LinkId** per "Manager", ad esempio, è 42 e **LinkId** per "reports" è 43.

Di seguito è riportato un elenco di linee guida per la definizione di una nuova coppia di attributi collegati:

-   I valori [**LinkId**](/windows/desktop/ADSchema/a-linkid) devono essere univoci tra tutti gli oggetti [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Per evitare conflitti, è necessario generare automaticamente il **LinkId** seguendo le istruzioni riportate nell'argomento [ottenere un ID di collegamento](obtaining-a-link-id.md).
-   Un collegamento indietro deve avere un collegamento in diretta corrispondente, ovvero è necessario che il collegamento in secondo piano esista prima che sia possibile creare un attributo back link corrispondente.
-   Un collegamento indietro è sempre un attributo multivalore. Un collegamento diretto può essere a valore singolo o multivalore. Utilizzare un collegamento in diretta multivalore quando è presente una relazione molti-a-molti.
-   Il valore [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) di un collegamento in futuro deve essere 2.5.5.1, 2.5.5.7 o 2.5.5.14. Questi valori corrispondono a sintassi che contengono un nome distinto, ad esempio la sintassi dell' [**oggetto (DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) .
-   Il valore [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) di un collegamento indietro deve essere 2.5.5.1, ovvero la sintassi dell' [**oggetto (DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) .
-   Per convenzione, gli attributi di collegamento indietro vengono aggiunti al valore [**mayContain**](/windows/desktop/ADSchema/a-maycontain) della classe astratta [**Top**](/windows/desktop/ADSchema/c-top) . In questo modo l'attributo back link viene abilitato per la lettura da oggetti di qualsiasi classe poiché non vengono effettivamente archiviati con l'oggetto, ma vengono calcolati in base ai valori di collegamento in avanti.

 

 