---
description: Enumerazione che descrive il tipo di connessione di rete in cui è applicabile un profilo.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo semplice iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529ae39c2b0e137825e7a80d41c43203b0a27de7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478957"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Tipo semplice iwlanApplicabilityType

Enumerazione che descrive il tipo di connessione di rete in cui è applicabile un profilo.

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


| valore | Descrizione | 
|-------|-------------|
| CellularOnly | <p>Il profilo è valido solo per le connessioni di rete cellulare.</p> | 
| CellularAndIwlan | <p>Il profilo è valido per le connessioni Wi-Fi o offloaded.</p> | 
| IwlanOnly | <p>Il profilo è valido Wi-Fi solo connessioni offloaded.</p> | 


 

 



