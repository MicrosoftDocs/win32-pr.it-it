---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169aa9a34a561f65eed5dfc315e7711ef6bb9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343356"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span data-ttu-id="369ed-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span><span class="sxs-lookup"><span data-stu-id="369ed-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span></span>

<span data-ttu-id="369ed-104">L'elemento **IsAdditionalPdpContextProfile** contiene un **valore booleano** che è **true** se si tratta di un profilo "contesto aggiuntivo PDP (Packet Data Protocol)" e **false**, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="369ed-104">The **IsAdditionalPdpContextProfile** element contains a **boolean** that is **true** if this is an "additional PDP (Packet Data Protocol) context" profile and **false**, otherwise.</span></span> <span data-ttu-id="369ed-105">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="369ed-105">Default is **false**.</span></span>

<span data-ttu-id="369ed-106">Un profilo "contesto PDP aggiuntivo" è un profilo che non viene attivato sulla porta predefinita della scheda fisica e l'impostazione di questo elemento su true garantisce che il profilo non venga visualizzato in modo non appropriato nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="369ed-106">An "additional PDP context" profile is a profile that does not get activated over the physical adapter default port, and setting this element to true ensures that this profile is not displayed inappropriately in the user interface.</span></span>

<span data-ttu-id="369ed-107">Si noti che se questo elemento è impostato su true, deve essere true anche quanto segue.</span><span class="sxs-lookup"><span data-stu-id="369ed-107">Note that if this element is set to true, then the following must also be true.</span></span>

-   <span data-ttu-id="369ed-108">L'elemento [**IsDefault**](./schema-isdefault-mbnprofile-element.md) deve essere non specificato o impostato su **false** affinché il profilo sia valido.</span><span class="sxs-lookup"><span data-stu-id="369ed-108">The [**IsDefault**](./schema-isdefault-mbnprofile-element.md) element must be unspecified or set to **false** for the profile to be valid.</span></span>
-   <span data-ttu-id="369ed-109">L'elemento [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) non deve essere specificato o impostato su **Manual** affinché il profilo sia valido.</span><span class="sxs-lookup"><span data-stu-id="369ed-109">The [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) element must be unspecified or set to **manual** for the profile to be valid.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="369ed-110">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="369ed-110">Element hierarchy</span></span>

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a><span data-ttu-id="369ed-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="369ed-111">Syntax</span></span>

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="369ed-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="369ed-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="369ed-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="369ed-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="369ed-114">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="369ed-114">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="369ed-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="369ed-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="369ed-116">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="369ed-116">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="369ed-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="369ed-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="369ed-118">Questo elemento (documento) più esterno potrebbe non essere contenuto da altri elementi.</span><span class="sxs-lookup"><span data-stu-id="369ed-118">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="369ed-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="369ed-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="369ed-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="369ed-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
