---
title: MPCALLBACK_DATA (MpClient.h)
description: Dati passati alla funzione di callback.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA funzionalità dell'ambiente Windows legacy
- PMPCALLBACK_DATA puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: 1d1eb129101c341485a1e6b5763a0325cbf586a6e51e5e2875b4465696c39df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883653"
---
# <a name="mpcallback_data-structure"></a>Struttura MPCALLBACK \_ DATA

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

Modificare la notifica in report.

</dd> <dt>

**Hresult**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Codice di errore, in caso di errore interno.

</dd> <dt>

**Timestamp**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Timestamp corrente.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **MPCALLBACK \_ TYPE**](mpcallback-type.md)**

</dd> <dd>

Tipo di dati speciale di callback.

</dd> <dt>

**Dati**
</dt> <dd>

Dati speciali di callback. Il puntatore alla struttura appropriata dipende dal valore di **Tipo**.

<dl> <dt>

**pStatusData**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATA**

</dd> <dd>

Quando **digitare**  ==  **MPCALLBACK \_ STATUS**. Vedere [**MPSTATUS \_ DATA**](mpstatus-data.md).

</dd> <dt>

**pScanData**
</dt> <dd>

Tipo: **PMPSCAN \_ DATA**

</dd> <dd>

Quando **si digita**  ==  **MPCALLBACK \_ SCAN**. Vedere [**MPSCAN \_ DATA**](mpscan-data.md).

</dd> <dt>

**pCleanData**
</dt> <dd>

Tipo: **PMPCLEAN \_ DATA**

</dd> <dd>

Quando **si digita**  ==  **MPCALLBACK \_ CLEAN**. Vedere [**MPCLEAN \_ DATA**](mpclean-data.md).

</dd> <dt>

**pPrecheckData**
</dt> <dd>

Tipo: **PMPCLEAN \_ PRECHECK \_ DATA**

</dd> <dd>

Quando **si digita**  ==  **MPCALLBACK \_ PRECHECK**. Vedere [**MPCLEAN \_ PRECHECK \_ DATA**](mpclean-precheck-data.md).

</dd> <dt>

**pThreatData**
</dt> <dd>

Tipo: **PMPTHREAT \_ DATA**

</dd> <dd>

Quando **digitare**  ==  **MPCALLBACK \_ THREAT**. Vedere [**MPTHREAT \_ DATA**](mpthreat-data.md).

</dd> <dt>

**pSigUpdateData**
</dt> <dd>

Tipo: **PMPSIGUPDATE \_ DATA**

</dd> <dd>

Quando **si digita**  ==  **MPCALLBACK \_ SIGUPDATE**. Vedere [**MPSIGUPDATE \_ DATA**](mpsigupdate-data.md).

</dd> <dt>

**pSampleData**
</dt> <dd>

Tipo: **PMPSAMPLE \_ DATA**

</dd> <dd>

Quando **digitare**  ==  **MPCALLBACK \_ SAMPLE**. Vedere [**MPSAMPLE \_ DATA**](mpsample-data.md).

</dd> <dt>

**pReservedData**
</dt> <dd>

Tipo: **PMPRESERVED \_ DATA**

</dd> <dd>

Quando **è di tipo**  ==  **MPCALLBACK \_ RESERVED**. Vedere [**MPRESERVED \_ DATA**](mpreserved-data.md).

</dd> <dt>

**pConfigurationData**
</dt> <dd>

Tipo: **PMPCONFIGURATION \_ DATA**

</dd> <dd>

Quando **digitare**  ==  **MPCALLBACK \_ CONFIGURATION \_ NOTIFICATION**. Vedere [**MPCONFIGURATION \_ DATA**](mpconfiguration-data.md).

</dd> <dt>

**pFastPathData**
</dt> <dd>

Tipo: **PMPFASTPATH \_ DATA**

</dd> <dd>

Quando **si digita**  ==  **MPCALLBACK \_ FASTPATH**. Vedere [**MPFASTPATH \_ DATA**](mpfastpath-data.md).

</dd> <dt>

**pExpirationData**
</dt> <dd>

Tipo: **PMPEXPIRATION \_ DATA**

</dd> <dd>

Quando **digitare**  ==  **MPCALLBACK \_ PRODUCT \_ EXPIRATION**. Vedere [**MPEXPIRATION \_ DATA**](mpexpiration-data.md).

</dd> <dt>

**pNISPrivateData**
</dt> <dd>

Tipo: **PMPNIS \_ PRIVATE \_ DATA**

</dd> <dd>

Quando **si digita**  ==  **MPCALLBACK \_ NIS \_ PRIVATE**. Vedere [**MPNIS \_ PRIVATE \_ DATA (DATI PRIVATI MPNIS).**](mpnis-private-data.md)

</dd> <dt>

**pHealthData**
</dt> <dd>

Tipo: **PMPHEALTH \_ DATA**

</dd> <dd>

Quando **digitare**  ==  **MPCALLBACK \_ HEALTH**. Vedere [**MPHEALTH \_ DATA ( DATI MPHEALTH).**](mphealth-data.md)

</dd> <dt>

**pEndOfLifeData**
</dt> <dd>

Tipo: **PMPENDOFLIFE \_ DATA**

</dd> <dd>

Quando **si digita**  ==  **MPCALLBACK \_ ENDOFLIFE**. Vedere [**MPENDOFLIFE \_ DATA**](mpendoflife-data.md).

</dd> <dt>

**pMalwareToastData**
</dt> <dd>

Tipo: **PMPMALWARETOAST \_ DATA**

</dd> <dd>

Quando **digitare**  ==  **MPCALLBACK \_ MALWARETOAST**. Vedere [**MPMALWARETOAST \_ DATA**](mpmalwaretoast-data.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TIPO \_ MPCALLBACK**](mpcallback-type.md)
</dt> <dt>

[**DATI \_ MPCLEAN**](mpclean-data.md)
</dt> <dt>

[**DATI DI \_ CONTROLLO PRELIMINARE MPCLEAN \_**](mpclean-precheck-data.md)
</dt> <dt>

[**DATI \_ MPCONFIGURATION**](mpconfiguration-data.md)
</dt> <dt>

[**MPENDOFLIFE \_ DATA**](mpendoflife-data.md)
</dt> <dt>

[**DATI \_ MPEXPIRATION**](mpexpiration-data.md)
</dt> <dt>

[**DATI \_ MPFASTPATH**](mpfastpath-data.md)
</dt> <dt>

[**DATI \_ MPHEALTH**](mphealth-data.md)
</dt> <dt>

[**DATI MPMALWARETOAST \_**](mpmalwaretoast-data.md)
</dt> <dt>

[**DATI PRIVATI \_ MPNIS \_**](mpnis-private-data.md)
</dt> <dt>

[**MPNOTIFY**](mpnotify.md)
</dt> <dt>

[**MPRESERVED \_ DATA**](mpreserved-data.md)
</dt> <dt>

[**DATI \_ MPSAMPLE**](mpsample-data.md)
</dt> <dt>

[**MPSCAN \_ DATA**](mpscan-data.md)
</dt> <dt>

[**MPSIGUPDATE \_ DATA**](mpsigupdate-data.md)
</dt> <dt>

[**DATI \_ MPSTATUS**](mpstatus-data.md)
</dt> <dt>

[**MPTHREAT \_ DATA**](mpthreat-data.md)
</dt> </dl>

 

 





