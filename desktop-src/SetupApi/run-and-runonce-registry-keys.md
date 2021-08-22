---
description: Le chiavi del Registro di sistema Run e RunOnce determinano l'esecuzione dei programmi ogni volta che un utente esegue l'accesso.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Chiavi del Registro di sistema Run e RunOnce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e69559a1034e3dcdb6eae215400d475fb9ca8be4025a38d064e914837af8544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665241"
---
# <a name="run-and-runonce-registry-keys"></a>Chiavi del Registro di sistema Run e RunOnce

Le chiavi del Registro di sistema Run e RunOnce determinano l'esecuzione dei programmi ogni volta che un utente esegue l'accesso. Il valore dei dati per una chiave è una riga di comando che non contiene più di 260 caratteri. Registrare i programmi da eseguire aggiungendo voci della riga di comando della - *stringa di descrizione* = *del modulo*. È possibile scrivere più voci in una chiave. Se più di un programma è registrato con una chiave specifica, l'ordine in cui tali programmi vengono eseguiti è indeterminato.

Il Windows seguente include le quattro chiavi Run e RunOnce seguenti:

-   **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**
-   **HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**
-   **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**

Per impostazione predefinita, il valore di una chiave RunOnce viene eliminato prima dell'esecuzione della riga di comando. È possibile antedurre un nome di valore RunOnce con un punto esclamativo (!) per rinviare l'eliminazione del valore fino a dopo l'esecuzione del comando. Senza il prefisso del punto esclamativo, se l'operazione RunOnce non riesce, al successivo avvio del computer non verrà richiesto di eseguire il programma associato.

Per impostazione predefinita, queste chiavi vengono ignorate quando il computer viene avviato in Cassaforte predefinita. Il nome del valore delle chiavi RunOnce può essere preceduto da un asterisco ( ) per forzare l'esecuzione del programma \* anche in Cassaforte predefinita.

Un programma eseguito da una di queste chiavi non deve scrivere nella chiave durante l'esecuzione, perché ciò interferirà con l'esecuzione di altri programmi registrati sotto la chiave. Le applicazioni devono usare la chiave RunOnce solo per condizioni temporanee, ad esempio per completare la configurazione dell'applicazione. Un'applicazione non deve ricreare continuamente le voci in RunOnce perché ciò interferisce con Windows programma di installazione.
