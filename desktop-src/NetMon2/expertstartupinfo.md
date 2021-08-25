---
description: Contiene dati che descrivono un esperto all'avvio.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Struttura EXPERTSTARTUPINFO (Netmon.h)
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
ms.openlocfilehash: f49fcf3c87795dbd7c9e65745e1b5560331c96c471d8ff7b2c8a24560b143cb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911051"
---
# <a name="expertstartupinfo-structure"></a>Struttura EXPERTSTARTUPINFO

La **struttura EXPERTSTARTUPINFO** contiene dati che descrivono un esperto all'avvio.

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

Numero di fotogramma.

</dd> <dt>

**hProtocol**
</dt> <dd>

Handle per il protocollo.

</dd> <dt>

**lpPropertyInst**
</dt> <dd>

Puntatore a [**una struttura PROPERTYINST.**](propertyinst.md)

</dd> <dt>

**sBitfield**
</dt> <dd> <dl> <dt>

**Numero di bit**
</dt> <dd>

Utilizzato solo se il **membro DataQualifier** della [**struttura PROPERTYINST**](propertyinst.md) è impostato su PROP \_ QUAL \_ FLAGS.

</dd> <dt>

**Bon**
</dt> <dd>

Utilizzato solo se il **membro DataQualifier** della [**struttura PROPERTYINST**](propertyinst.md) è impostato su PROP \_ QUAL \_ FLAGS.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




