---
title: MPFASTPATH_DATA (MpClient.h)
description: Notifica di aggiornamento di FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA funzionalità dell'ambiente Windows legacy
- PMPFASTPATH_DATA puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: e138e9c45657cfc4ebeba1d1dbeed38070b6e07d09c512ec96835a04702d0c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556151"
---
# <a name="mpfastpath_data-structure"></a>Struttura MPFASTPATH \_ DATA

Notifica di aggiornamento di FastPath.

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

**Tipo di firma**
</dt> <dd>

Tipo: **[ **MP \_ SIGNATURE \_ TYPE**](mp-signature-type.md)**

</dd> <dd>

Tipo di firma.

</dd> <dt>

**FastPathSignatureType**
</dt> <dd>

Tipo: **[ **MP \_ FASTPATH \_ TYPE**](mp-fastpath-type.md)**

</dd> <dd>

Tipo di firma FastPath.

</dd> <dt>

**FastPathSignatureVersion**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Versione della firma FastPath (facoltativa).

</dd> <dt>

**CompilationTimestamp**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Timestamp di compilazione (UTC).

</dd> <dt>

**Tipo di persistenza**
</dt> <dd>

Tipo: **[ **MP PERSISTENCE \_ LIMIT \_ \_ TYPE**](mp-persistence-limit-type.md)**

</dd> <dd>

Tipo di persistenza (facoltativo).

</dd> <dt>

**PersistenceValue**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Valore di persistenza (facoltativo).

</dd> <dt>

**PersistencePath**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Percorso di persistenza (facoltativo).

</dd> <dt>

**Motivo**
</dt> <dd>

Tipo: **[ **MP \_ REMOVAL \_ REASON**](mp-removal-reason.md)**

</dd> <dd>

Motivo della rimozione della firma.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TIPO \_ FASTPATH \_ MP**](mp-fastpath-type.md)
</dt> <dt>

[**TIPO DI \_ LIMITE DI \_ PERSISTENZA \_ MP**](mp-persistence-limit-type.md)
</dt> <dt>

[**TIPO \_ DI FIRMA \_ MP**](mp-signature-type.md)
</dt> </dl>

 

 





