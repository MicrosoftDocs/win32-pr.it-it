---
description: Contiene dati che descrivono un esperto all'avvio.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Struttura EXPERTSTARTUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966479"
---
# <a name="expertstartupinfo-structure"></a>Struttura EXPERTSTARTUPINFO

La struttura **EXPERTSTARTUPINFO** contiene dati che descrivono un esperto all'avvio.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Flag**
</dt> <dd>

Flag che descrivono l'esperto.

</dd> <dt>

**hCapture**
</dt> <dd>

Handle per un'acquisizione.

</dd> <dt>

**szCaptureFile**
</dt> <dd>

Nome del file di acquisizione.

</dd> <dt>

**dwFrameNumber**
</dt> <dd>

Numero di frame.

</dd> <dt>

**hProtocol**
</dt> <dd>

Handle per il protocollo.

</dd> <dt>

**lpPropertyInst**
</dt> <dd>

Puntatore a una struttura [**PROPERTYINST**](propertyinst.md) .

</dd> <dt>

**sBitfield**
</dt> <dd> <dl> <dt>

**BitNumber**
</dt> <dd>

Utilizzato solo se il membro **dataqualifier** della struttura [**PROPERTYINST**](propertyinst.md) è impostato su propa \_ \_ Flags.

</dd> <dt>

**bOn**
</dt> <dd>

Utilizzato solo se il membro **dataqualifier** della struttura [**PROPERTYINST**](propertyinst.md) è impostato su propa \_ \_ Flags.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




