---
description: Enumerazione che descrive il tipo di connessione di rete in cui un profilo è applicabile.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo semplice iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80013fa21574221de24a7fc8309e4459a80ad670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526616"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span data-ttu-id="ad569-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Tipo semplice iwlanApplicabilityType</span><span class="sxs-lookup"><span data-stu-id="ad569-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>iwlanApplicabilityType Simple Type</span></span>

<span data-ttu-id="ad569-104">Enumerazione che descrive il tipo di connessione di rete in cui un profilo è applicabile.</span><span class="sxs-lookup"><span data-stu-id="ad569-104">Enumeration that describes the kind of network connection where a profile is applicable.</span></span>

``` syntax
<xs:simpleType name="iwlanApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="CellularOnly"
         />
        <xs:enumeration
            value="CellularAndIwlan"
         />
        <xs:enumeration
            value="IwlanOnly"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="ad569-105">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="ad569-105">Enumeration values</span></span>

<span data-ttu-id="ad569-106">Il tipo semplice **iwlanApplicabilityType** definisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad569-106">The **iwlanApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad569-107">Valore</span><span class="sxs-lookup"><span data-stu-id="ad569-107">Value</span></span></th>
<th><span data-ttu-id="ad569-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad569-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ad569-109">CellularOnly</span><span class="sxs-lookup"><span data-stu-id="ad569-109">CellularOnly</span></span></td>
<td><p><span data-ttu-id="ad569-110">Il profilo è valido solo per le connessioni di rete cellulare.</span><span class="sxs-lookup"><span data-stu-id="ad569-110">Profile is valid for cellular network connections only.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad569-111">CellularAndIwlan</span><span class="sxs-lookup"><span data-stu-id="ad569-111">CellularAndIwlan</span></span></td>
<td><p><span data-ttu-id="ad569-112">Il profilo è valido per le connessioni con offload cellulare o Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="ad569-112">Profile is valid for cellular or Wi-Fi offloaded connections.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad569-113">IwlanOnly</span><span class="sxs-lookup"><span data-stu-id="ad569-113">IwlanOnly</span></span></td>
<td><p><span data-ttu-id="ad569-114">Il profilo è valido solo per le connessioni di Wi-Fi offload.</span><span class="sxs-lookup"><span data-stu-id="ad569-114">Profile is valid for Wi-Fi offloaded connections only.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



