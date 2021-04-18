---
title: Enumerazione MPDETECTION_ORIGIN (MpClient. h)
description: Origine del rilevamento.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPDETECTION_ORIGIN
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPDETECTION_ORIGIN
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301410"
---
# <a name="mpdetection_origin-enumeration"></a>\_Enumerazione MPDETECTION Origin

Origine del rilevamento.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**\_origine MPDETECTION \_ sconosciuta**
</dt> <dd>

Origine rilevata minaccia sconosciuta.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**\_ \_ computer locale di origine MPDETECTION \_**
</dt> <dd>

Minaccia rilevata nel computer locale.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ Origin \_ NETWORKSHARE**
</dt> <dd>

Minaccia rilevata nella condivisione di rete.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**\_Internet di origine MPDETECTION \_**
</dt> <dd>

Minaccia rilevata in Internet.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**origine MPDETECTION in \_ \_ uscita**
</dt> <dd>

Minaccia rilevata in una connessione in uscita.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**origine MPDETECTION in \_ \_ ingresso**
</dt> <dd>

Minaccia rilevata in una connessione in ingresso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





