---
description: Descrive il modo in cui il profilo controlla il roaming.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo semplice roamControlType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911e379773e7d8eabfb7a1524b1a21ba16718a53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307526"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span data-ttu-id="a24d4-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Tipo semplice roamControlType</span><span class="sxs-lookup"><span data-stu-id="a24d4-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamControlType Simple Type</span></span>

<span data-ttu-id="a24d4-104">Descrive il modo in cui il profilo controlla il roaming.</span><span class="sxs-lookup"><span data-stu-id="a24d4-104">Describes how the profile controls roaming.</span></span>

<span data-ttu-id="a24d4-105">Esistono due possibili stati di registrazione roaming:</span><span class="sxs-lookup"><span data-stu-id="a24d4-105">There are two possible roam registration states:</span></span>

-   <span data-ttu-id="a24d4-106">Partner: registrato in una rete strettamente collegata alla rete domestica</span><span class="sxs-lookup"><span data-stu-id="a24d4-106">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="a24d4-107">Non partner: registrato in una rete non strettamente affiliata alla rete domestica</span><span class="sxs-lookup"><span data-stu-id="a24d4-107">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="a24d4-108">Il significato esatto di "partner" varia a seconda della rete, ma rappresenta una relazione più stretta con tariffe più favorevoli rispetto a un non partner.</span><span class="sxs-lookup"><span data-stu-id="a24d4-108">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="a24d4-109">Questa situazione può verificarsi se un operatore basato su aree ha una disposizione aziendale per usare la rete di accesso radiofonico di un altro operatore al di fuori dell'area di residenza.</span><span class="sxs-lookup"><span data-stu-id="a24d4-109">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="a24d4-110">Potrebbe anche rappresentare la differenza tra il roaming all'interno di un'area (ad esempio, l'Unione europea) e all'esterno.</span><span class="sxs-lookup"><span data-stu-id="a24d4-110">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

<span data-ttu-id="a24d4-111">Si noti che [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) è un attributo più espressivo di **roamControlType** e un profilo deve usare **roamControlType** o **roamApplicabilityType**, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="a24d4-111">Note that [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) is a more expressive attribute than **roamControlType**, and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="a24d4-112">Se un profilo usa entrambi, vengono applicati entrambi.</span><span class="sxs-lookup"><span data-stu-id="a24d4-112">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="a24d4-113">Il risultato è l'intersezione dei due.</span><span class="sxs-lookup"><span data-stu-id="a24d4-113">The result is the intersection of the two.)</span></span>

``` syntax
<xs:simpleType name="roamControlType">
    <xs:restriction>
        <xs:enumeration
            value="AllRoamAllowed"
         />
        <xs:enumeration
            value="PartnerRoamAllowed"
         />
        <xs:enumeration
            value="NoRoamAllowed"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="a24d4-114">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="a24d4-114">Enumeration values</span></span>

<span data-ttu-id="a24d4-115">Il tipo semplice **roamControlType** definisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a24d4-115">The **roamControlType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a24d4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a24d4-116">Value</span></span></th>
<th><span data-ttu-id="a24d4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a24d4-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a24d4-118">AllRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="a24d4-118">AllRoamAllowed</span></span></td>
<td><p><span data-ttu-id="a24d4-119">Il roaming è consentito nelle reti partner e non partner.</span><span class="sxs-lookup"><span data-stu-id="a24d4-119">Roaming is allowed on Partner and Non-Partner networks.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a24d4-120">PartnerRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="a24d4-120">PartnerRoamAllowed</span></span></td>
<td><p><span data-ttu-id="a24d4-121">Il roaming è consentito solo nelle reti partner.</span><span class="sxs-lookup"><span data-stu-id="a24d4-121">Roaming is allowed only on Partner networks.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a24d4-122">NoRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="a24d4-122">NoRoamAllowed</span></span></td>
<td><p><span data-ttu-id="a24d4-123">Nessun roaming consentito.</span><span class="sxs-lookup"><span data-stu-id="a24d4-123">No roaming is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



