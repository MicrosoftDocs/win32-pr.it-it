---
title: Enumerazione MPSCAN_TYPE (MpClient. h)
description: Tipo di analisi eseguita.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPSCAN_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPSCAN_TYPE
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb89137dc9cfe5b8a4ff1f44a7a101239aa3a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740135"
---
# <a name="mpscan_type-enumeration"></a>\_Enumerazione del tipo MPSCAN

Tipo di analisi eseguita.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**\_tipo MPSCAN \_ sconosciuto**
</dt> <dd>

Solo per uso interno.

</dd> <dt>

<span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN \_ tipo \_ rapido**
</dt> <dd>

Esegue l'analisi dei processi in esecuzione e di diversi punti di l'oggetto in cui il malware si nasconde in genere.

</dd> <dt>

<span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**tipo di MPSCAN \_ \_ completo**
</dt> <dd>

Esegue un'analisi veloce seguita dall'analisi di tutte le unità fisse del sistema.

</dd> <dt>

<span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**\_risorsa di tipo MPSCAN \_**
</dt> <dd>

Analizza risorse specifiche, ad esempio file o cartelle.

</dd> <dt>

<span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN di \_ tipo \_ MaxValue**
</dt> <dd>

Valore massimo possibile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





