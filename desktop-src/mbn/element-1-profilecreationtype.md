---
description: ProfileCreationType (in ModemDMConfigProfile)
MS-HAID: WWAN\_profile\_v4.element\_1\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (in ModemDMConfigProfile)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b755840d0308ec2d7a7bba5896b0cf67b7b61198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879158"
---
# <a name="span-idwwan_profile_v4element_1_profilecreationtypespanprofilecreationtype-in-modemdmconfigprofile"></a><span data-ttu-id="ae1d0-103"><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (in ModemDMConfigProfile)</span><span class="sxs-lookup"><span data-stu-id="ae1d0-103"><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (in ModemDMConfigProfile)</span></span>

<span data-ttu-id="ae1d0-104">Specifica il modo in cui è stato creato il profilo DM del modem.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-104">Specifies how this modem DM profile was created.</span></span>

<span data-ttu-id="ae1d0-105">Questo valore viene usato per decidere se un utente può eliminare il profilo.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-105">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="ae1d0-106">Gli utenti possono eliminare solo i profili **UserProvisioned** .</span><span class="sxs-lookup"><span data-stu-id="ae1d0-106">Users can only delete **UserProvisioned** profiles.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="ae1d0-107">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="ae1d0-107">Element hierarchy</span></span>

[<ModemDMConfigProfile>](element-modemdmconfigprofile.md)  
**<ProfileCreationType>**

## <a name="syntax"></a><span data-ttu-id="ae1d0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae1d0-108">Syntax</span></span>

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="ae1d0-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="ae1d0-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="ae1d0-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="ae1d0-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="ae1d0-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="ae1d0-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ae1d0-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="ae1d0-113">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="ae1d0-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ae1d0-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae1d0-115">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="ae1d0-115">Parent Element</span></span></th>
<th><span data-ttu-id="ae1d0-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae1d0-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae1d0-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="ae1d0-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="ae1d0-118">Profilo di configurazione modem DM.</span><span class="sxs-lookup"><span data-stu-id="ae1d0-118">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="related-elements"></a><span data-ttu-id="ae1d0-119">Elementi correlati</span><span class="sxs-lookup"><span data-stu-id="ae1d0-119">Related elements</span></span>

<span data-ttu-id="ae1d0-120">Gli elementi seguenti hanno lo stesso nome di questo elemento, ma il contenuto o gli attributi sono diversi:</span><span class="sxs-lookup"><span data-stu-id="ae1d0-120">The following elements have the same name as this one, but different content or attributes:</span></span>

-   <span data-ttu-id="ae1d0-121">**[ProfileCreationType (in MBNProfileExt)](element-profilecreationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="ae1d0-121">**[ProfileCreationType (in MBNProfileExt)](element-profilecreationtype.md)**</span></span>

## <a name="requirements"></a><span data-ttu-id="ae1d0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae1d0-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae1d0-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ae1d0-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



