---
title: Struttura MPCALLBACK_DATA (MpClient. h)
description: Dati passati alla funzione di callback.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- Struttura MPCALLBACK_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCALLBACK_DATA
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119674"
---
# <a name="mpcallback_data-structure"></a>\_Struttura dei dati MPCALLBACK

Dati passati alla funzione di callback.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**Notificare**
</dt> <dd>

Tipo: **[ **MPNOTIFY**](mpnotify.md)**

</dd> <dd>

Notifica di modifica per il report.

</dd> <dt>

**hResult**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Codice di errore, in caso di errore interno.

</dd> <dt>

**TimeStamp**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Timestamp corrente.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **MPCALLBACK \_**](mpcallback-type.md)**

</dd> <dd>

Tipo di dati speciale di callback.

</dd> <dt>

**Dati**
</dt> <dd>

Richiamata di dati speciali. Il puntatore alla struttura appropriata dipende dal valore di **tipo**.

<dl> <dt>

**pStatusData**
</dt> <dd>

Tipo: **PMPSTATUS \_ Data**

</dd> <dd>

Quando **digitare**  ==  **MPCALLBACK \_ status**. Vedere [**MPSTATUS \_ Data**](mpstatus-data.md).

</dd> <dt>

**pScanData**
</dt> <dd>

Tipo: **PMPSCAN \_ Data**

</dd> <dd>

Quando si **digita**  ==  **MPCALLBACK \_ Scan**. Vedere [**MPSCAN \_ Data**](mpscan-data.md).

</dd> <dt>

**pCleanData**
</dt> <dd>

Tipo: **PMPCLEAN \_ Data**

</dd> <dd>

Quando il **tipo**  ==  **MPCALLBACK è \_ Clean**. Vedere [**MPCLEAN \_ Data**](mpclean-data.md).

</dd> <dt>

**pPrecheckData**
</dt> <dd>

Tipo: **PMPCLEAN \_ Precheck \_ dati**

</dd> <dd>

Quando il **tipo**  ==  **MPCALLBACK è \_ Precheck**. Vedere [**MPCLEAN \_ Precheck \_ Data**](mpclean-precheck-data.md).

</dd> <dt>

**pThreatData**
</dt> <dd>

Tipo: **PMPTHREAT \_ Data**

</dd> <dd>

Quando **digitare**  ==  **MPCALLBACK \_ Threat**. Vedere [**MPTHREAT \_ Data**](mpthreat-data.md).

</dd> <dt>

**pSigUpdateData**
</dt> <dd>

Tipo: **PMPSIGUPDATE \_ Data**

</dd> <dd>

Quando il **tipo** è  ==  **MPCALLBACK \_ SIGUPDATE**. Vedere [**MPSIGUPDATE \_ Data**](mpsigupdate-data.md).

</dd> <dt>

**pSampleData**
</dt> <dd>

Tipo: **PMPSAMPLE \_ Data**

</dd> <dd>

Quando si **digita**  ==  **MPCALLBACK \_ Sample**. Vedere [**MPSAMPLE \_ Data**](mpsample-data.md).

</dd> <dt>

**pReservedData**
</dt> <dd>

Tipo: **PMPRESERVED \_ Data**

</dd> <dd>

Quando il **tipo**  ==  **MPCALLBACK è \_ riservato**. Vedere [**MPRESERVED \_ Data**](mpreserved-data.md).

</dd> <dt>

**pConfigurationData**
</dt> <dd>

Tipo: **PMPCONFIGURATION \_ Data**

</dd> <dd>

Quando si **digita** la  ==  **\_ \_ notifica di configurazione MPCALLBACK**. Vedere [**MPCONFIGURATION \_ Data**](mpconfiguration-data.md).

</dd> <dt>

**pFastPathData**
</dt> <dd>

Tipo: **PMPFASTPATH \_ Data**

</dd> <dd>

Quando il **tipo** è  ==  **MPCALLBACK \_ FastPath**. Vedere [**MPFASTPATH \_ Data**](mpfastpath-data.md).

</dd> <dt>

**pExpirationData**
</dt> <dd>

Tipo: **PMPEXPIRATION \_ Data**

</dd> <dd>

Quando il **tipo**  ==  **MPCALLBACK \_ \_ scadenza del prodotto**. Vedere [**MPEXPIRATION \_ Data**](mpexpiration-data.md).

</dd> <dt>

**pNISPrivateData**
</dt> <dd>

Tipo: **PMPNIS \_ private \_ Data**

</dd> <dd>

Quando il **tipo**  ==  **MPCALLBACK \_ NIS è \_ privato**. Vedere [**MPNIS \_ private \_ Data**](mpnis-private-data.md).

</dd> <dt>

**pHealthData**
</dt> <dd>

Tipo: **PMPHEALTH \_ Data**

</dd> <dd>

Quando **digitare**  ==  **MPCALLBACK \_ Health**. Vedere [**MPHEALTH \_ Data**](mphealth-data.md).

</dd> <dt>

**pEndOfLifeData**
</dt> <dd>

Tipo: **PMPENDOFLIFE \_ Data**

</dd> <dd>

Quando il **tipo** è  ==  **MPCALLBACK \_ ENDOFLIFE**. Vedere [**MPENDOFLIFE \_ Data**](mpendoflife-data.md).

</dd> <dt>

**pMalwareToastData**
</dt> <dd>

Tipo: **PMPMALWARETOAST \_ Data**

</dd> <dd>

Quando il **tipo** è  ==  **MPCALLBACK \_ MALWARETOAST**. Vedere [**MPMALWARETOAST \_ Data**](mpmalwaretoast-data.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tipo MPCALLBACK**](mpcallback-type.md)
</dt> <dt>

[**\_dati MPCLEAN**](mpclean-data.md)
</dt> <dt>

[**MPCLEAN \_ i dati di PREverifica \_**](mpclean-precheck-data.md)
</dt> <dt>

[**\_dati MPCONFIGURATION**](mpconfiguration-data.md)
</dt> <dt>

[**\_dati MPENDOFLIFE**](mpendoflife-data.md)
</dt> <dt>

[**\_dati MPEXPIRATION**](mpexpiration-data.md)
</dt> <dt>

[**\_dati MPFASTPATH**](mpfastpath-data.md)
</dt> <dt>

[**\_dati MPHEALTH**](mphealth-data.md)
</dt> <dt>

[**\_dati MPMALWARETOAST**](mpmalwaretoast-data.md)
</dt> <dt>

[**MPNIS \_ \_ dati privati**](mpnis-private-data.md)
</dt> <dt>

[**MPNOTIFY**](mpnotify.md)
</dt> <dt>

[**\_dati MPRESERVED**](mpreserved-data.md)
</dt> <dt>

[**\_dati MPSAMPLE**](mpsample-data.md)
</dt> <dt>

[**\_dati MPSCAN**](mpscan-data.md)
</dt> <dt>

[**\_dati MPSIGUPDATE**](mpsigupdate-data.md)
</dt> <dt>

[**\_dati MPSTATUS**](mpstatus-data.md)
</dt> <dt>

[**\_dati MPTHREAT**](mpthreat-data.md)
</dt> </dl>

 

 





