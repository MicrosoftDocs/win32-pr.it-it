---
title: MPDETECTION_ORIGIN enumerazione (MpClient.h)
description: Origine del rilevamento.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN di enumerazione Legacy Windows Environment Features
- PMPDETECTION_ORIGIN puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: 70b46ed86276ccb3fc3bd4d2b26388d778c102c1c1fa3bb7ced8f1ad64cd0203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092361"
---
# <a name="mpdetection_origin-enumeration"></a>Enumerazione MPDETECTION \_ ORIGIN

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

<span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**ORIGINE MPDETECTION \_ \_ SCONOSCIUTA**
</dt> <dd>

L'origine rilevata dalla minaccia è sconosciuta.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**COMPUTER LOCALE DI ORIGINE MPDETECTION \_ \_ \_**
</dt> <dd>

Minaccia rilevata nel computer locale.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ ORIGIN \_ NETWORKSHARE**
</dt> <dd>

Minaccia rilevata nella condivisione di rete.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION \_ ORIGIN \_ INTERNET**
</dt> <dd>

Minaccia rilevata su Internet.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**ORIGINE MPDETECTION \_ IN \_ USCITA**
</dt> <dd>

Minaccia rilevata in una connessione in uscita.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**ORIGINE MPDETECTION \_ \_ IN INGRESSO**
</dt> <dd>

Minaccia rilevata in una connessione in ingresso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





