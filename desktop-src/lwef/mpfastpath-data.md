---
title: Struttura MPFASTPATH_DATA (MpClient. h)
description: Notifica di aggiornamento FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- Struttura MPFASTPATH_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPFASTPATH_DATA
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301408"
---
# <a name="mpfastpath_data-structure"></a>\_Struttura dei dati MPFASTPATH

Notifica di aggiornamento FastPath.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**SignatureType**
</dt> <dd>

Tipo: **[ **\_ \_ tipo di firma MP**](mp-signature-type.md)**

</dd> <dd>

Tipo di firma.

</dd> <dt>

**FastPathSignatureType**
</dt> <dd>

Tipo: **[ **\_ FastPath MP \_**](mp-fastpath-type.md)**

</dd> <dd>

Tipo di firma FastPath.

</dd> <dt>

**FastPathSignatureVersion**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Versione della firma FastPath (facoltativa).

</dd> <dt>

**CompilationTimestamp**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Timestamp compilazione (UTC).

</dd> <dt>

**PersistenceType**
</dt> <dd>

Tipo: **[ **\_ limite di \_ \_ persistenza MP**](mp-persistence-limit-type.md)**

</dd> <dd>

Tipo di persistenza (facoltativo).

</dd> <dt>

**PersistenceValue**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Valore di persistenza (facoltativo).

</dd> <dt>

**PersistencePath**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Percorso di persistenza (facoltativo).

</dd> <dt>

**Motivo**
</dt> <dd>

Tipo: **[ **\_ \_ motivo della rimozione MP**](mp-removal-reason.md)**

</dd> <dd>

Motivo della rimozione della firma.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tipo di FastPath MP \_**](mp-fastpath-type.md)
</dt> <dt>

[**\_tipo limite di persistenza MP \_ \_**](mp-persistence-limit-type.md)
</dt> <dt>

[**\_tipo di firma MP \_**](mp-signature-type.md)
</dt> </dl>

 

 





