---
description: Un gestore di terminazione garantisce che un blocco di codice specifico sia eseguito ogni volta che il flusso di controllo lascia un corpo di codice sorvegliato specifico. Un gestore di terminazione è costituito dai seguenti elementi.
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: Gestione della terminazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23e2c81465ab9d469d3d5c503c12f5bf1c7a333507d302f3e5639e0158834e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292960"
---
# <a name="termination-handling"></a>Gestione della terminazione

Un *gestore di terminazione* garantisce che un blocco di codice specifico viene eseguito ogni volta che il flusso di controllo lascia un corpo di codice sorvegliato specifico. Un gestore di terminazione è costituito dai seguenti elementi.

-   Corpo di codice sorvegliato
-   Blocco di codice di terminazione da eseguire quando il flusso di controllo esce dal corpo sorvegliato

I gestori di terminazione vengono dichiarati nella sintassi specifica del linguaggio. Usando il compilatore di ottimizzazione di Microsoft C/C++, questi vengono implementati usando **\_ \_ try** e **\_ \_ infine**. Per altre informazioni, vedere [Sintassi del gestore.](handler-syntax.md)

Il corpo sorvegliato del codice può essere un blocco di codice, un set di blocchi annidati o un'intera routine o funzione. Ogni volta che viene eseguito il corpo sorvegliato, verrà eseguito il blocco di codice di terminazione. L'unica eccezione è quando il thread termina durante l'esecuzione del corpo sorvegliato( ad esempio, se la funzione [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) o [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) viene chiamata dall'interno del corpo sorvegliato).

Il blocco di terminazione viene eseguito quando il flusso di controllo lascia il corpo sorvegliato, indipendentemente dal fatto che il corpo sorvegliato termini normalmente o in modo anomalo. Il corpo sorvegliato viene considerato terminato normalmente quando viene eseguita l'ultima istruzione nel blocco e il controllo procede in sequenza nel blocco di terminazione. La terminazione anomala si verifica quando il flusso di controllo lascia il corpo sorvegliato a causa di un'eccezione o a causa di un'istruzione di controllo, ad esempio **return**, **goto**, **break** o **continue.** La [**funzione AbnormalTermination**](abnormaltermination.md) può essere chiamata dall'interno del blocco di terminazione per determinare se il corpo sorvegliato è terminato normalmente.

 

 
