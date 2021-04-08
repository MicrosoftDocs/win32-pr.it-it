---
description: Un gestore di terminazione garantisce che un blocco di codice specifico venga eseguito ogni volta che il flusso di controllo lascia un particolare corpo sorvegliato del codice. Un gestore di terminazione è costituito dagli elementi seguenti.
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: Gestione della terminazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e926a47a3c0bb4f2cb8a8df350807aee89b49bab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877789"
---
# <a name="termination-handling"></a>Gestione della terminazione

Un *gestore di terminazione* garantisce che un blocco di codice specifico venga eseguito ogni volta che il flusso di controllo lascia un particolare corpo sorvegliato del codice. Un gestore di terminazione è costituito dagli elementi seguenti.

-   Corpo sorvegliato del codice
-   Un blocco di codice di terminazione da eseguire quando il flusso di controllo lascia il corpo sorvegliato

I gestori di terminazione sono dichiarati nella sintassi specifica del linguaggio. Utilizzando il compilatore Microsoft C/C++ Optimizing, questi vengono implementati usando **\_ \_ try** e **\_ \_ infine**. Per ulteriori informazioni, vedere [sintassi del gestore](handler-syntax.md).

Il corpo sorvegliato del codice può essere un blocco di codice, un set di blocchi annidati o un'intera procedura o funzione. Ogni volta che viene eseguito il corpo sorvegliato, verrà eseguito il blocco del codice di terminazione. L'unica eccezione è rappresentata dal momento in cui il thread termina durante l'esecuzione del corpo sorvegliato (ad esempio, se la funzione [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) o [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) viene chiamata dall'interno del corpo sorvegliato).

Il blocco di terminazione viene eseguito quando il flusso di controllo lascia il corpo sorvegliato, indipendentemente dal fatto che il corpo sorvegliato venga terminato normalmente o in modo anomalo. Il corpo sorvegliato viene considerato terminato normalmente quando viene eseguita l'ultima istruzione nel blocco e il controllo procede in modo sequenziale nel blocco di terminazione. Una terminazione anomala si verifica quando il flusso di controllo lascia il corpo sorvegliato a causa di un'eccezione o a causa di un'istruzione di controllo come **return**, **goto**, **break** o **continue**. La funzione [**AbnormalTermination**](abnormaltermination.md) può essere chiamata dall'interno del blocco di terminazione per determinare se il corpo sorvegliato termina normalmente.

 

 
