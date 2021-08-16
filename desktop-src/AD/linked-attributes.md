---
title: Attributi collegati (Ad DS)
description: Gli attributi collegati sono coppie di attributi in cui il sistema calcola i valori di un attributo (collegamento indietro) in base ai valori impostati sull'altro attributo (collegamento in avanti) in tutta la foresta.
ms.assetid: 31b7e8f5-e46d-4aff-9b17-c8dec7f19bae
ms.tgt_platform: multiple
keywords:
- Attributi collegati AD
- Attributi AD , collegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2167169d6a9d2f8eabe69323054767ae66823d8e1fe954a232ed63fd31a9b845
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186994"
---
# <a name="linked-attributes-ad-ds"></a>Attributi collegati (Ad DS)

Gli attributi collegati sono coppie di attributi in cui il sistema calcola i valori di un attributo (collegamento indietro) in base ai valori impostati sull'altro attributo (collegamento in avanti) in tutta la foresta. Un valore di back-link in qualsiasi istanza di oggetto è costituito dai nomi DN di tutti gli oggetti per cui il DN dell'oggetto è impostato nel collegamento in avanti corrispondente. Ad esempio, "Manager" e "Report" sono una coppia di attributi collegati, dove Manager è il collegamento in avanti e Report è il collegamento indietro. Si supponga ora che Bill sia il responsabile di Joe. Se si archivia il DN dell'oggetto utente di Bill nell'attributo "Manager" dell'oggetto utente di Joe, il DN dell'oggetto utente di Joe verrà visualizzato nell'attributo "Reports" dell'oggetto utente di Bill.

Una coppia collegamento in avanti/collegamento indietro è identificata dai [**valori linkID**](/windows/desktop/ADSchema/a-linkid) di due [**definizioni attributeSchema.**](/windows/desktop/ADSchema/c-attributeschema) Il **linkID** del collegamento in avanti è un valore pari, positivo, diverso da zero e **il linkID** del collegamento indietro associato è il **linkID** di inoltro più uno. Ad esempio, **linkID** per "Manager" è 42 e **linkID** per "Reports" è 43.

Di seguito è riportato un elenco di linee guida per la definizione di una nuova coppia di attributi collegati:

-   I [**valori linkID**](/windows/desktop/ADSchema/a-linkid) devono essere univoci tra tutti [**gli oggetti attributeSchema.**](/windows/desktop/ADSchema/c-attributeschema) Per evitare conflitti, è necessario generare automaticamente **il linkID** seguendo le istruzioni nell'argomento [Ottenere un ID collegamento](obtaining-a-link-id.md).
-   Un collegamento indietro deve avere un collegamento in avanti corrispondente, cio' deve esistere prima di poter creare un attributo di collegamento indietro corrispondente.
-   Un collegamento indietro è sempre un attributo multivalore. Un collegamento in avanti può essere a valore singolo o multivalore. Usare un collegamento in avanti multivalore quando è presente una relazione molti-a-molti.
-   Il [**valore attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) di un collegamento in avanti deve essere 2.5.5.1, 2.5.5.7 o 2.5.5.14. Questi valori corrispondono a sintassi che contengono un nome distinto, ad esempio la [**sintassi Object(DS-DN).**](/windows/desktop/ADSchema/s-object-ds-dn)
-   Il [**valore attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) di un collegamento indietro deve essere 2.5.5.1, ovvero la [**sintassi Object(DS-DN).**](/windows/desktop/ADSchema/s-object-ds-dn)
-   Per convenzione, gli attributi di collegamento indietro vengono aggiunti al [**valore mayContain**](/windows/desktop/ADSchema/a-maycontain) della [**classe**](/windows/desktop/ADSchema/c-top) astratta superiore. In questo modo l'attributo di collegamento indietro può essere letto dagli oggetti di qualsiasi classe perché non vengono effettivamente archiviati con l'oggetto , ma vengono calcolati in base ai valori del collegamento in avanti.

 

 