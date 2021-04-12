---
description: ModemDMConfigProfile \/ ... \/ AuthProtocol (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_AuthProtocol
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AuthProtocol
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5e6c5a25-fe9e-4d0a-8b5b-4ff585f562af
api_name:
- AuthProtocol
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7a935d7367589a3043fdd9d064935d0c0dd64b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526052"
---
# <a name="span-idwwan_profile_v4element_1_authprotocolspanmodemdmconfigprofileauthprotocol-v4"></a><span data-ttu-id="90838-103"><span id="WWAN_profile_v4.element_1_AuthProtocol"></span>ModemDMConfigProfile \/ ... \/ AuthProtocol (v4)</span><span class="sxs-lookup"><span data-stu-id="90838-103"><span id="WWAN_profile_v4.element_1_AuthProtocol"></span>ModemDMConfigProfile\/...\/AuthProtocol (v4)</span></span>

><span data-ttu-id="90838-104">Specifica il protocollo di autenticazione da utilizzare per l'attivazione di un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="90838-104">Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="90838-105">Si noti che in V4 è disponibile un nuovo valore di enumerazione per questo elemento.</span><span class="sxs-lookup"><span data-stu-id="90838-105">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="90838-106">La **selezione di autoselezione** indica che un protocollo di autenticazione deve essere prelevato da uno o più livelli inferiori.</span><span class="sxs-lookup"><span data-stu-id="90838-106">**AutoSelection** means that an auth protocol is to be picked by lower layer(s).</span></span>

<span data-ttu-id="90838-107">Per ulteriori informazioni, vedere la documentazione per l'elemento V1 [**AuthProtocol**](./schema-authprotocol-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="90838-107">For further information, see the documentation for the v1 [**AuthProtocol**](./schema-authprotocol-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="90838-108">Gerarchia degli elementi</span><span class="sxs-lookup"><span data-stu-id="90838-108">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

## <a name="syntax"></a><span data-ttu-id="90838-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90838-109">Syntax</span></span>

``` syntax
<AuthProtocol>

  "NONE" | "PAP" | "CHAP" | "MsCHAPv2" | "AutoSelection"

</AuthProtocol>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="90838-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="90838-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="90838-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="90838-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="90838-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="90838-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="90838-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="90838-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="90838-114">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="90838-114">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="90838-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre</span><span class="sxs-lookup"><span data-stu-id="90838-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90838-116">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="90838-116">Parent Element</span></span></th>
<th><span data-ttu-id="90838-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90838-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90838-118"><a href="element-1-context.md">Contesto</a></span><span class="sxs-lookup"><span data-stu-id="90838-118"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="90838-119">Specifica i parametri necessari per stabilire una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="90838-119">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="90838-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90838-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90838-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="90838-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
