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
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Tipo semplice iwlanApplicabilityType

Enumerazione che descrive il tipo di connessione di rete in cui un profilo è applicabile.

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

## <a name="enumeration-values"></a>Valori di enumerazione

Il tipo semplice **iwlanApplicabilityType** definisce i valori seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CellularOnly</td>
<td><p>Il profilo è valido solo per le connessioni di rete cellulare.</p></td>
</tr>
<tr class="even">
<td>CellularAndIwlan</td>
<td><p>Il profilo è valido per le connessioni con offload cellulare o Wi-Fi.</p></td>
</tr>
<tr class="odd">
<td>IwlanOnly</td>
<td><p>Il profilo è valido solo per le connessioni di Wi-Fi offload.</p></td>
</tr>
</tbody>
</table>

 

 



