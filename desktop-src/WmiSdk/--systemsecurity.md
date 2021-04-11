---
description: Contiene metodi che consentono di accedere e modificare le impostazioni di sicurezza per uno spazio dei nomi.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: Classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132083"
---
# <a name="__systemsecurity-class"></a><span data-ttu-id="a4240-103">\_\_Classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="a4240-103">\_\_SystemSecurity class</span></span>

<span data-ttu-id="a4240-104">La classe di sistema **\_ \_ SystemSecurity** contiene metodi che consentono di accedere e modificare le impostazioni di sicurezza per uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a4240-104">The **\_\_SystemSecurity** system class contains methods that let you access and modify the security settings for a namespace.</span></span> <span data-ttu-id="a4240-105">La classe **\_ \_ SystemSecurity** è una classe singleton in ogni spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a4240-105">The **\_\_SystemSecurity** class is a singleton class in each namespace.</span></span>

> [!Note]  
> <span data-ttu-id="a4240-106">Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="a4240-106">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

 

<span data-ttu-id="a4240-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a4240-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a4240-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a4240-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4240-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4240-109">Syntax</span></span>

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a><span data-ttu-id="a4240-110">Members</span><span class="sxs-lookup"><span data-stu-id="a4240-110">Members</span></span>

<span data-ttu-id="a4240-111">La classe **\_ \_ SystemSecurity** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a4240-111">The **\_\_SystemSecurity** class has these types of members:</span></span>

-   [<span data-ttu-id="a4240-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a4240-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a4240-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a4240-113">Methods</span></span>

<span data-ttu-id="a4240-114">La classe **\_ \_ SystemSecurity** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a4240-114">The **\_\_SystemSecurity** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a4240-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="a4240-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a4240-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4240-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a4240-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4240-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a4240-118">Ottiene un elenco di utenti a cui è consentito l'accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="a4240-118">Gets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a4240-119">Questo metodo non funziona sulle versioni supportate di Windows.</span><span class="sxs-lookup"><span data-stu-id="a4240-119">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="a4240-120"><a href="--systemsecurity-getsd.md"><strong>Viene</strong></a> invece utilizzato.</span><span class="sxs-lookup"><span data-stu-id="a4240-120">Use <a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a4240-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4240-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a4240-122">Restituisce una maschera con ogni bit corrispondente a un diritto di accesso.</span><span class="sxs-lookup"><span data-stu-id="a4240-122">Returns a mask with each bit that corresponds to an access right.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a4240-123"><a href="--systemsecurity-getsd.md"><strong>Getsd ha</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4240-123"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a4240-124">Ottiene l' <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> per lo spazio dei nomi a cui è connesso l'utente.</span><span class="sxs-lookup"><span data-stu-id="a4240-124">Gets the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a4240-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4240-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a4240-126">Ottiene il descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI associato all'istanza di <strong>__SystemSecurity</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4240-126">Gets the security descriptor that controls access to the WMI namespace associated with the instance of <strong>__SystemSecurity</strong>.</span></span> <span data-ttu-id="a4240-127">Il descrittore di sicurezza viene restituito come un'istanza di<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a4240-127">The security descriptor is returned as an instance of<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a4240-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4240-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a4240-129">Imposta un elenco di utenti a cui è consentito l'accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="a4240-129">Sets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a4240-130">Questo metodo non funziona sulle versioni supportate di Windows.</span><span class="sxs-lookup"><span data-stu-id="a4240-130">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="a4240-131">Utilizzare invece <a href="--systemsecurity-setsd.md"><strong>set</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a4240-131">Use <a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a4240-132"><a href="--systemsecurity-setsd.md"><strong>Setsd ha</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4240-132"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a4240-133">Imposta il descrittore di sicurezza per lo spazio dei nomi a cui è connesso l'utente.</span><span class="sxs-lookup"><span data-stu-id="a4240-133">Sets the security descriptor for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a4240-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4240-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a4240-135">Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso alla stampante.</span><span class="sxs-lookup"><span data-stu-id="a4240-135">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="a4240-136">Il descrittore di sicurezza è rappresentato da un'istanza di <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a4240-136">The security descriptor is represented by an instance of <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a4240-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4240-137">Remarks</span></span>

<span data-ttu-id="a4240-138">È possibile richiedere che le applicazioni e gli script client usino una connessione crittografata per l'autenticazione aggiungendo il qualificatore **RequiresEncryption** al file MOF che crea lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a4240-138">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="a4240-139">È anche possibile modificare uno spazio dei nomi esistente aggiungendo questo attributo e compilare di nuovo il file con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="a4240-139">You can also modify an existing namespace by adding this attribute and compile the .mof file again.</span></span> <span data-ttu-id="a4240-140">Per ulteriori informazioni sull'utilizzo di **RequiresEncryption**, vedere la pagina relativa alla [richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="a4240-140">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4240-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4240-141">Requirements</span></span>



| <span data-ttu-id="a4240-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4240-142">Requirement</span></span> | <span data-ttu-id="a4240-143">Valore</span><span class="sxs-lookup"><span data-stu-id="a4240-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a4240-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4240-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a4240-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4240-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a4240-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4240-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a4240-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4240-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a4240-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a4240-148">Namespace</span></span><br/>                | <span data-ttu-id="a4240-149">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="a4240-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a4240-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4240-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4240-151">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="a4240-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a4240-152">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="a4240-152">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="a4240-153">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="a4240-153">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="a4240-154">Sicurezza degli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="a4240-154">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="a4240-155">Definizione dell'ereditarietà della sicurezza dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a4240-155">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="a4240-156">Elenchi di controllo di accesso (ACL)</span><span class="sxs-lookup"><span data-stu-id="a4240-156">Access Control Lists (ACLs)</span></span>](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[<span data-ttu-id="a4240-157">**Descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="a4240-157">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

