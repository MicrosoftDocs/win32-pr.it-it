---
description: Un servizio non deve accedere all' \_ utente corrente di HKEY \_ o alla radice delle \_ classi HKEY \_ , soprattutto quando si rappresenta un utente. Usare invece la funzione RegOpenCurrentUser o RegOpenUserClassesRoot.
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Servizi e registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317670"
---
# <a name="services-and-the-registry"></a><span data-ttu-id="f36e2-104">Servizi e registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f36e2-104">Services and the Registry</span></span>

<span data-ttu-id="f36e2-105">Un servizio non deve accedere **all' \_ \_ utente corrente di HKEY** o alla **\_ \_ radice delle classi HKEY**, soprattutto quando si rappresenta un utente.</span><span class="sxs-lookup"><span data-stu-id="f36e2-105">A service should not access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT**, especially when impersonating a user.</span></span> <span data-ttu-id="f36e2-106">Usare invece la funzione [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) o [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) .</span><span class="sxs-lookup"><span data-stu-id="f36e2-106">Instead, use the [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) or [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) function.</span></span>

<span data-ttu-id="f36e2-107">Se si tenta di accedere **all' \_ \_ utente corrente di HKEY** o alla **\_ \_ radice delle classi HKEY** da un servizio, potrebbe non riuscire o potrebbe sembrare funzionante, ma esiste una perdita sottostante che può causare problemi durante il caricamento o lo scaricamento del profilo utente.</span><span class="sxs-lookup"><span data-stu-id="f36e2-107">If you attempt to access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT** from a service it may fail, or it may appear to work but there is an underlying leak that can lead to problems loading or unloading the user profile.</span></span>

 

 
