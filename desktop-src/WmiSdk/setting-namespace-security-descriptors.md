---
description: Sia le applicazioni C++ che gli script in esecuzione con un account amministratore completo possono modificare il descrittore di sicurezza dello spazio dei nomi.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Impostazione di descrittori di sicurezza dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318527"
---
# <a name="setting-namespace-security-descriptors"></a><span data-ttu-id="21eb7-103">Impostazione di descrittori di sicurezza dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21eb7-103">Setting Namespace Security Descriptors</span></span>

<span data-ttu-id="21eb7-104">Sia le applicazioni C++ che gli script in esecuzione con un account amministratore completo possono modificare il descrittore di sicurezza dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="21eb7-104">Both C++ applications and scripts running under a full administrator account can change a namespace security descriptor.</span></span>

## <a name="namespace-security-descriptors"></a><span data-ttu-id="21eb7-105">Descrittori di sicurezza dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21eb7-105">Namespace Security Descriptors</span></span>

<span data-ttu-id="21eb7-106">Ogni spazio dei nomi WMI dispone di un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)che consente a ogni spazio dei nomi di disporre di impostazioni di sicurezza univoche che determinano chi ha accesso ai dati e ai metodi dello spazio</span><span class="sxs-lookup"><span data-stu-id="21eb7-106">Each WMI namespace has a [*security descriptor*](/windows/desktop/SecGloss/s-gly), which allows each namespace to have unique security settings that determine who has access to the namespace data and methods.</span></span> <span data-ttu-id="21eb7-107">Per ulteriori informazioni sulla sicurezza dell'accesso WMI, vedere [accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="21eb7-107">For more information about WMI access security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span> <span data-ttu-id="21eb7-108">L' [accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md) descrive le impostazioni di sicurezza predefinite per gli spazi dei nomi WMI e il controllo della sicurezza in WMI.</span><span class="sxs-lookup"><span data-stu-id="21eb7-108">[Access to WMI Namespaces](access-to-wmi-namespaces.md) describes the default security settings for WMI namespaces and security auditing in WMI.</span></span>

<span data-ttu-id="21eb7-109">È possibile impostare le autorizzazioni dell'account per ogni spazio dei nomi WMI nel repository WMI (CIM) nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="21eb7-109">You can set account permissions for each WMI namespace in the WMI (CIM) repository in the following ways:</span></span>

-   <span data-ttu-id="21eb7-110">Quando lo spazio dei nomi viene creato nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="21eb7-110">When the namespace is created in the MOF file.</span></span> <span data-ttu-id="21eb7-111">Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei nomi](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="21eb7-111">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>
-   <span data-ttu-id="21eb7-112">Manualmente, utilizzando il controllo WMI.</span><span class="sxs-lookup"><span data-stu-id="21eb7-112">Manually, using the WMI Control.</span></span> <span data-ttu-id="21eb7-113">Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="21eb7-113">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>
-   <span data-ttu-id="21eb7-114">A livello di codice, chiamando i metodi della classe [**\_ \_ SystemSecurity**](--systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="21eb7-114">Programmatically, by calling the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span>

<span data-ttu-id="21eb7-115">I metodi seguenti dell'oggetto [**\_ \_ SystemSecurity**](--systemsecurity.md) associato a ogni spazio dei nomi consentono di leggere o modificare la sicurezza in uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="21eb7-115">The following methods of the [**\_\_SystemSecurity**](--systemsecurity.md) object associated with each namespace allow you to read or change security on a namespace.</span></span>

<dl> <dt>

<span data-ttu-id="21eb7-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span><span class="sxs-lookup"><span data-stu-id="21eb7-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span></span>
</dt> <dd>

<span data-ttu-id="21eb7-117">Imposta il parametro *Rights* come bitmap con ogni bit corrispondente a un diritto di accesso.</span><span class="sxs-lookup"><span data-stu-id="21eb7-117">Sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span>

</dd> <dt>

<span data-ttu-id="21eb7-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**Getsd ha**](--systemsecurity-getsd.md)</span><span class="sxs-lookup"><span data-stu-id="21eb7-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="21eb7-119">Ottiene il descrittore di sicurezza per lo spazio dei nomi a cui è connesso l'utente.</span><span class="sxs-lookup"><span data-stu-id="21eb7-119">Gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="21eb7-120">Questo metodo restituisce un descrittore di sicurezza in formato di matrice di byte binario.</span><span class="sxs-lookup"><span data-stu-id="21eb7-120">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="21eb7-121">Se si scrive uno script, usare il metodo [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .</span><span class="sxs-lookup"><span data-stu-id="21eb7-121">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="21eb7-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**Setsd ha**](--systemsecurity-setsd.md)</span><span class="sxs-lookup"><span data-stu-id="21eb7-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="21eb7-123">Imposta il descrittore di sicurezza (SD) per lo spazio dei nomi a cui è connesso un utente.</span><span class="sxs-lookup"><span data-stu-id="21eb7-123">Sets the security descriptor (SD) for the namespace to which a user is connected.</span></span> <span data-ttu-id="21eb7-124">Questo metodo richiede un descrittore di sicurezza in formato di matrice di byte binario.</span><span class="sxs-lookup"><span data-stu-id="21eb7-124">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="21eb7-125">Se si scrive uno script, usare il metodo [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="21eb7-125">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="21eb7-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span><span class="sxs-lookup"><span data-stu-id="21eb7-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span></span>
</dt> <dd>

<span data-ttu-id="21eb7-127">Ottiene il descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI associato all'istanza di [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="21eb7-127">Gets the security descriptor that controls access to the WMI namespace associated with the instance of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="21eb7-128">Il descrittore di sicurezza viene restituito come un'istanza di [**\_ \_ securityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="21eb7-128">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="21eb7-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span><span class="sxs-lookup"><span data-stu-id="21eb7-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span></span>
</dt> <dd>

<span data-ttu-id="21eb7-130">Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso alla stampante.</span><span class="sxs-lookup"><span data-stu-id="21eb7-130">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="21eb7-131">Il descrittore di sicurezza è rappresentato da un'istanza di [**\_ \_ securityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="21eb7-131">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="21eb7-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="21eb7-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="21eb7-133">Ottiene i diritti di accesso remoto per un elenco di singoli utenti in computer in cui sono in esecuzione versioni obsolete di Windows, in cui il controllo degli accessi tramite descrittori di sicurezza di Windows non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="21eb7-133">Gets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> <dt>

<span data-ttu-id="21eb7-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="21eb7-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="21eb7-135">Consente di impostare i diritti di accesso remoto per un elenco di singoli utenti nei computer che eseguono versioni obsolete di Windows, in cui il controllo dell'accesso tramite descrittori di sicurezza di Windows non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="21eb7-135">Sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> </dl>

<span data-ttu-id="21eb7-136">Se si scrivono script, usare [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) e [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="21eb7-136">If you are writing scripts, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) and [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span></span> <span data-ttu-id="21eb7-137">Per modificare i descrittori di sicurezza, è possibile usare i metodi della classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) .</span><span class="sxs-lookup"><span data-stu-id="21eb7-137">You can use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to alter the security descriptors.</span></span>

<span data-ttu-id="21eb7-138">Se si sta programmando in C++, è possibile modificare il descrittore di sicurezza binario usando il [linguaggio SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e i metodi di conversione [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="21eb7-138">If you are programming in C++, you can manipulate the binary security descriptor using [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="21eb7-139">Tenere presente che, a partire da Windows Vista, [controllo dell'account utente](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) influisca sull'accesso ai dati WMI e su cosa può essere configurato con il [*controllo WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="21eb7-139">Be aware that, starting with Windows Vista, [User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="21eb7-140">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="21eb7-140">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="21eb7-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21eb7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21eb7-142">Sicurezza degli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="21eb7-142">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="21eb7-143">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="21eb7-143">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="21eb7-144">Accesso agli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="21eb7-144">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="21eb7-145">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="21eb7-145">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
