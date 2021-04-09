---
description: RoamApplicabilityType descrive le condizioni di roaming per le quali viene applicato un profilo mobile.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo semplice roamApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d81214ab5a44dcac60bb5e1a6accc81b0d0418
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879149"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span data-ttu-id="aa9fb-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Tipo semplice roamApplicabilityType</span><span class="sxs-lookup"><span data-stu-id="aa9fb-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType Simple Type</span></span>

<span data-ttu-id="aa9fb-104">RoamApplicabilityType descrive le condizioni di roaming per le quali viene applicato un profilo mobile.</span><span class="sxs-lookup"><span data-stu-id="aa9fb-104">The roamApplicabilityType describes the roaming conditions for which a roaming profile applies.</span></span>

<span data-ttu-id="aa9fb-105">Si tratta di un attributo più espressivo di [**roamControlType**](simpletype-roamcontroltype.md)e un profilo deve usare **roamControlType** o **roamApplicabilityType**, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="aa9fb-105">This is a more expressive attribute than [**roamControlType**](simpletype-roamcontroltype.md), and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="aa9fb-106">Se un profilo usa entrambi, vengono applicati entrambi.</span><span class="sxs-lookup"><span data-stu-id="aa9fb-106">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="aa9fb-107">Il risultato è l'intersezione dei due.</span><span class="sxs-lookup"><span data-stu-id="aa9fb-107">The result is the intersection of the two.)</span></span>

<span data-ttu-id="aa9fb-108">Utilizzare questo attributo per distinguere tra più profili con condizioni di roaming non contigue, per specificare diversi attributi del profilo per, ad esempio, Home e roaming.</span><span class="sxs-lookup"><span data-stu-id="aa9fb-108">Use this attribute to differentiate between multiple profiles with disjoint roaming conditions, to specify different profile attributes for, for example, home versus roaming.</span></span>

<span data-ttu-id="aa9fb-109">Esistono tre possibili stati di registrazione di casa/roaming:</span><span class="sxs-lookup"><span data-stu-id="aa9fb-109">There are three possible home/roam registration states:</span></span>

-   <span data-ttu-id="aa9fb-110">Home page: registrato nella rete domestica</span><span class="sxs-lookup"><span data-stu-id="aa9fb-110">Home: registered on the home network</span></span>
-   <span data-ttu-id="aa9fb-111">Partner: registrato in una rete strettamente collegata alla rete domestica</span><span class="sxs-lookup"><span data-stu-id="aa9fb-111">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="aa9fb-112">Non partner: registrato in una rete non strettamente affiliata alla rete domestica</span><span class="sxs-lookup"><span data-stu-id="aa9fb-112">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="aa9fb-113">Il significato esatto di "partner" varia a seconda della rete, ma rappresenta una relazione più stretta con tariffe più favorevoli rispetto a un non partner.</span><span class="sxs-lookup"><span data-stu-id="aa9fb-113">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="aa9fb-114">Questa situazione può verificarsi se un operatore basato su aree ha una disposizione aziendale per usare la rete di accesso radiofonico di un altro operatore al di fuori dell'area di residenza.</span><span class="sxs-lookup"><span data-stu-id="aa9fb-114">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="aa9fb-115">Potrebbe anche rappresentare la differenza tra il roaming all'interno di un'area (ad esempio, l'Unione europea) e all'esterno.</span><span class="sxs-lookup"><span data-stu-id="aa9fb-115">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

``` syntax
<xs:simpleType name="roamApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="NonPartnerOnly"
         />
        <xs:enumeration
            value="PartnerOnly"
         />
        <xs:enumeration
            value="HomeOnly"
         />
        <xs:enumeration
            value="HomeAndPartner"
         />
        <xs:enumeration
            value="PartnerAndNonpartner"
         />
        <xs:enumeration
            value="AllRoaming"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="aa9fb-116">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="aa9fb-116">Enumeration values</span></span>

<span data-ttu-id="aa9fb-117">Il tipo semplice **roamApplicabilityType** definisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="aa9fb-117">The **roamApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa9fb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="aa9fb-118">Value</span></span></th>
<th><span data-ttu-id="aa9fb-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa9fb-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa9fb-120">NonPartnerOnly</span><span class="sxs-lookup"><span data-stu-id="aa9fb-120">NonPartnerOnly</span></span></td>
<td><p><span data-ttu-id="aa9fb-121">Questo profilo viene usato solo quando si esegue il roaming in una rete non partner</span><span class="sxs-lookup"><span data-stu-id="aa9fb-121">This profile is used only when roaming on a non-partner network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa9fb-122">PartnerOnly</span><span class="sxs-lookup"><span data-stu-id="aa9fb-122">PartnerOnly</span></span></td>
<td><p><span data-ttu-id="aa9fb-123">Questo profilo viene usato solo quando si esegue il roaming in una rete partner</span><span class="sxs-lookup"><span data-stu-id="aa9fb-123">This profile is used only when roaming on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa9fb-124">HomeOnly</span><span class="sxs-lookup"><span data-stu-id="aa9fb-124">HomeOnly</span></span></td>
<td><p><span data-ttu-id="aa9fb-125">Questo profilo viene usato solo quando si usa la rete domestica</span><span class="sxs-lookup"><span data-stu-id="aa9fb-125">This profile is used only when on the home network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa9fb-126">HomeAndPartner</span><span class="sxs-lookup"><span data-stu-id="aa9fb-126">HomeAndPartner</span></span></td>
<td><p><span data-ttu-id="aa9fb-127">Questo profilo viene usato solo quando si è a casa o in una rete partner</span><span class="sxs-lookup"><span data-stu-id="aa9fb-127">This profile is used only when at home or on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa9fb-128">PartnerAndNonpartner</span><span class="sxs-lookup"><span data-stu-id="aa9fb-128">PartnerAndNonpartner</span></span></td>
<td><p><span data-ttu-id="aa9fb-129">Questo profilo viene usato quando non è a casa (roaming in qualsiasi rete)</span><span class="sxs-lookup"><span data-stu-id="aa9fb-129">This profile is used when not at home (roaming on any network)</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa9fb-130">AllRoaming</span><span class="sxs-lookup"><span data-stu-id="aa9fb-130">AllRoaming</span></span></td>
<td><p><span data-ttu-id="aa9fb-131">Questo profilo viene usato in tutte le reti</span><span class="sxs-lookup"><span data-stu-id="aa9fb-131">This profile is used on all networks</span></span></p></td>
</tr>
</tbody>
</table>

 

 



