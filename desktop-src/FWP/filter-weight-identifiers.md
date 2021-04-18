---
title: Identificatori di peso del filtro (Fwpmu. h)
description: Filtrare gli identificatori di peso usati dal motore di filtro di base (BFE) per calcolare i pesi dei filtri generati automaticamente.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302354"
---
# <a name="filter-weight-identifiers"></a>Identificatori di peso del filtro

Di seguito sono elencati gli identificatori di peso del filtro usati dal motore di filtro di base (BFE) per calcolare i pesi dei filtri generati automaticamente.

Per altre informazioni sulla generazione del peso del filtro, vedere [assegnazione del peso del filtro](filter-weight-assignment.md) .

<dl> <dt>

<span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**\_bit di \_ peso \_ automatico FWPM**
</dt> <dd> <dl> <dt>

(60)
</dt> <dt>



Numero di bit utilizzati per i pesi di filtro generati automaticamente.


</dt> </dl> </dd> <dt>

<span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**\_ \_ Max peso automatico \_ FWPM**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 4)
</dt> <dt>



Peso massimo del filtro generato automaticamente.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**
</dt> <dd> <dl> <dt>

0xC
</dt> <dt>



BFE assegna un peso con questo valore di intervallo ai filtri IKE e AuthIP.

Per ulteriori informazioni sui filtri IKE/AuthIP, vedere [esenzioni IKE/AuthIP](ike-exemptions.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**\_IPSec FWPM intervallo di ponderazione \_ \_**
</dt> <dd> <dl> <dt>

(0x0)
</dt> <dt>



BFE assegna un peso con questo valore di intervallo ai filtri dei criteri IPsec.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**\_Max FWPM intervallo di ponderazione \_ \_**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 60)
</dt> <dt>



Valore massimo dell'intervallo di ponderazione del filtro consentito.


</dt> </dl> </dd> </dl>

> [!Note]  
> **MAXUINT64** rappresenta il valore massimo possibile di **UInt64**. Il valore di questa costante è 0xFFFFFFFFFFFFFFFF.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





