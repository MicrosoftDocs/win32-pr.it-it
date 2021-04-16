---
description: WMI dispone di oggetti e metodi che consentono di leggere e modificare i descrittori di sicurezza per determinare chi ha accesso agli oggetti a protezione diretta.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Oggetti descrittore di sicurezza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571726"
---
# <a name="wmi-security-descriptor-objects"></a><span data-ttu-id="3037a-103">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="3037a-103">WMI Security Descriptor Objects</span></span>

<span data-ttu-id="3037a-104">WMI dispone di oggetti e metodi che consentono di leggere e modificare i descrittori di sicurezza per determinare chi ha accesso agli oggetti a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="3037a-104">WMI has objects and methods that allow you to read and manipulate security descriptors to determine who has access to securable objects.</span></span>

-   [<span data-ttu-id="3037a-105">Ruolo dei descrittori di sicurezza</span><span class="sxs-lookup"><span data-stu-id="3037a-105">The Role of Security Descriptors</span></span>](#the-role-of-security-descriptors)
-   [<span data-ttu-id="3037a-106">Controllo di accesso e oggetti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="3037a-106">Access Control and WMI Security Objects</span></span>](#access-control-and-wmi-security-objects)
-   [<span data-ttu-id="3037a-107">\_Oggetto securityDescriptor Win32</span><span class="sxs-lookup"><span data-stu-id="3037a-107">Win32\_SecurityDescriptor Object</span></span>](/windows)
-   [<span data-ttu-id="3037a-108">DACL e SACL</span><span class="sxs-lookup"><span data-stu-id="3037a-108">DACL and SACL</span></span>](#dacl-and-sacl)
-   [<span data-ttu-id="3037a-109">\_ACE Win32, \_ trustee Win32, \_ SID Win32</span><span class="sxs-lookup"><span data-stu-id="3037a-109">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>](/windows)
-   [<span data-ttu-id="3037a-110">Esempio: controllo dell'accesso alle stampanti</span><span class="sxs-lookup"><span data-stu-id="3037a-110">Example: Checking Who has Access to Printers</span></span>](#example-checking-who-has-access-to-printers)
-   [<span data-ttu-id="3037a-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3037a-111">Related topics</span></span>](#related-topics)

## <a name="the-role-of-security-descriptors"></a><span data-ttu-id="3037a-112">Ruolo dei descrittori di sicurezza</span><span class="sxs-lookup"><span data-stu-id="3037a-112">The Role of Security Descriptors</span></span>

<span data-ttu-id="3037a-113">I descrittori di sicurezza definiscono gli attributi di sicurezza degli oggetti a protezione diretta, ad esempio file, chiavi del registro di sistema, spazi dei nomi WMI, stampanti, servizi o condivisioni.</span><span class="sxs-lookup"><span data-stu-id="3037a-113">Security descriptors define the security attributes of securable objects such as files, registry keys, WMI namespaces, printers, services, or shares.</span></span> <span data-ttu-id="3037a-114">Un descrittore di sicurezza contiene informazioni sul proprietario e sul gruppo primario di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="3037a-114">A security descriptor contains information about the owner and primary group of an object.</span></span> <span data-ttu-id="3037a-115">Un provider può confrontare il descrittore di sicurezza delle risorse con l'identità di un utente richiedente e determinare se l'utente ha il diritto di accedere alla risorsa richiesta da un utente.</span><span class="sxs-lookup"><span data-stu-id="3037a-115">A provider can compare the resource security descriptor to the identity of a requesting user, and determine whether or not the user has the right to access the resource that a user is requesting.</span></span> <span data-ttu-id="3037a-116">Per ulteriori informazioni, vedere [accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3037a-116">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="3037a-117">Alcuni metodi WMI, ad esempio [**getsd**](--systemsecurity-getsd.md), restituiscono un descrittore di sicurezza nel formato della matrice di byte binaria.</span><span class="sxs-lookup"><span data-stu-id="3037a-117">Some WMI methods, such as [**GetSD**](--systemsecurity-getsd.md), return a security descriptor in the binary byte array format.</span></span> <span data-ttu-id="3037a-118">A partire da Windows Vista, utilizzare i metodi della classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) per convertire un descrittore di sicurezza binario in un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), che può essere modificato più facilmente.</span><span class="sxs-lookup"><span data-stu-id="3037a-118">Starting with Windows Vista, use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to convert a binary security descriptor to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), which can be manipulated more easily.</span></span> <span data-ttu-id="3037a-119">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3037a-119">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="access-control-and-wmi-security-objects"></a><span data-ttu-id="3037a-120">Controllo di accesso e oggetti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="3037a-120">Access Control and WMI Security Objects</span></span>

<span data-ttu-id="3037a-121">Di seguito è riportato un elenco di oggetti di sicurezza WMI:</span><span class="sxs-lookup"><span data-stu-id="3037a-121">The following is a list of WMI security objects:</span></span>

-   [<span data-ttu-id="3037a-122">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="3037a-122">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [<span data-ttu-id="3037a-123">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="3037a-123">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [<span data-ttu-id="3037a-124">**\_Trustee Win32**</span><span class="sxs-lookup"><span data-stu-id="3037a-124">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [<span data-ttu-id="3037a-125">**\_SID Win32**</span><span class="sxs-lookup"><span data-stu-id="3037a-125">**Win32\_SID**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

<span data-ttu-id="3037a-126">Nel diagramma seguente vengono illustrate le relazioni tra gli oggetti di sicurezza WMI.</span><span class="sxs-lookup"><span data-stu-id="3037a-126">The following diagram shows the relationships among WMI security objects.</span></span>

![relazioni tra oggetti di sicurezza WMI](images/security-descriptor.png)

<span data-ttu-id="3037a-128">Per ulteriori informazioni sul ruolo di sicurezza dell'accesso, vedere [procedure](/windows/desktop/SecBP/best-practices-for-the-security-apis)consigliate per la sicurezza, [gestione della sicurezza WMI](maintaining-wmi-security.md)e [controllo degli accessi](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="3037a-128">For more information about the role of access security, see [Security Best Practices](/windows/desktop/SecBP/best-practices-for-the-security-apis), [Maintaining WMI Security](maintaining-wmi-security.md), and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

## <a name="win32_securitydescriptor-object"></a><span data-ttu-id="3037a-129">\_Oggetto securityDescriptor Win32</span><span class="sxs-lookup"><span data-stu-id="3037a-129">Win32\_SecurityDescriptor Object</span></span>

<span data-ttu-id="3037a-130">Nella tabella seguente sono elencate le proprietà della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="3037a-130">The following table lists the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class properties.</span></span>



| <span data-ttu-id="3037a-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3037a-131">Property</span></span>         | <span data-ttu-id="3037a-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3037a-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3037a-133">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="3037a-133">**ControlFlags**</span></span> | <span data-ttu-id="3037a-134">Set di bit di controllo che qualificano il significato di una SD o dei singoli membri.</span><span class="sxs-lookup"><span data-stu-id="3037a-134">Set of control bits that qualify the meaning of an SD or its individual members.</span></span> <span data-ttu-id="3037a-135">Per ulteriori informazioni sull'impostazione dei valori di bit **ControlFlags** , vedere [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="3037a-135">For more information about setting the **ControlFlags** bit values, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span><br/>                                                                                                                                                                      |
| <span data-ttu-id="3037a-136">**DACL**</span><span class="sxs-lookup"><span data-stu-id="3037a-136">**DACL**</span></span>         | <span data-ttu-id="3037a-137">[Elenco di controllo di accesso discrezionale (ACL)](/windows/desktop/SecAuthZ/access-control-lists) di utenti e gruppi e dei rispettivi diritti di accesso a un oggetto protetto.</span><span class="sxs-lookup"><span data-stu-id="3037a-137">[Discretionary Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) of users and groups, and their access rights to a secured object.</span></span> <span data-ttu-id="3037a-138">Questa proprietà contiene una matrice di [**istanze \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) che rappresentano le [voci di controllo di accesso](/windows/desktop/SecAuthZ/access-control-entries).</span><span class="sxs-lookup"><span data-stu-id="3037a-138">This property contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent [Access Control Entries](/windows/desktop/SecAuthZ/access-control-entries).</span></span> <span data-ttu-id="3037a-139">Per ulteriori informazioni, vedere [creazione di un DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="3037a-139">For more information, see [Creating a DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span><br/> |
| <span data-ttu-id="3037a-140">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="3037a-140">**Group**</span></span>        | <span data-ttu-id="3037a-141">Gruppo a cui appartiene questo oggetto protetto.</span><span class="sxs-lookup"><span data-stu-id="3037a-141">Group to which this secured object belongs.</span></span> <span data-ttu-id="3037a-142">Questa proprietà contiene un'istanza di [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) che contiene il nome, il dominio e l'ID di sicurezza (SID) del gruppo a cui appartiene il proprietario.</span><span class="sxs-lookup"><span data-stu-id="3037a-142">This property contains an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the group to which the owner belongs.</span></span><br/>                                                                                                                                                             |
| <span data-ttu-id="3037a-143">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="3037a-143">**Owner**</span></span>        | <span data-ttu-id="3037a-144">Proprietario di questo oggetto protetto.</span><span class="sxs-lookup"><span data-stu-id="3037a-144">Owner of this secured object.</span></span> <span data-ttu-id="3037a-145">Questa proprietà contiene un'istanza di [ \_ trustee Win32](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) che contiene il nome, il dominio e l'ID di sicurezza (SID) del proprietario.</span><span class="sxs-lookup"><span data-stu-id="3037a-145">This property contains an instance of [Win32\_Trustee](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the owner.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="3037a-146">**SACL**</span><span class="sxs-lookup"><span data-stu-id="3037a-146">**SACL**</span></span>         | <span data-ttu-id="3037a-147">L' [elenco di controllo di accesso di sistema (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contiene una matrice di istanze [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) che rappresentano il tipo di tentativi di accesso che generano record di controllo per utenti o gruppi.</span><span class="sxs-lookup"><span data-stu-id="3037a-147">[System Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent the type of access attempts that generate audit records for users or groups.</span></span> <span data-ttu-id="3037a-148">Per ulteriori informazioni, vedere [SACL per un nuovo oggetto](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span><span class="sxs-lookup"><span data-stu-id="3037a-148">For more information, see [SACL for a New Object](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span></span><br/>                                                                        |



 

## <a name="dacl-and-sacl"></a><span data-ttu-id="3037a-149">DACL e SACL</span><span class="sxs-lookup"><span data-stu-id="3037a-149">DACL and SACL</span></span>

<span data-ttu-id="3037a-150">Le matrici di oggetti [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) nell'elenco di controllo di accesso discrezionale (DACL) e nell'elenco di controllo di accesso di sistema {SACL) creano un collegamento tra un utente o un gruppo e i rispettivi diritti di accesso.</span><span class="sxs-lookup"><span data-stu-id="3037a-150">The arrays of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) objects in the discretionary access control list (DACL) and system access control list {SACL) create a link between a user or group and their access rights.</span></span>

<span data-ttu-id="3037a-151">Quando una proprietà DACL non contiene una voce di controllo di accesso (ACE), non vengono concessi i diritti di accesso e l'accesso all'oggetto viene negato.</span><span class="sxs-lookup"><span data-stu-id="3037a-151">When a DACL property does not contain an access control entry (ACE), access rights are not granted and access to the object is denied.</span></span>

> [!Note]  
> <span data-ttu-id="3037a-152">Un DACL **null** fornisce l'accesso completo a tutti gli utenti, che costituisce un grave rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="3037a-152">A **NULL** DACL gives full access to everyone, which is a serious security risk.</span></span> <span data-ttu-id="3037a-153">Per ulteriori informazioni, vedere [creazione di un DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="3037a-153">For more information, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

## <a name="win32_ace-win32_trustee-win32_sid"></a><span data-ttu-id="3037a-154">\_ACE Win32, \_ trustee Win32, \_ SID Win32</span><span class="sxs-lookup"><span data-stu-id="3037a-154">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>

<span data-ttu-id="3037a-155">Un [**oggetto \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) contiene un'istanza della classe [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) che identifica un utente o un gruppo e una proprietà **accessMask** che è una maschera di maschera, che specifica le azioni che possono essere eseguite da un utente o da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="3037a-155">A [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object contains an instance of the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class that identifies a user or group, and an **AccessMask** property that is a bitmask, which specifies the actions that a user or group can take.</span></span> <span data-ttu-id="3037a-156">Ad esempio, a un utente o a un gruppo potrebbe essere concesso il diritto di leggere un file, ma non di scrivere nel file.</span><span class="sxs-lookup"><span data-stu-id="3037a-156">For example, a user or group might be granted the right to read a file but not write to the file.</span></span> <span data-ttu-id="3037a-157">Un **oggetto \_ ACE Win32** contiene anche una voce ACE che indica se si tratta o meno di un accesso Consenti o nega.</span><span class="sxs-lookup"><span data-stu-id="3037a-157">A **Win32\_ACE** object also contains an ACE that indicates whether or not it is an allow or a deny access.</span></span>

> [!Note]  
> <span data-ttu-id="3037a-158">L'ordine degli [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) in un DACL è importante perché in un elenco DACL sono consentite sia la voce di controllo di accesso (ACE) che la negazione.</span><span class="sxs-lookup"><span data-stu-id="3037a-158">The [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) order in a DACL is important because both allow and deny access control entry (ACE) are permitted in a DACL.</span></span> <span data-ttu-id="3037a-159">Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="3037a-159">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="3037a-160">Ogni account utente o gruppo rappresentato da un [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) dispone di un ID di sicurezza (SID) che identifica in modo univoco un account e specifica i privilegi di accesso dell'account.</span><span class="sxs-lookup"><span data-stu-id="3037a-160">Each user account or group represented by a [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) has a security identifier (SID) that uniquely identifies an account, and specifies the access privileges of the account.</span></span> <span data-ttu-id="3037a-161">Il modo in cui si specificano i dati SID dipende dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3037a-161">How you specify the SID data depends on the operating system.</span></span> <span data-ttu-id="3037a-162">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3037a-162">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="3037a-163">Il diagramma seguente illustra il contenuto di un' [**istanza \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="3037a-163">The following diagram shows the contents of one [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instance.</span></span>

![contenuto di un' \- istanza Ace Win32](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a><span data-ttu-id="3037a-165">Esempio: controllo dell'accesso alle stampanti</span><span class="sxs-lookup"><span data-stu-id="3037a-165">Example: Checking Who has Access to Printers</span></span>

<span data-ttu-id="3037a-166">Nell'esempio di codice VBScript riportato di seguito viene illustrato come utilizzare il descrittore di sicurezza della stampante.</span><span class="sxs-lookup"><span data-stu-id="3037a-166">The following VBScript code example shows how to use the printer security descriptor.</span></span> <span data-ttu-id="3037a-167">Lo script chiama il metodo [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) nella classe [**\_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) per ottenere il descrittore, quindi determina se è presente un elenco di controllo di accesso discrezionale (DACL) nel descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="3037a-167">The script calls the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method in the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class to obtain the descriptor then determines if there is a Discretionary Access Control List (DACL) present in the security descriptor.</span></span> <span data-ttu-id="3037a-168">Se è presente un DACL, lo script ottiene l'elenco di voci di controllo di accesso (ACE) dal DACL.</span><span class="sxs-lookup"><span data-stu-id="3037a-168">If there is a DACL, then the script obtains the list of Access Control Entries (ACE) from the DACL.</span></span> <span data-ttu-id="3037a-169">Ogni voce ACE è rappresentata da un'istanza di [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span><span class="sxs-lookup"><span data-stu-id="3037a-169">Each ACE is represented by an instance of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span></span> <span data-ttu-id="3037a-170">Lo script controlla ogni voce ACE per ottenere il nome dell'utente e determinare se l'utente ha accesso alla stampante.</span><span class="sxs-lookup"><span data-stu-id="3037a-170">The script checks every ACE to get the name of the user and determine whether the user has access to the printer.</span></span> <span data-ttu-id="3037a-171">L'utente è rappresentato da un'istanza del [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) incorporato nell'istanza **\_ ACE Win32** .</span><span class="sxs-lookup"><span data-stu-id="3037a-171">The user is represented in by an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded in the **Win32\_ACE** instance.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a><span data-ttu-id="3037a-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3037a-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3037a-173">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="3037a-173">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> <dt>

[<span data-ttu-id="3037a-174">Classe helper del descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="3037a-174">Security Descriptor Helper Class</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[<span data-ttu-id="3037a-175">Procedure di sicurezza consigliate</span><span class="sxs-lookup"><span data-stu-id="3037a-175">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[<span data-ttu-id="3037a-176">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="3037a-176">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="3037a-177">Controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="3037a-177">Access Control</span></span>](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[<span data-ttu-id="3037a-178">Accesso agli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="3037a-178">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

