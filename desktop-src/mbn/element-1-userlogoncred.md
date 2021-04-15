---
description: ModemDMConfigProfile \/ ... \/ UserLogonCred (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserLogonCred
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d563cf8-ea40-46b3-a74e-ec7640ca9824
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ff222738c591f6445e835e59662259dc744add98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484852"
---
# <a name="span-idwwan_profile_v4element_1_userlogoncredspanmodemdmconfigprofileuserlogoncred-v4"></a><span data-ttu-id="e46ec-103"><span id="WWAN_profile_v4.element_1_UserLogonCred"></span>ModemDMConfigProfile \/ ... \/ UserLogonCred (v4)</span><span class="sxs-lookup"><span data-stu-id="e46ec-103"><span id="WWAN_profile_v4.element_1_UserLogonCred"></span>ModemDMConfigProfile\/...\/UserLogonCred (v4)</span></span>

<span data-ttu-id="e46ec-104">Credenziali di accesso per una connessione.</span><span class="sxs-lookup"><span data-stu-id="e46ec-104">Logon credentials for a connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="e46ec-105">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="e46ec-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a><span data-ttu-id="e46ec-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e46ec-106">Syntax</span></span>

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a><span data-ttu-id="e46ec-107">Chiave</span><span class="sxs-lookup"><span data-stu-id="e46ec-107">Key</span></span>

<span data-ttu-id="e46ec-108">`?`   facoltativo (zero o uno)</span><span class="sxs-lookup"><span data-stu-id="e46ec-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="e46ec-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="e46ec-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="e46ec-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="e46ec-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="e46ec-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="e46ec-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="e46ec-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e46ec-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e46ec-113">Elemento figlio</span><span class="sxs-lookup"><span data-stu-id="e46ec-113">Child Element</span></span></th>
<th><span data-ttu-id="e46ec-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e46ec-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e46ec-115"><a href="element-1-ignorepassword.md">IgnorePassword</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-115"><a href="element-1-ignorepassword.md">IgnorePassword</a></span></span></td>
<td><p><span data-ttu-id="e46ec-116">Specifica il modo in cui vengono gestite le password durante l'aggiornamento dei profili.</span><span class="sxs-lookup"><span data-stu-id="e46ec-116">Specifies how passwords are handled when upgrading profiles.</span></span></p>
<p><span data-ttu-id="e46ec-117">Se è impostato su <strong>true</strong> e al momento dell'operazione di aggiornamento esiste un profilo con lo stesso nome, la password del profilo verrà acquisita e archiviata nel nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="e46ec-117">If set to <strong>TRUE</strong> and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span></p>
<p><span data-ttu-id="e46ec-118">Per altri dettagli, vedere la documentazione per l'elemento V1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e46ec-118">For more details, see the documentation for the v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e46ec-119"><a href="element-1-password.md">Password</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-119"><a href="element-1-password.md">Password</a></span></span></td>
<td><p><span data-ttu-id="e46ec-120">Specifica la password utilizzata per autenticare un utente.</span><span class="sxs-lookup"><span data-stu-id="e46ec-120">Specifies the password used to authenticate a user.</span></span></p>
<p><span data-ttu-id="e46ec-121">Per ulteriori informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-password-userlogoncred-element.md"><strong>password</strong></a> V1.</span><span class="sxs-lookup"><span data-stu-id="e46ec-121">For more information, see the documentation for the v1 <a href="../mbn/schema-password-userlogoncred-element.md"><strong>Password</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e46ec-122"><a href="element-1-username.md">UserName</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-122"><a href="element-1-username.md">UserName</a></span></span></td>
<td><p><span data-ttu-id="e46ec-123">Nome utente da utilizzare per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="e46ec-123">The user name to use for logon.</span></span></p>
<p><span data-ttu-id="e46ec-124">Per altri dettagli, vedere la documentazione per l'elemento <a href="../mbn/schema-username-userlogoncred-element.md"><strong>nome utente</strong></a> V1.</span><span class="sxs-lookup"><span data-stu-id="e46ec-124">For more details, see the documentation for the v1 <a href="../mbn/schema-username-userlogoncred-element.md"><strong>UserName</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="e46ec-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="e46ec-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e46ec-126">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e46ec-126">Parent Element</span></span></th>
<th><span data-ttu-id="e46ec-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e46ec-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e46ec-128"><a href="element-1-context.md">Contesto</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-128"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="e46ec-129">Specifica i parametri necessari per stabilire una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="e46ec-129">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="e46ec-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e46ec-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e46ec-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e46ec-131">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



