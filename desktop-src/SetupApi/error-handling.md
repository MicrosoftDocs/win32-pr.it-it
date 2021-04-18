---
description: 'Sono disponibili tre funzioni che generano finestre di dialogo per la gestione degli errori: SetupCopyError, SetupDeleteError e SetupRenameError.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Gestione degli errori (API di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb1347a3bec800200c2b6bda81e3f1eeeb866de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308108"
---
# <a name="error-handling-setup-api"></a><span data-ttu-id="87990-103">Gestione degli errori (API di installazione)</span><span class="sxs-lookup"><span data-stu-id="87990-103">Error Handling (Setup API)</span></span>

<span data-ttu-id="87990-104">Sono disponibili tre funzioni che generano finestre di dialogo per la gestione degli errori: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)e [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).</span><span class="sxs-lookup"><span data-stu-id="87990-104">There are three functions that generate dialog boxes to handle errors: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora), and [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).</span></span>

<span data-ttu-id="87990-105">Le routine di callback possono usare queste funzioni per generare un'interfaccia utente per gestire le notifiche [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)e [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md) .</span><span class="sxs-lookup"><span data-stu-id="87990-105">Callback routines can use these functions to generate a user interface to handle [**SPFILENOTIFY\_COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md), and [**SPFILENOTIFY\_RENAMEERROR**](spfilenotify-renameerror.md) notifications.</span></span>

<span data-ttu-id="87990-106">Ognuna di queste funzioni di gestione degli errori genera una finestra di dialogo in cui viene chiesto all'utente di ottenere informazioni su come procedere.</span><span class="sxs-lookup"><span data-stu-id="87990-106">Each of these error-handling functions generates a dialog box that asks the user for information on how to proceed.</span></span> <span data-ttu-id="87990-107">Come per [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), è possibile modificare il layout e il comportamento della finestra di dialogo specificando flag durante la chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="87990-107">As with [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), you can modify the dialog box's layout and behavior by specifying flags during the function call.</span></span>

 

 



