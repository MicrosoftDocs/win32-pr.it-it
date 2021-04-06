---
title: Struttura MPTHREAT_INFOEX_BEHAVIOR (MpClient. h)
description: Contiene informazioni specifiche relative alla modifica del comportamento.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- Struttura MPTHREAT_INFOEX_BEHAVIOR le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_INFOEX_BEHAVIOR
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743175"
---
# <a name="mpthreat_infoex_behavior-structure"></a>\_Struttura del comportamento INFOEX di MPTHREAT \_

Contiene informazioni specifiche relative alla modifica del comportamento.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a>Members

<dl> <dt>

**SignatureID**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

ID firma della modifica del comportamento fornito dal motore al momento del rilevamento.

</dd> <dt>

**EngineVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versione del modulo del motore.

</dd> <dt>

**ASDeltaSignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versione della firma antispyware.

</dd> <dt>

**AVDeltaSignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versione della firma antivirus

</dd> <dt>

**HashType**
</dt> <dd>

Tipo: **[ **\_ \_ tipo di hash MP**](mp-hash-type.md)**

</dd> <dd>

Tipo di hash utilizzato. Vedere [**\_ \_ tipo di hash MP**](mp-hash-type.md).

</dd> <dt>

**FidelityValue**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valore fedeltà.

</dd> <dt>

**HashValue**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Hash del file.

</dd> <dt>

**TargetFileName**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Il percorso e il nome del file di destinazione.

</dd> <dt>

**TargetFileHash**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Hash del file di destinazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tipo di hash MP \_**](mp-hash-type.md)
</dt> </dl>

 

 





