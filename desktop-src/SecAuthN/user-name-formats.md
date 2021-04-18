---
description: Quando un'applicazione usa l'API di gestione delle credenziali per richiedere le credenziali, è previsto che l'utente immetta le informazioni che possono essere convalidate dal sistema operativo o dall'applicazione.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formati di nome utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315856"
---
# <a name="user-name-formats"></a><span data-ttu-id="e4d14-103">Formati di nome utente</span><span class="sxs-lookup"><span data-stu-id="e4d14-103">User Name Formats</span></span>

<span data-ttu-id="e4d14-104">Quando un'applicazione usa l'API di gestione delle credenziali per richiedere le credenziali, è previsto che l'utente immetta le informazioni che possono essere convalidate dal sistema operativo o dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e4d14-104">When an application uses the Credentials Management API to prompt for credentials, the user is expected to enter information that can be validated, either by the operating system or by the application.</span></span> <span data-ttu-id="e4d14-105">L'utente può specificare le informazioni sulle credenziali di dominio in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="e4d14-105">The user can specify domain credentials information in one of the following formats:</span></span>

-   [<span data-ttu-id="e4d14-106">Nome entità utente</span><span class="sxs-lookup"><span data-stu-id="e4d14-106">User Principal Name</span></span>](#user-principal-name)
-   [<span data-ttu-id="e4d14-107">Nome di accesso di livello inferiore</span><span class="sxs-lookup"><span data-stu-id="e4d14-107">Down-Level Logon Name</span></span>](#down-level-logon-name)

## <a name="user-principal-name"></a><span data-ttu-id="e4d14-108">Nome entità utente</span><span class="sxs-lookup"><span data-stu-id="e4d14-108">User Principal Name</span></span>

<span data-ttu-id="e4d14-109">Il formato del [*nome dell'entità utente*](../secgloss/u-gly.md) (UPN) viene usato per specificare un nome di tipo Internet, ad esempio <b>UserName@Example.Microsoft.com</b> .</span><span class="sxs-lookup"><span data-stu-id="e4d14-109">[*User principal name*](../secgloss/u-gly.md) (UPN) format is used to specify an Internet-style name, such as <b>UserName@Example.Microsoft.com</b>.</span></span> <span data-ttu-id="e4d14-110">Nella tabella seguente sono riepilogate le parti di un UPN.</span><span class="sxs-lookup"><span data-stu-id="e4d14-110">The following table summarizes the parts of a UPN.</span></span>



| <span data-ttu-id="e4d14-111">Parte</span><span class="sxs-lookup"><span data-stu-id="e4d14-111">Part</span></span>                                                        | <span data-ttu-id="e4d14-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="e4d14-112">Example</span></span>                                |
|-------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="e4d14-113">Nome dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="e4d14-113">User account name.</span></span> <span data-ttu-id="e4d14-114">Noto anche come nome di accesso.</span><span class="sxs-lookup"><span data-stu-id="e4d14-114">Also known as the logon name.</span></span><br/> | <span data-ttu-id="e4d14-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="e4d14-115">*UserName*</span></span><br/>                  |
| <span data-ttu-id="e4d14-116">Separatore.</span><span class="sxs-lookup"><span data-stu-id="e4d14-116">Separator.</span></span> <span data-ttu-id="e4d14-117">Valore letterale carattere, il simbolo di chiocciola (@).</span><span class="sxs-lookup"><span data-stu-id="e4d14-117">A character literal, the at sign (@).</span></span><br/> | @<br/>                           |
| <span data-ttu-id="e4d14-118">Suffisso UPN.</span><span class="sxs-lookup"><span data-stu-id="e4d14-118">UPN suffix.</span></span> <span data-ttu-id="e4d14-119">Noto anche come nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="e4d14-119">Also known as the domain name.</span></span><br/>       | <span data-ttu-id="e4d14-120">*Example.Microsoft.com*</span><span class="sxs-lookup"><span data-stu-id="e4d14-120">*Example.Microsoft.com*</span></span> <br/> |



 

<span data-ttu-id="e4d14-121">Un UPN può essere definito in modo implicito o esplicito.</span><span class="sxs-lookup"><span data-stu-id="e4d14-121">A UPN can be implicitly or explicitly defined.</span></span> <span data-ttu-id="e4d14-122">Un UPN implicito è nel formato <b>UserName@DNSDomainName.com</b> .</span><span class="sxs-lookup"><span data-stu-id="e4d14-122">An implicit UPN is of the form <b>UserName@DNSDomainName.com</b>.</span></span> <span data-ttu-id="e4d14-123">Un UPN implicito è sempre associato all'account dell'utente, anche se non è definito un UPN esplicito.</span><span class="sxs-lookup"><span data-stu-id="e4d14-123">An implicit UPN is always associated with the user's account, even if an explicit UPN is not defined.</span></span> <span data-ttu-id="e4d14-124">Un UPN esplicito è nel formato <i><b>Name@Suffix</b></i> , in cui le stringhe nome e suffisso sono definite in modo esplicito dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="e4d14-124">An explicit UPN is of the form <i><b>Name@Suffix</b></i>, where both the name and suffix strings are explicitly defined by the administrator.</span></span>

## <a name="down-level-logon-name"></a><span data-ttu-id="e4d14-125">Nome di accesso Down-Level</span><span class="sxs-lookup"><span data-stu-id="e4d14-125">Down-Level Logon Name</span></span>

<span data-ttu-id="e4d14-126">Il formato del nome di accesso di livello inferiore viene usato per specificare un dominio e un account utente in tale dominio, ad esempio <i><b>dominio \\ username</b></i>.</span><span class="sxs-lookup"><span data-stu-id="e4d14-126">The down-level logon name format is used to specify a domain and a user account in that domain, for example, <i><b>DOMAIN\\UserName</b></i>.</span></span> <span data-ttu-id="e4d14-127">Nella tabella seguente sono riepilogate le parti di un nome di accesso di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="e4d14-127">The following table summarizes the parts of a down-level logon name.</span></span>



| <span data-ttu-id="e4d14-128">Parte</span><span class="sxs-lookup"><span data-stu-id="e4d14-128">Part</span></span>                                                           | <span data-ttu-id="e4d14-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="e4d14-129">Example</span></span>               |
|----------------------------------------------------------------|-----------------------|
| <span data-ttu-id="e4d14-130">Nome di dominio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="e4d14-130">NetBIOS domain name.</span></span><br/>                                | <span data-ttu-id="e4d14-131">*DOMAIN*</span><span class="sxs-lookup"><span data-stu-id="e4d14-131">*DOMAIN*</span></span><br/>   |
| <span data-ttu-id="e4d14-132">Separatore.</span><span class="sxs-lookup"><span data-stu-id="e4d14-132">Separator.</span></span> <span data-ttu-id="e4d14-133">Valore letterale carattere, barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="e4d14-133">A character literal, the backslash (\\).</span></span><br/> | **\\**<br/>     |
| <span data-ttu-id="e4d14-134">Nome dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="e4d14-134">User account name.</span></span> <span data-ttu-id="e4d14-135">Noto anche come nome di accesso.</span><span class="sxs-lookup"><span data-stu-id="e4d14-135">Also known as the logon name.</span></span><br/>    | <span data-ttu-id="e4d14-136">*UserName*</span><span class="sxs-lookup"><span data-stu-id="e4d14-136">*UserName*</span></span><br/> |



 

 

 
