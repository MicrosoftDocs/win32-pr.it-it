---
description: La Windows directory è la directory che contiene applicazioni basate Windows, file di inizializzazione e file della Guida. La funzione GetWindowsDirectory recupera il percorso di questa directory.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Configurazione del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 747a881568f9814152a230880d38891590d33ffc67cfa5e8178adfa66c1a01fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885288"
---
# <a name="operating-system-configuration"></a>Configurazione del sistema operativo

La *Windows directory* è la directory che contiene applicazioni basate Windows, file di inizializzazione e file della Guida. La [**funzione GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) recupera il percorso di questa directory.

La *directory di sistema* è la directory che contiene librerie, driver e file dei tipi di carattere a collegamento dinamico. La [**funzione GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) recupera il percorso di questa directory.

La [**funzione GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) recupera il nome dell'utente attualmente connesso al sistema. Il nome utente è il nome di accesso o il nome completo dell'utente, se quest'ultimo è incluso nel Registro di sistema.

Una *variabile di ambiente* è una variabile simbolica che rappresenta un elemento del sistema, ad esempio un percorso, un nome file o altri dati letterali. Ad esempio, la variabile di ambiente PATH rappresenta le directory in cui cercare i file eseguibili. Quando un utente accede, il sistema inizializza le variabili di ambiente in base alla sezione environment del Registro di sistema. La [**funzione ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) recupera i valori delle variabili di ambiente specificate.

Altre informazioni vengono fornite [**dall'interfaccia IADsADSystemInfo.**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo)

 

 
