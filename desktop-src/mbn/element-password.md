---
description: MBNProfileExt \/ ... \/ Password (v4)
MS-HAID: WWAN\_profile\_v4.element\_Password
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Password
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5d8816c7-a3be-4a9c-a3e0-5c12230dc06f
api_name:
- Password
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c90b2481aa503b7b616d21fca24917b960a92dc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226197"
---
# <a name="span-idwwan_profile_v4element_passwordspanmbnprofileextpassword-v4"></a><span data-ttu-id="415bf-103"><span id="WWAN_profile_v4.element_Password"></span>MBNProfileExt \/ ... \/ Password (v4)</span><span class="sxs-lookup"><span data-stu-id="415bf-103"><span id="WWAN_profile_v4.element_Password"></span>MBNProfileExt\/...\/Password (v4)</span></span>

<span data-ttu-id="415bf-104">Specifica la password utilizzata per autenticare un utente.</span><span class="sxs-lookup"><span data-stu-id="415bf-104">Specifies the password used to authenticate a user.</span></span>

<span data-ttu-id="415bf-105">Per ulteriori informazioni, vedere la documentazione relativa all'elemento [**password**](./schema-password-userlogoncred-element.md) V1.</span><span class="sxs-lookup"><span data-stu-id="415bf-105">For more information, see the documentation for the v1 [**Password**](./schema-password-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="415bf-106">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="415bf-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<Password\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<Password\>**

## <a name="syntax"></a><span data-ttu-id="415bf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="415bf-107">Syntax</span></span>

``` syntax
<Password>

  string

</Password>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="415bf-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="415bf-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="415bf-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="415bf-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="415bf-110">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="415bf-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="415bf-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="415bf-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="415bf-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="415bf-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="415bf-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="415bf-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="415bf-114">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="415bf-114">Parent Element</span></span></th>
<th><span data-ttu-id="415bf-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="415bf-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="415bf-116"><a href="element-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="415bf-116"><a href="element-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="415bf-117">Credenziali di accesso per una connessione.</span><span class="sxs-lookup"><span data-stu-id="415bf-117">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="415bf-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="415bf-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="415bf-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="415bf-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
