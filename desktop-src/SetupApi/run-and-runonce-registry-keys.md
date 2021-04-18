---
description: Le chiavi del registro di sistema Run e RunOnce provocano l'esecuzione dei programmi ogni volta che un utente esegue l'accesso.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Chiavi del registro di sistema Run e RunOnce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89cf51ad3c7e2096aeffbbd6ed98c02a202f2ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318622"
---
# <a name="run-and-runonce-registry-keys"></a>Chiavi del registro di sistema Run e RunOnce

Le chiavi del registro di sistema Run e RunOnce provocano l'esecuzione dei programmi ogni volta che un utente esegue l'accesso. Il valore dei dati per una chiave è una riga di comando non più lunga di 260 caratteri. Registrare i programmi da eseguire aggiungendo voci della riga di comando della stringa di *Descrizione* del modulo -  = . È possibile scrivere più voci in una chiave. Se più di un programma viene registrato con una chiave specifica, l'ordine in cui vengono eseguiti i programmi è indeterminato.

Il registro di sistema di Windows include le quattro chiavi Run e RunOnce seguenti:

-   **HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**

Per impostazione predefinita, il valore di una chiave RunOnce viene eliminato prima dell'esecuzione della riga di comando. È possibile anteporre un nome di valore RunOnce a un punto esclamativo (!) per rinviare l'eliminazione del valore finché non viene eseguito il comando. Senza il prefisso del punto esclamativo, se l'operazione RunOnce ha esito negativo, al successivo avvio del computer non verrà richiesto di eseguire il programma associato.

Per impostazione predefinita, queste chiavi vengono ignorate quando il computer viene avviato in modalità provvisoria. Il nome del valore delle chiavi RunOnce può essere preceduto da un asterisco ( \* ) per forzare l'esecuzione del programma anche in modalità provvisoria.

Un programma eseguito da una qualsiasi di queste chiavi non deve scrivere nella chiave durante l'esecuzione, in quanto questa operazione interferisce con l'esecuzione di altri programmi registrati con la chiave. Le applicazioni devono utilizzare la chiave RunOnce solo per le condizioni temporanee, ad esempio per completare la configurazione dell'applicazione. Un'applicazione non deve ricreare continuamente le voci in RunOnce perché questa operazione interferisce con Installazione di Windows.
