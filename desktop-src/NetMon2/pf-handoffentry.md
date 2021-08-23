---
description: La struttura PF HANDOFFENTRY definisce un protocollo \_ che Network Monitor aggiunge al set di consegna di un parser.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: PF_HANDOFFENTRY struttura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: faf98490424754d6ae2223ca063e0e3a4eec69c113b1a220e9657b7db5edbb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778671"
---
# <a name="pf_handoffentry-structure"></a>Struttura PF \_ HANDOFFENTRY

La **struttura PF \_ HANDOFFENTRY** definisce un protocollo che Network Monitor aggiunge al set di handoff di un parser.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**szIniFile**
</dt> <dd>

Nome del file INI associato al protocollo.

</dd> <dt>

**szIniSection**
</dt> <dd>

Etichetta di sezione all'interno del file INI.

</dd> <dt>

**szProtocol**
</dt> <dd>

Nome del protocollo.

</dd> <dt>

**dwHandOffValue**
</dt> <dd>

Valore associato al protocollo.

</dd> <dt>

**ValueFormatBase**
</dt> <dd>

Base numerica del valore del protocollo specificato in **dwHandOffValue**. La **funzione ValueFormatBase** deve essere impostata su uno dei valori seguenti:



| Valore                                                                                                                                                                                                                        | Significato                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <dt>**HANDOFF \_ VALUE \_ FORMAT \_ BASE \_ UNKNOWN**</dt> </dl> | Base sconosciuta<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <dt>**HANDOFF \_ VALUE \_ FORMAT \_ BASE \_ DECIMAL**</dt> </dl> | Base decimale<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <dt>**HANDOFF \_ VALUE \_ FORMAT \_ BASE \_ HEX**</dt> </dl>             | Base esadecimale<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Nella struttura [PF \_ HANDOFFSET](pf-handoffset.md) viene usata una matrice delle strutture **PF \_ HANDOFFENTRY.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> </dl>

 

 




