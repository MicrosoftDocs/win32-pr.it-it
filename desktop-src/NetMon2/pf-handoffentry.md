---
description: La \_ struttura PF HANDOFFENTRY definisce un protocollo che Network Monitor aggiunge al set di continuità di un parser.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: Struttura PF_HANDOFFENTRY (Netmon. h)
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
ms.openlocfilehash: 5ad431e936265be96831778f9949ae67ef737beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314752"
---
# <a name="pf_handoffentry-structure"></a>\_Struttura PF HANDOFFENTRY

La struttura **PF \_ HANDOFFENTRY** definisce un protocollo che Network Monitor aggiunge al set di continuità di un parser.

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

Etichetta della sezione all'interno del file INI.

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

Base numerica del valore del protocollo specificato in **dwHandOffValue**. La funzione **ValueFormatBase** deve essere impostata su uno dei seguenti elementi:



| Valore                                                                                                                                                                                                                        | Significato                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <dt>**\_ \_ base formato valore \_ uniforme \_ sconosciuto**</dt> </dl> | Base sconosciuta<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <dt>**\_ \_ \_ decimale base \_ formato valore uniforme**</dt> </dl> | Base decimale<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <dt>**\_ \_ \_ Hex base formato valore \_ uniforme**</dt> </dl>             | Base esadecimale<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Una matrice di strutture **PF \_ HANDOFFENTRY** viene usata nella struttura [PF \_ HANDOFFSET](pf-handoffset.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> </dl>

 

 




