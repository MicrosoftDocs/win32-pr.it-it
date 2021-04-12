---
description: La directory Windows è la directory che contiene le applicazioni basate su Windows, i file di inizializzazione e i file della guida. La funzione GetWindowsDirectory Recupera il percorso di questa directory.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Configurazione del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38aa2c2b6b4f6b3ac5caac78a89ad980a9bd074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232650"
---
# <a name="operating-system-configuration"></a>Configurazione del sistema operativo

La *directory Windows* è la directory che contiene le applicazioni basate su Windows, i file di inizializzazione e i file della guida. La funzione [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) Recupera il percorso di questa directory.

La *directory di sistema* è la directory che contiene le librerie a collegamento dinamico, i driver e i file del tipo di carattere. La funzione [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) Recupera il percorso di questa directory.

La funzione [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) Recupera il nome dell'utente attualmente connesso al sistema. Il nome utente è il nome dell'account di accesso o il nome completo dell'utente, se quest'ultimo è incluso nel registro di sistema.

Una *variabile di ambiente* è una variabile simbolica che rappresenta un elemento del sistema, ad esempio un percorso, un nome di file o altri dati letterali. Ad esempio, il percorso della variabile di ambiente rappresenta le directory in cui cercare i file eseguibili. Quando un utente esegue l'accesso, il sistema Inizializza le variabili di ambiente in base alla sezione dell'ambiente del registro di sistema. La funzione [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) recupera i valori delle variabili di ambiente specificate.

Le informazioni aggiuntive sono fornite dall'interfaccia [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) .

 

 
