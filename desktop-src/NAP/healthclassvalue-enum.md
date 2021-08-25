---
title: Enumerazione HealthClassValue (NapProtocol.h)
description: Indica il valore della classe di integrità TLV.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- Enumerazione HealthClassValue NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76b3fef268417f14bf22d2e25539a245cebc31820b746847f1e7b1091492b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891641"
---
# <a name="healthclassvalue-enumeration"></a>Enumerazione HealthClassValue

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **tipo di enumerazione HealthClassValue** indica il valore della classe di integrità TLV.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**
</dt> <dd>

La classe di integrità TLV è firewall.

</dd> <dt>

<span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**
</dt> <dd>

La classe di integrità TLV è a livello di patch.

</dd> <dt>

<span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**
</dt> <dd>

La classe di integrità TLV è antivirus.

</dd> <dt>

<span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**
</dt> <dd>

La classe di integrità TLV è un aggiornamento critico.

</dd> <dt>

<span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**
</dt> <dd>

Riservato solo per l'uso del sistema.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |



 

 





