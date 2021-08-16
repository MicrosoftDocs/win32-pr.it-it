---
description: Si tratta di criteri di sistema per computer che possono essere usati quando l'amministratore vuole installare solo applicazioni per computer.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 171c003dbe739c890bf15e5c372e40840fee0aabc9159a837c0b5572a8741b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378514"
---
# <a name="disableuserinstalls"></a>DisableUserInstalls

Si tratta di criteri di sistema per [computer che](system-policy.md) possono essere usati quando l'amministratore vuole installare solo applicazioni per computer.

Se questo criterio non è impostato, il programma di installazione cerca nel Registro di sistema le applicazioni nell'ordine seguente: applicazioni gestite registrate come per utente, applicazioni non gestite registrate come per utente e infine applicazioni registrate come per computer.

Se questo criterio è impostato su 1, il programma di installazione ignora tutte le applicazioni registrate come per utente e cerca solo le applicazioni registrate come per computer. Le chiamate all'interfaccia Windows programma di programmazione dell'applicazione o al sistema ignorano le applicazioni per utente. Se si tenta di eseguire un'installazione nel contesto di installazione per utente, il programma di installazione visualizza un messaggio di errore e arresta l'installazione. [](installation-context.md) In questo caso, il programma Windows di installazione impedisce anche le installazioni per utente da un server terminal.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del** \\ **computer** \\ **locale Programma** di installazione di \\ **Microsoft** \\ **Windows** \\ 

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



