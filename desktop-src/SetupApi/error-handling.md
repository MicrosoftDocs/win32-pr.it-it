---
description: 'Sono disponibili tre funzioni che generano finestre di dialogo per gestire gli errori: SetupCopyError, SetupDeleteError e SetupRenameError.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Gestione degli errori (API di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f3c69a4ab4943589d00354c401b1f35aa984b04552ecd03a1c4863fcf9134a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665991"
---
# <a name="error-handling-setup-api"></a>Gestione degli errori (API di installazione)

Sono disponibili tre funzioni che generano finestre di dialogo per gestire gli errori: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)e [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).

Le routine di callback possono utilizzare queste funzioni per generare un'interfaccia utente per gestire le notifiche [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)e [**SPFILENOTIFY \_ RENAMEERROR.**](spfilenotify-renameerror.md)

Ognuna di queste funzioni di gestione degli errori genera una finestra di dialogo che chiede all'utente informazioni su come procedere. Come per [**SetupPromptForDisk,**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)è possibile modificare il layout e il comportamento della finestra di dialogo specificando flag durante la chiamata di funzione.

 

 



