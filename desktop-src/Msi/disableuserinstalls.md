---
description: Si tratta di un criterio di sistema per computer che può essere utilizzato quando l'amministratore desidera che siano installate solo le applicazioni per computer.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128391"
---
# <a name="disableuserinstalls"></a>DisableUserInstalls

Si tratta di un criterio di [sistema](system-policy.md) per computer che può essere utilizzato quando l'amministratore desidera che siano installate solo le applicazioni per computer.

Se questo criterio non è impostato, il programma di installazione cerca le applicazioni nel registro di sistema nell'ordine seguente: applicazioni gestite registrate come per utente, applicazioni non gestite registrate come per utente e infine applicazioni registrate come per computer.

Se questo criterio è impostato su 1, il programma di installazione ignorerà tutte le applicazioni registrate come per singolo utente e cercherà solo le applicazioni registrate come per computer. Le chiamate al Windows Installer Application Programming Interface o al sistema ignorano le applicazioni per utente. Il tentativo di eseguire un'installazione nel [contesto di installazione](installation-context.md) per utente fa in modo che il programma di installazione visualizzi un messaggio di errore e interrompa l'installazione. In questo caso, il Windows Installer impedisce inoltre le installazioni per utente da un server terminal.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



