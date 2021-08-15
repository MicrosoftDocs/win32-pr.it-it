---
description: Le funzioni di installazione possono generare finestre di dialogo per gestire situazioni di installazione comuni e raccogliere informazioni dall'utente.
ms.assetid: 0bff17a6-590d-4410-9ed1-0a655d94caad
title: Informazioni sulla richiesta del disco e sulla gestione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9aa7a43cc0efd81f066872a55cde20b66bb13d1c117153606f4b9fe2dd2e58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887964"
---
# <a name="about-disk-prompting-and-error-handling"></a>Informazioni sulla richiesta del disco e sulla gestione degli errori

Anche se le funzioni di installazione non forniscono un'interfaccia utente, esistono quattro funzioni di installazione che generano finestre di dialogo per gestire situazioni di installazione comuni e raccogliere informazioni dall'utente. Questi sono: [**SetupPromptForDisk,**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) [**SetupCopyError,**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)e [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora).

Le routine di callback possono chiamare queste funzioni per creare finestre di dialogo per facilitare l'elaborazione delle notifiche inviate da altre funzioni di installazione, ad esempio [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) e [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea).

La [**funzione SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) richiede all'utente di inserire supporti rimovibili, specificare un nuovo percorso di origine o annullare l'installazione. L'applicazione può offrire opzioni aggiuntive all'utente, a seconda dei flag specificati quando viene chiamata la funzione. Ad esempio, ignorare il file corrente o cercare un nuovo percorso di origine.

Le tre funzioni [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)e [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)creano finestre di dialogo che interagiscono con l'utente per raccogliere informazioni su come procedere quando si verifica un errore.

La [**funzione SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) genera una finestra di dialogo che chiede all'utente come eseguire il ripristino da un errore di copia. L'utente può specificare un nuovo percorso di origine per l'operazione di copia o annullare l'installazione. A seconda dei flag specificati durante la chiamata a **SetupCopyError,** l'utente potrebbe anche essere in grado di cercare un nuovo percorso di origine, visualizzare i dettagli dell'errore o ignorare il file corrente.

Una finestra di dialogo in cui viene chiesto all'utente come elaborare gli errori che si verificano durante un'operazione di ridenominazione di file può essere generata chiamando [**SetupRenameError.**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora) Con questa finestra di dialogo, l'utente ha la possibilità di ripetere l'operazione, ignorare l'operazione di ridenominazione corrente o interrompere l'operazione.

La [**funzione SetupDeleteError genera**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora) una finestra di dialogo in grado di raccogliere input sul modo in cui l'utente desidera gestire un errore che si è verificato durante un'operazione di eliminazione di file. All'utente vengono fornite le opzioni per ripetere l'operazione, ignorare l'operazione di eliminazione corrente o interrompere l'operazione.

La routine di callback della coda [**predefinita, SetupDefaultQueueCallback,**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)usa le quattro funzioni indicate in precedenza per generare parti dell'interfaccia utente e per gestire gli errori e richiedere nuovi supporti.

 

 



