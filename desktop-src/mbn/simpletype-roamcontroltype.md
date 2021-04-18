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
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Tipo semplice roamControlType

Descrive il modo in cui il profilo controlla il roaming.

Esistono due possibili stati di registrazione roaming:

-   Partner: registrato in una rete strettamente collegata alla rete domestica
-   Non partner: registrato in una rete non strettamente affiliata alla rete domestica

Il significato esatto di "partner" varia a seconda della rete, ma rappresenta una relazione più stretta con tariffe più favorevoli rispetto a un non partner. Questa situazione può verificarsi se un operatore basato su aree ha una disposizione aziendale per usare la rete di accesso radiofonico di un altro operatore al di fuori dell'area di residenza. Potrebbe anche rappresentare la differenza tra il roaming all'interno di un'area (ad esempio, l'Unione europea) e all'esterno.

Si noti che [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) è un attributo più espressivo di **roamControlType** e un profilo deve usare **roamControlType** o **roamApplicabilityType**, ma non entrambi. Se un profilo usa entrambi, vengono applicati entrambi. Il risultato è l'intersezione dei due.

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

## <a name="enumeration-values"></a>Valori di enumerazione

Il tipo semplice **roamControlType** definisce i valori seguenti.

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
<td>AllRoamAllowed</td>
<td><p>Il roaming è consentito nelle reti partner e non partner.</p></td>
</tr>
<tr class="even">
<td>PartnerRoamAllowed</td>
<td><p>Il roaming è consentito solo nelle reti partner.</p></td>
</tr>
<tr class="odd">
<td>NoRoamAllowed</td>
<td><p>Nessun roaming consentito.</p></td>
</tr>
</tbody>
</table>

 

 



