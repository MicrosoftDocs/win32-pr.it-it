---
description: Descrive il modo in cui il profilo controlla il roaming.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo semplice roamControlType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19243625c07afae49011638a37734a5515e626d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480237"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Tipo semplice roamControlType

Descrive il modo in cui il profilo controlla il roaming.

Esistono due possibili stati di registrazione di roaming:

-   Partner: registrato in una rete strettamente affiliata alla rete domestica
-   Non partner: registrato in una rete non strettamente affiliata alla rete domestica

Il significato preciso di "partner" varia in base alla rete, ma rappresenta una relazione più stretta con tariffe più vantaggiose rispetto a un non partner. Ciò può verificarsi se un operatore locale ha una disposizione aziendale per usare la rete di accesso radio di un altro operatore al di fuori della propria area domestica. Può anche rappresentare la differenza tra roaming all'interno di un'area (ad esempio, UE) e all'esterno di essa.

Si noti che [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) è un attributo più espressivo rispetto a **roamControlType** e un profilo deve usare **roamControlType** o **roamApplicabilityType**, ma non entrambi. Se un profilo usa entrambi, vengono applicati entrambi. Il risultato è l'intersezione dei due.

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

Il **tipo semplice roamControlType** definisce i valori seguenti.


| valore | Descrizione | 
|-------|-------------|
| AllRoamAllowed | <p>Il roaming è consentito nelle reti partner e non partner.</p> | 
| PartnerRoamAllowed | <p>Il roaming è consentito solo nelle reti partner.</p> | 
| NoRoamAllowed | <p>Non è consentito il roaming.</p> | 


 

 



