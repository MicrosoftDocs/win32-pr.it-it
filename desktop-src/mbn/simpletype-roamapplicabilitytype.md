---
description: RoamApplicabilityType descrive le condizioni di roaming a cui si applica un profilo mobile.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo semplice roamApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2ce8f24e0987d5e8463838b33d4f2f2cf859da
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474757"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Tipo semplice roamApplicabilityType

RoamApplicabilityType descrive le condizioni di roaming a cui si applica un profilo mobile.

Si tratta di un attributo più espressivo rispetto a [**roamControlType**](simpletype-roamcontroltype.md)e un profilo deve usare **roamControlType** o **roamApplicabilityType**, ma non entrambi. Se un profilo usa entrambi, vengono applicati entrambi. Il risultato è l'intersezione dei due.

Usare questo attributo per distinguere tra più profili con condizioni di roaming non contigue, per specificare attributi del profilo diversi per, ad esempio, home rispetto al roaming.

Esistono tre possibili stati di registrazione home/roaming:

-   Home: registrato nella rete domestica
-   Partner: registrato in una rete strettamente affiliata alla rete domestica
-   Non partner: registrato in una rete non strettamente affiliata alla rete domestica

Il significato preciso di "partner" varia in base alla rete, ma rappresenta una relazione più stretta con tariffe più vantaggiose rispetto a un non partner. Ciò può verificarsi se un operatore locale ha una disposizione aziendale per usare la rete di accesso radio di un altro operatore al di fuori della propria area domestica. Può anche rappresentare la differenza tra roaming all'interno di un'area (ad esempio, UE) e all'esterno di essa.

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

Il **tipo semplice roamApplicabilityType** definisce i valori seguenti.


| valore | Descrizione | 
|-------|-------------|
| NonPartnerOnly | <p>Questo profilo viene usato solo quando si esegue il roaming in una rete non partner</p> | 
| PartnerOnly | <p>Questo profilo viene usato solo quando si esegue il roaming in una rete partner</p> | 
| HomeOnly | <p>Questo profilo viene usato solo nella rete domestica</p> | 
| HomeAndPartner | <p>Questo profilo viene usato solo quando si è a casa o in una rete partner</p> | 
| PartnerAndNonpartner | <p>Questo profilo viene usato quando non è a casa (roaming in qualsiasi rete)</p> | 
| AllRoaming | <p>Questo profilo viene usato in tutte le reti</p> | 


 

 



