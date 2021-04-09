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
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Tipo semplice roamApplicabilityType

RoamApplicabilityType descrive le condizioni di roaming per le quali viene applicato un profilo mobile.

Si tratta di un attributo più espressivo di [**roamControlType**](simpletype-roamcontroltype.md)e un profilo deve usare **roamControlType** o **roamApplicabilityType**, ma non entrambi. Se un profilo usa entrambi, vengono applicati entrambi. Il risultato è l'intersezione dei due.

Utilizzare questo attributo per distinguere tra più profili con condizioni di roaming non contigue, per specificare diversi attributi del profilo per, ad esempio, Home e roaming.

Esistono tre possibili stati di registrazione di casa/roaming:

-   Home page: registrato nella rete domestica
-   Partner: registrato in una rete strettamente collegata alla rete domestica
-   Non partner: registrato in una rete non strettamente affiliata alla rete domestica

Il significato esatto di "partner" varia a seconda della rete, ma rappresenta una relazione più stretta con tariffe più favorevoli rispetto a un non partner. Questa situazione può verificarsi se un operatore basato su aree ha una disposizione aziendale per usare la rete di accesso radiofonico di un altro operatore al di fuori dell'area di residenza. Potrebbe anche rappresentare la differenza tra il roaming all'interno di un'area (ad esempio, l'Unione europea) e all'esterno.

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

## <a name="enumeration-values"></a>Valori di enumerazione

Il tipo semplice **roamApplicabilityType** definisce i valori seguenti.

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
<td>NonPartnerOnly</td>
<td><p>Questo profilo viene usato solo quando si esegue il roaming in una rete non partner</p></td>
</tr>
<tr class="even">
<td>PartnerOnly</td>
<td><p>Questo profilo viene usato solo quando si esegue il roaming in una rete partner</p></td>
</tr>
<tr class="odd">
<td>HomeOnly</td>
<td><p>Questo profilo viene usato solo quando si usa la rete domestica</p></td>
</tr>
<tr class="even">
<td>HomeAndPartner</td>
<td><p>Questo profilo viene usato solo quando si è a casa o in una rete partner</p></td>
</tr>
<tr class="odd">
<td>PartnerAndNonpartner</td>
<td><p>Questo profilo viene usato quando non è a casa (roaming in qualsiasi rete)</p></td>
</tr>
<tr class="even">
<td>AllRoaming</td>
<td><p>Questo profilo viene usato in tutte le reti</p></td>
</tr>
</tbody>
</table>

 

 



