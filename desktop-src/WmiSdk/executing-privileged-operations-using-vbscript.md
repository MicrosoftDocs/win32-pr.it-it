---
description: Se si utilizza l'API di scripting per WMI, è possibile impostare privilegi di sicurezza specifici.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Esecuzione di operazioni con privilegi tramite VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131975"
---
# <a name="executing-privileged-operations-using-vbscript"></a><span data-ttu-id="9eeea-103">Esecuzione di operazioni con privilegi tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="9eeea-103">Executing Privileged Operations Using VBScript</span></span>

<span data-ttu-id="9eeea-104">Se si utilizza l'API di scripting per WMI, è possibile impostare privilegi di sicurezza specifici.</span><span class="sxs-lookup"><span data-stu-id="9eeea-104">If you use the scripting API for WMI, you can set specific security privileges.</span></span> <span data-ttu-id="9eeea-105">Ad esempio, è possibile impostare i privilegi di sicurezza per richiedere l'arresto di un sistema operativo o per esaminare il registro eventi di protezione.</span><span class="sxs-lookup"><span data-stu-id="9eeea-105">For example, you can set the security privileges to request an operating system shutdown, or to examine the security event log.</span></span> <span data-ttu-id="9eeea-106">Per ulteriori informazioni, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="9eeea-106">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="9eeea-107">È necessario impostare i privilegi solo quando si accede a WMI nel computer.</span><span class="sxs-lookup"><span data-stu-id="9eeea-107">You only need to set privileges when you are accessing WMI on your computer.</span></span> <span data-ttu-id="9eeea-108">Quando si accede a un host remoto, in COM RPC i privilegi vengono impostati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9eeea-108">When you are accessing a remote host, COM RPC automatically sets the privileges.</span></span> <span data-ttu-id="9eeea-109">Per determinare tutti i privilegi richiesti, consultare la documentazione per le classi WMI specifiche a cui si vuole accedere, ad esempio [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="9eeea-109">To determine all the required privileges, consult the documentation for the specific WMI classes that you want to access, such as [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span> <span data-ttu-id="9eeea-110">Per ulteriori informazioni, vedere [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="9eeea-110">For more information, see [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>

<span data-ttu-id="9eeea-111">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="9eeea-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="9eeea-112">Impostazione di un privilegio dall'oggetto di sicurezza \_</span><span class="sxs-lookup"><span data-stu-id="9eeea-112">Setting a Privilege from the Security\_ Object</span></span>](/windows)
-   [<span data-ttu-id="9eeea-113">Impostazione di un privilegio come parte di un moniker</span><span class="sxs-lookup"><span data-stu-id="9eeea-113">Setting a Privilege as Part of a Moniker</span></span>](#setting-a-privilege-as-part-of-a-moniker)
-   [<span data-ttu-id="9eeea-114">Revoca e reimpostazione dei privilegi</span><span class="sxs-lookup"><span data-stu-id="9eeea-114">Revoking and Resetting Privileges</span></span>](#revoking-and-resetting-privileges)
-   [<span data-ttu-id="9eeea-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9eeea-115">Related topics</span></span>](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a><span data-ttu-id="9eeea-116">Impostazione di un privilegio dall'oggetto di sicurezza \_</span><span class="sxs-lookup"><span data-stu-id="9eeea-116">Setting a Privilege from the Security\_ Object</span></span>

<span data-ttu-id="9eeea-117">Utilizzare la procedura seguente per impostare i privilegi di sicurezza in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9eeea-117">Use the following procedure to set security privileges in Visual Basic.</span></span>

<span data-ttu-id="9eeea-118">**Per impostare i privilegi in Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="9eeea-118">**To set privileges in Visual Basic**</span></span>

1.  <span data-ttu-id="9eeea-119">Creare un oggetto di tipo [**SWbemLocator**](swbemlocator.md).</span><span class="sxs-lookup"><span data-stu-id="9eeea-119">Create an object of type [**SWbemLocator**](swbemlocator.md).</span></span>
2.  <span data-ttu-id="9eeea-120">Aggiungere il nuovo privilegio all'oggetto [**SWbemLocator. Security \_**](swbemlocator-security-.md) .</span><span class="sxs-lookup"><span data-stu-id="9eeea-120">Add the new privilege to the [**SWbemLocator.Security\_**](swbemlocator-security-.md) object.</span></span>

    <span data-ttu-id="9eeea-121">L'oggetto di [**sicurezza \_**](swbemlocator-security-.md) contiene una raccolta [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="9eeea-121">The [**Security\_**](swbemlocator-security-.md) object contains an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="9eeea-122">Gli oggetti nel set sono oggetti [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="9eeea-122">The objects in the set are [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="9eeea-123">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="9eeea-123">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

3.  <span data-ttu-id="9eeea-124">Accedere a WMI e recuperare un oggetto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="9eeea-124">Log on to WMI and retrieve an [**SWbemServices**](swbemservices.md) object.</span></span>

    <span data-ttu-id="9eeea-125">L'oggetto [**SWbemServices**](swbemservices.md) eredita il privilegio impostato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="9eeea-125">The [**SWbemServices**](swbemservices.md) object inherits the privilege that is set in the previous step.</span></span>

<span data-ttu-id="9eeea-126">È anche possibile impostare un privilegio usando il metodo [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) .</span><span class="sxs-lookup"><span data-stu-id="9eeea-126">You can also set a privilege using the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method.</span></span>

## <a name="setting-a-privilege-as-part-of-a-moniker"></a><span data-ttu-id="9eeea-127">Impostazione di un privilegio come parte di un moniker</span><span class="sxs-lookup"><span data-stu-id="9eeea-127">Setting a Privilege as Part of a Moniker</span></span>

<span data-ttu-id="9eeea-128">È possibile impostare un privilegio come parte di un moniker.</span><span class="sxs-lookup"><span data-stu-id="9eeea-128">You can set a privilege as part of a moniker.</span></span>

<span data-ttu-id="9eeea-129">Nell'esempio seguente viene illustrato come aggiungere un privilegio di debug a un moniker.</span><span class="sxs-lookup"><span data-stu-id="9eeea-129">The following example shows you how to add a debug privilege to a moniker.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a><span data-ttu-id="9eeea-130">Revoca e reimpostazione dei privilegi</span><span class="sxs-lookup"><span data-stu-id="9eeea-130">Revoking and Resetting Privileges</span></span>

<span data-ttu-id="9eeea-131">Nell'esempio seguente viene illustrato come impostare il privilegio **SeDebugPrivilege** e revocare il privilegio **SeRemoteShutdownPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="9eeea-131">The following example shows you how to set the **SeDebugPrivilege** privilege, and revoke the **SeRemoteShutdownPrivilege** privilege.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a><span data-ttu-id="9eeea-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9eeea-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eeea-133">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="9eeea-133">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="9eeea-134">Esecuzione di operazioni con privilegi</span><span class="sxs-lookup"><span data-stu-id="9eeea-134">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> </dl>

 

 
