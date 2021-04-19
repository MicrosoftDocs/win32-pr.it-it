---
description: ModemDMConfigProfile \/ ... \/ IgnorePassword (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_IgnorePassword
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IgnorePassword (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0286fcc7a025bc565916e68b817c6a79f378f26d
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388791"
---
# <a name="span-idwwan_profile_v4element_1_ignorepasswordspanmodemdmconfigprofileignorepassword-v4"></a><span data-ttu-id="0ac64-103"><span id="WWAN_profile_v4.element_1_IgnorePassword"></span>ModemDMConfigProfile \/ ... \/ IgnorePassword (v4)</span><span class="sxs-lookup"><span data-stu-id="0ac64-103"><span id="WWAN_profile_v4.element_1_IgnorePassword"></span>ModemDMConfigProfile\/...\/IgnorePassword (v4)</span></span>

<span data-ttu-id="0ac64-104">Specifica il modo in cui vengono gestite le password durante l'aggiornamento dei profili.</span><span class="sxs-lookup"><span data-stu-id="0ac64-104">Specifies how passwords are handled when upgrading profiles.</span></span>

<span data-ttu-id="0ac64-105">Se è impostato su **true** e al momento dell'operazione di aggiornamento esiste un profilo con lo stesso nome, la password del profilo verrà acquisita e archiviata nel nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="0ac64-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span>

<span data-ttu-id="0ac64-106">Per altri dettagli, vedere la documentazione per l'elemento V1 [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0ac64-106">For more details, see the documentation for the v1 [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="0ac64-107">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="0ac64-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

## <a name="syntax"></a><span data-ttu-id="0ac64-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ac64-108">Syntax</span></span>

``` syntax
<IgnorePassword>

  boolean

</IgnorePassword>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="0ac64-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="0ac64-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="0ac64-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="0ac64-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="0ac64-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="0ac64-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="0ac64-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0ac64-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="0ac64-113">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="0ac64-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="0ac64-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0ac64-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ac64-115">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="0ac64-115">Parent Element</span></span></th>
<th><span data-ttu-id="0ac64-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ac64-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ac64-117"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="0ac64-117"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="0ac64-118">Credenziali di accesso per una connessione.</span><span class="sxs-lookup"><span data-stu-id="0ac64-118">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="0ac64-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ac64-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ac64-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0ac64-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
