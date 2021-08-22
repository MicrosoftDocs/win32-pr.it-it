---
title: MPSCAN_TYPE enumerazione (MpClient.h)
description: Tipo di analisi eseguita.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE funzionalità dell'ambiente Windows legacy
- PMPSCAN_TYPE puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: 56906bfc9ad57f93bac4c8b8c27360b5ade9592ac33efe39574fe8890299e13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747132"
---
# <a name="mpscan_type-enumeration"></a>Enumerazione MPSCAN \_ TYPE

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

<span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**TIPO MPSCAN \_ \_ SCONOSCIUTO**
</dt> <dd>

Solo per uso interno.

</dd> <dt>

<span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN \_ TYPE \_ QUICK**
</dt> <dd>

Analizza i processi in esecuzione e vari punti asep nel sistema in cui il malware in genere si nasconde.

</dd> <dt>

<span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**TIPO MPSCAN \_ \_ COMPLETO**
</dt> <dd>

Esegue un'analisi veloce seguita dall'analisi di tutte le unità fisse del sistema.

</dd> <dt>

<span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**RISORSA DI TIPO MPSCAN \_ \_**
</dt> <dd>

Analizza risorse specifiche, ad esempio file o cartelle.

</dd> <dt>

<span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**TIPO MPSCAN \_ \_ MAXVALUE**
</dt> <dd>

Valore massimo possibile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





