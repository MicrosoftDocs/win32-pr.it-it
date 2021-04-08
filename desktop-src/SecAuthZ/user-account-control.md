---
description: Consente agli utenti di eseguire attività comuni come non amministratori, denominati utenti standard e come amministratori senza dover cambiare utenti, disconnettersi o utilizzare Run As.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Controllo dell'account utente (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968222"
---
# <a name="user-account-control-authorization"></a><span data-ttu-id="85e3c-103">Controllo dell'account utente (autorizzazione)</span><span class="sxs-lookup"><span data-stu-id="85e3c-103">User Account Control (Authorization)</span></span>

<span data-ttu-id="85e3c-104">Il controllo dell'account utente consente agli utenti di eseguire attività comuni come utenti non amministratori, detti utenti standard e come amministratori senza dover cambiare utente, disconnettersi o utilizzare **Esegui come**.</span><span class="sxs-lookup"><span data-stu-id="85e3c-104">User Account Control (UAC) enables users to perform common tasks as nonadministrators, called standard users, and as administrators without having to switch users, log off, or use **Run As**.</span></span> <span data-ttu-id="85e3c-105">Il comportamento del controllo dell'account utente per l'impostazione "non notifica mai" non consente più di disabilitare UAC.</span><span class="sxs-lookup"><span data-stu-id="85e3c-105">The behavior of UAC for the "Never notify" setting no longer disables UAC.</span></span> <span data-ttu-id="85e3c-106">L'impostazione "mai notifica" fornisce un token di divisione e eleva sempre automaticamente il privilegio richiesto.</span><span class="sxs-lookup"><span data-stu-id="85e3c-106">The "Never notify" setting gives you a split token and always automatically elevates the privilege required.</span></span> <span data-ttu-id="85e3c-107">Questa sottigliezza può causare problemi di compatibilità con l'app.</span><span class="sxs-lookup"><span data-stu-id="85e3c-107">This subtlety may cause your app to have compatibility problems.</span></span> <span data-ttu-id="85e3c-108">È comunque possibile disabilitare il controllo dell'account utente usando criteri di gruppo o impostando manualmente la chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="85e3c-108">You can still disable UAC by using Group Policies or manually setting the registry key.</span></span>

<span data-ttu-id="85e3c-109">**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** L'impostazione "non notifica mai" Disabilita il controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="85e3c-109">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** The "Never notify" setting disables UAC.</span></span>

<span data-ttu-id="85e3c-110">Se, ad esempio, si eseguono i passaggi seguenti per modificare l'impostazione "non notificare mai", si ottengono risultati diversi quando si tenta di creare un file in una cartella che richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="85e3c-110">For example, if you perform the following steps to change the "Never notify" setting, you get different outcomes when you attempt to create a file in a folder that requires elevated privileges.</span></span> <span data-ttu-id="85e3c-111">Il comportamento di Windows 8 consiste nel negare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="85e3c-111">The Windows 8 behavior is to deny access.</span></span> <span data-ttu-id="85e3c-112">Il comportamento di Windows 7 consente di creare il file di File.txt.</span><span class="sxs-lookup"><span data-stu-id="85e3c-112">The Windows 7 behavior allows you to create the File.txt file.</span></span>

1.  <span data-ttu-id="85e3c-113">Toccare o fare clic su **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="85e3c-113">Click or tap **Start**.</span></span> <span data-ttu-id="85e3c-114">Nella casella di ricerca digitare "modifica impostazioni di controllo dell'account utente".</span><span class="sxs-lookup"><span data-stu-id="85e3c-114">In the search box, type "Change User Account Control settings".</span></span>
2.  <span data-ttu-id="85e3c-115">Toccare o fare clic su **Modifica impostazioni di controllo dell'account utente** per aprirlo.</span><span class="sxs-lookup"><span data-stu-id="85e3c-115">Click or tap **Change User Account Control settings** to open it.</span></span>
3.  <span data-ttu-id="85e3c-116">Spostare il dispositivo di scorrimento su **non notificare mai**.</span><span class="sxs-lookup"><span data-stu-id="85e3c-116">Move the slider to **Never notify**.</span></span>
4.  <span data-ttu-id="85e3c-117">Toccare o fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="85e3c-117">Click or tap **OK**.</span></span>
5.  <span data-ttu-id="85e3c-118">Riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="85e3c-118">Restart your computer.</span></span>
6.  <span data-ttu-id="85e3c-119">Toccare o fare clic su **Start** , quindi su **Esegui**.</span><span class="sxs-lookup"><span data-stu-id="85e3c-119">Click or tap **Start** and then **Run**.</span></span> <span data-ttu-id="85e3c-120">Nella casella **Apri** digitare "Cmd.exe".</span><span class="sxs-lookup"><span data-stu-id="85e3c-120">In the **Open** box, type "Cmd.exe".</span></span> <span data-ttu-id="85e3c-121">Si noti che il titolo della finestra non contiene la stringa "Administrator".</span><span class="sxs-lookup"><span data-stu-id="85e3c-121">Note that the title of the window doesn't contain the string "Administrator".</span></span>
7.  <span data-ttu-id="85e3c-122">Digitare "Echo >% windir% \\ system32 \\File.txt".</span><span class="sxs-lookup"><span data-stu-id="85e3c-122">Type "echo > %windir%\\system32\\File.txt".</span></span>

<span data-ttu-id="85e3c-123">UAC è stato aggiunto in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="85e3c-123">UAC was added in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="85e3c-124">Un account utente standard è sinonimo di un account utente in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="85e3c-124">A standard user account is synonymous with a user account in Windows XP.</span></span> <span data-ttu-id="85e3c-125">Gli account utente che sono membri del gruppo Administrators locale eseguiranno la maggior parte delle applicazioni come utente standard.</span><span class="sxs-lookup"><span data-stu-id="85e3c-125">User accounts that are members of the local Administrators group will run most applications as a standard user.</span></span>

<span data-ttu-id="85e3c-126">Per informazioni su UAC, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="85e3c-126">For information about UAC, see the following topics.</span></span>



| <span data-ttu-id="85e3c-127">Argomento</span><span class="sxs-lookup"><span data-stu-id="85e3c-127">Topic</span></span>                                                                                                                                        | <span data-ttu-id="85e3c-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85e3c-128">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85e3c-129">[Linee guida per il controllo dell'account utente nello sviluppo dell'interfaccia utente](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="85e3c-129">[Guidelines for User Account Control in UI Development](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span></span><br/> | <span data-ttu-id="85e3c-130">Informazioni generali sul controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="85e3c-130">General information about UAC.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="85e3c-131">Sviluppo di applicazioni che richiedono privilegi di amministratore</span><span class="sxs-lookup"><span data-stu-id="85e3c-131">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)<br/>  | <span data-ttu-id="85e3c-132">Modelli per lo sviluppo di applicazioni che eseguono operazioni che richiedono privilegi amministrativi, ma che vengono eseguite come utente standard.</span><span class="sxs-lookup"><span data-stu-id="85e3c-132">Models for developing applications that perform operations that require administrative privilege, but that run as a standard user.</span></span><br/> |
| [<span data-ttu-id="85e3c-133">Riferimento all'autorizzazione</span><span class="sxs-lookup"><span data-stu-id="85e3c-133">Authorization Reference</span></span>](authorization-reference.md)<br/>                                                                            | <span data-ttu-id="85e3c-134">Informazioni dettagliate sulle funzioni di autorizzazione, le interfacce, le strutture e altri elementi di programmazione.</span><span class="sxs-lookup"><span data-stu-id="85e3c-134">Detailed information about authorization functions, interfaces, structures, and other programming elements.</span></span><br/>                        |



 

 

 




