---
title: Attributi di identificazione utente
description: L'identità dell'utente che richiede l'autenticazione viene fornita alle DLL di estensione NPS in una serie di attributi diversi.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Attributi, identificazione utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300151"
---
# <a name="user-identification-attributes"></a><span data-ttu-id="f103a-104">Attributi di identificazione utente</span><span class="sxs-lookup"><span data-stu-id="f103a-104">User Identification Attributes</span></span>

> [!Note]  
> <span data-ttu-id="f103a-105">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f103a-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="f103a-106">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="f103a-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="f103a-107">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="f103a-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="f103a-108">L'identità dell'utente che richiede l'autenticazione viene fornita alle DLL di estensione NPS in una serie di attributi diversi.</span><span class="sxs-lookup"><span data-stu-id="f103a-108">The identity of the user requesting authentication is supplied to the NPS Extension DLLs in a number of different attributes.</span></span>

-   <span data-ttu-id="f103a-109">**ratUserName**</span><span class="sxs-lookup"><span data-stu-id="f103a-109">**ratUserName**</span></span>
-   <span data-ttu-id="f103a-110">**ratStrippedUserName**</span><span class="sxs-lookup"><span data-stu-id="f103a-110">**ratStrippedUserName**</span></span>
-   <span data-ttu-id="f103a-111">**ratFQUserName**</span><span class="sxs-lookup"><span data-stu-id="f103a-111">**ratFQUserName**</span></span>

<span data-ttu-id="f103a-112">Ogni attributo fornisce l'identità dell'utente in un formato diverso.</span><span class="sxs-lookup"><span data-stu-id="f103a-112">Each attribute provides the user identity in a different format.</span></span> <span data-ttu-id="f103a-113">In generale, gli sviluppatori devono usare **ratStrippedUserName**.</span><span class="sxs-lookup"><span data-stu-id="f103a-113">In general, developers should use **ratStrippedUserName**.</span></span> <span data-ttu-id="f103a-114">Gli utilizzi degli attributi **ratUserName** e **ratFQUserName** sono più specializzati.</span><span class="sxs-lookup"><span data-stu-id="f103a-114">The uses of the **ratUserName** and **ratFQUserName** attributes are more specialized.</span></span>

> [!Note]  
> <span data-ttu-id="f103a-115">L'attributo User-Password, **ratUserPassword**, è già stato decrittografato quando viene inviato alla DLL di estensione ed è utilizzabile in tale formato.</span><span class="sxs-lookup"><span data-stu-id="f103a-115">The User-Password attribute, **ratUserPassword**, has already been decrypted when it is sent to the extension DLL and is usable in that form.</span></span>

 

## <a name="ratusername"></a><span data-ttu-id="f103a-116">ratUserName</span><span class="sxs-lookup"><span data-stu-id="f103a-116">ratUserName</span></span>

<span data-ttu-id="f103a-117">L'attributo **ratUserName** contiene il nome effettivamente inviato "in transito".</span><span class="sxs-lookup"><span data-stu-id="f103a-117">The **ratUserName** attribute contains the name that was actually sent "over the wire."</span></span> <span data-ttu-id="f103a-118">NPS non è in alcun modo in grado di elaborare o convalidare il contenuto di questo attributo.</span><span class="sxs-lookup"><span data-stu-id="f103a-118">NPS has not, in any way, processed or validated the contents of this attribute.</span></span> <span data-ttu-id="f103a-119">Questo attributo potrebbe non essere disponibile perché l'utente potrebbe essere stato identificato tramite un mezzo, ad esempio ID chiamante.</span><span class="sxs-lookup"><span data-stu-id="f103a-119">This attribute may not be available at all because the user may have been identified through a means such as caller ID.</span></span>

<span data-ttu-id="f103a-120">Quando si usa [**RadiusExtensionProcess/ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), se questo attributo è disponibile, è disponibile solo nel plug-in DLL dell'estensione di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f103a-120">When using [**RadiusExtensionProcess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), if this attribute is available, it is available only at the Authentication Extension DLL plug-in point.</span></span> <span data-ttu-id="f103a-121">L'attributo **ratUserName** non è disponibile nel punto di plug-in DLL dell'estensione di autorizzazione perché nelle DLL dell'estensione di autorizzazione le funzioni **RadiusExtensionProcess/ex** visualizzano solo gli attributi "in uscita".</span><span class="sxs-lookup"><span data-stu-id="f103a-121">The **ratUserName** attribute is not available at the Authorization Extension DLL plug-in point because in Authorization Extension DLLs the **RadiusExtensionProcess/Ex** functions see only the "outbound" attributes.</span></span>

<span data-ttu-id="f103a-122">Quando si usa [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), se questo attributo è disponibile, è disponibile sia per il punto di plug-in DLL dell'estensione di autenticazione che per il plug-in DLL dell'estensione di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="f103a-122">When using [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), if this attribute is available, it is available at both the Authentication Extension DLL plug-in point and the Authorization Extension DLL plug-in point.</span></span>

## <a name="ratstrippedusername"></a><span data-ttu-id="f103a-123">ratStrippedUserName</span><span class="sxs-lookup"><span data-stu-id="f103a-123">ratStrippedUserName</span></span>

<span data-ttu-id="f103a-124">**RatStrippedUserName** è l'identità dell'utente dopo l'"estrazione dell'area di autenticazione".</span><span class="sxs-lookup"><span data-stu-id="f103a-124">The **ratStrippedUserName** is the user's identity after "realm stripping."</span></span> <span data-ttu-id="f103a-125">Per ulteriori informazioni sulla rimozione dell'area di autenticazione, vedere l'argomento relativo ai nomi dell'area di [autenticazione](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) in http: \\ \\ technet2.Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f103a-125">For more information on realm stripping, see the [Realm names](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) topic on http:\\\\technet2.microsoft.com.</span></span>

<span data-ttu-id="f103a-126">Questo attributo può essere presente nel punto di plug-in DLL dell'estensione di autenticazione, nel punto di plug-in DLL dell'estensione di autorizzazione o in entrambi.</span><span class="sxs-lookup"><span data-stu-id="f103a-126">This attribute may be present at the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="f103a-127">Il formato di questo attributo è garantito:</span><span class="sxs-lookup"><span data-stu-id="f103a-127">This attribute is guaranteed to have the format:</span></span>

<span data-ttu-id="f103a-128">\*\*\*\*\\*\*\* Nome utente dominio\*</span><span class="sxs-lookup"><span data-stu-id="f103a-128">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="f103a-129">Dove *Domain* è il nome di dominio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="f103a-129">Where *Domain* is the NetBIOS domain name.</span></span>

## <a name="ratfqusername"></a><span data-ttu-id="f103a-130">ratFQUserName</span><span class="sxs-lookup"><span data-stu-id="f103a-130">ratFQUserName</span></span>

<span data-ttu-id="f103a-131">L'attributo **ratFQUserName** è il nome utente "completo".</span><span class="sxs-lookup"><span data-stu-id="f103a-131">The **ratFQUserName** attribute is the "fully qualified" user name.</span></span>

<span data-ttu-id="f103a-132">Questo attributo può essere presente nel punto di plug-in DLL dell'estensione di autenticazione, nel punto di plug-in DLL dell'estensione di autorizzazione o in entrambi.</span><span class="sxs-lookup"><span data-stu-id="f103a-132">This attribute may be present in the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="f103a-133">Tuttavia, il formato dell'attributo può essere diverso tra i due punti di plug-in.</span><span class="sxs-lookup"><span data-stu-id="f103a-133">However, the format of the attribute may differ between the two plug-in points.</span></span> <span data-ttu-id="f103a-134">Al punto di plug-in DLL dell'estensione di autenticazione, questo attributo sarà sempre nel formato:</span><span class="sxs-lookup"><span data-stu-id="f103a-134">At the Authentication Extension DLL plug-in point, this attribute will always be of the form:</span></span>

<span data-ttu-id="f103a-135">\*\*\*\*\\*\*\* Nome utente dominio\*</span><span class="sxs-lookup"><span data-stu-id="f103a-135">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="f103a-136">Il formato dell'attributo **ratFQUserName** in corrispondenza del punto di plug-in DLL dell'estensione di autorizzazione varia a seconda che l'utente sia un utente Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f103a-136">The format of the **ratFQUserName** attribute at the Authorization Extension DLL plug-in point depends on whether the user is an Active Directory user.</span></span>

-   <span data-ttu-id="f103a-137">Se l'utente è un utente locale **ratFQUserName** ha lo stesso formato del punto di plug-in DLL dell'estensione di autenticazione:</span><span class="sxs-lookup"><span data-stu-id="f103a-137">If the user is a local user **ratFQUserName** has the same format as for the Authentication Extension DLL plug-in point:</span></span>

    <span data-ttu-id="f103a-138">\*\*\*\*\\*\*\* Nome utente dominio\*</span><span class="sxs-lookup"><span data-stu-id="f103a-138">*Domain ***\\*** UserName*</span></span>

    <span data-ttu-id="f103a-139">.</span><span class="sxs-lookup"><span data-stu-id="f103a-139">.</span></span>

-   <span data-ttu-id="f103a-140">Se l'utente è un Active Directory utente, **ratFQUserName** può contenere il nome dell'utente nel formato "canonical".</span><span class="sxs-lookup"><span data-stu-id="f103a-140">If the user is an Active Directory user, **ratFQUserName** may contain the user's name in "canonical" format.</span></span> <span data-ttu-id="f103a-141">Il formato canonico è il formato utilizzato dal Active Directory per identificare l'utente.</span><span class="sxs-lookup"><span data-stu-id="f103a-141">Canonical format is the format used by the Active Directory to identify the user.</span></span> <span data-ttu-id="f103a-142">Si tratta del percorso dalla radice dell'albero Active Directory e include l'unità organizzativa (OU) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f103a-142">It is the path from the root of the Active Directory tree, and includes the user's Organizational Unit (OU).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f103a-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f103a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f103a-144">Impostazione delle DLL di estensione</span><span class="sxs-lookup"><span data-stu-id="f103a-144">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[<span data-ttu-id="f103a-145">Richiamo delle DLL di estensione</span><span class="sxs-lookup"><span data-stu-id="f103a-145">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 