---
description: Le funzioni di installazione possono generare finestre di dialogo per gestire situazioni di installazione comuni e raccogliere informazioni dall'utente.
ms.assetid: 0bff17a6-590d-4410-9ed1-0a655d94caad
title: Informazioni su richiesta disco e gestione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6c171d1e479d5d16198ba6d632848ff152f4ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306522"
---
# <a name="about-disk-prompting-and-error-handling"></a>Informazioni su richiesta disco e gestione degli errori

Sebbene le funzioni di installazione non forniscano un'interfaccia utente, sono disponibili quattro funzioni di configurazione che generano finestre di dialogo per gestire situazioni di installazione comuni e raccogliere informazioni dall'utente. Ovvero [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)e [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora).

Le routine di callback possono chiamare queste funzioni per creare finestre di dialogo che facilitano l'elaborazione delle notifiche inviate da altre funzioni di installazione, ad esempio [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) e [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea).

La funzione [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) richiede all'utente di inserire supporti rimovibili, specificare un nuovo percorso di origine o annullare l'installazione. L'applicazione può offrire opzioni aggiuntive all'utente, a seconda dei flag specificati quando viene chiamata la funzione. Sono incluse le ignorazioni del file corrente o l'esplorazione di un nuovo percorso di origine.

Le tre funzioni, [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)e [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora), consentono di creare finestre di dialogo che interagiscono con l'utente per raccogliere informazioni dall'utente su come procedere quando si verifica un errore.

La funzione [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) genera una finestra di dialogo in cui viene chiesto all'utente come eseguire il ripristino da un errore di copia. L'utente può specificare un nuovo percorso di origine per l'operazione di copia o annullare l'installazione. A seconda dei flag specificati durante la chiamata a **SetupCopyError**, l'utente potrebbe anche essere in grado di cercare un nuovo percorso di origine, visualizzare i dettagli dell'errore o ignorare il file corrente.

Una finestra di dialogo in cui viene chiesto all'utente come elaborare gli errori che si verificano durante un'operazione di ridenominazione dei file può essere generata chiamando [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora). Con questa finestra di dialogo, l'utente ha la possibilità di ripetere l'operazione, ignorare l'operazione di ridenominazione corrente o interrompere.

La funzione [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora) genera una finestra di dialogo in grado di raccogliere input sul modo in cui l'utente desidera gestire un errore che si è verificato durante un'operazione di eliminazione del file. All'utente vengono concesse le opzioni per ripetere l'operazione, ignorare l'operazione di eliminazione corrente o interrompere.

La routine di callback della coda predefinita, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), USA le quattro funzioni citate in precedenza per generare parti della relativa interfaccia utente e per gestire gli errori e richiedere nuovi supporti.

 

 



