---
title: Enumerazione MPSOURCE (MpClient. h)
description: Categoria di origine possibile.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPSOURCE
- Funzionalità dell'ambiente Windows legacy del puntatore di enumerazione PMPSOURCE
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9255029512499a0e2948a44701ef4482aff4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964486"
---
# <a name="mpsource-enumeration"></a>Enumerazione MPSOURCE

Categoria di origine possibile.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE \_ sconosciuto**
</dt> <dd>

Origine sconosciuta.

</dd> <dt>

<span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**\_utente MPSOURCE**
</dt> <dd>

Avviata dall'utente.

</dd> <dt>

<span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**\_sistema MPSOURCE**
</dt> <dd>

avviato dal sistema.

</dd> <dt>

<span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE in \_ tempo reale**
</dt> <dd>

Componente in tempo reale avviato.

</dd> <dt>

<span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**\_IOAV MPSOURCE**
</dt> <dd>

Vengono avviati i download di IE e gli allegati di Outlook Express.

</dd> <dt>

<span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**\_NIS MPSOURCE**
</dt> <dd>

Sistema di ispezione di rete.

</dd> <dt>

<span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**\_bho MPSOURCE**
</dt> <dd>

BHO-script Web (deprecato).

</dd> <dt>

<span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**\_IEPROTECT MPSOURCE**
</dt> <dd>

IE-IExtensionValidation.

</dd> <dt>

<span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**\_Elam MPSOURCE**
</dt> <dd>

ELAM

</dd> <dt>

<span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**\_ \_ attestazione locale MPSOURCE**
</dt> <dd>

Attestazione locale.

</dd> <dt>

<span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**\_ \_ attestazione remota MPSOURCE**
</dt> <dd>

Attestazione remota.

</dd> <dt>

<span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**\_AMSI MPSOURCE**
</dt> <dd>

AMSI

</dd> <dt>

<span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**\_MaxValue origine \_ MP**
</dt> <dd>

Valore massimo possibile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





