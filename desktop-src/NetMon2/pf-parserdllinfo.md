---
description: La \_ struttura PF PARSERDLLINFO definisce i parser presenti nella dll del parser.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: Struttura PF_PARSERDLLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967895"
---
# <a name="pf_parserdllinfo-structure"></a>\_Struttura PF PARSERDLLINFO

La struttura **PF \_ PARSERDLLINFO** definisce i parser presenti nella dll del parser.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**nParsers**
</dt> <dd>

Numero di parser nella DLL del parser.

</dd> <dt>

**ParserInfo**
</dt> <dd>

Matrice di strutture [PF \_ PARSERINFO](pf-parserinfo.md) che descrivono ogni parser nella dll del parser.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **PF \_ PARSERDLLINFO** viene restituita dalla funzione di esportazione [PARSERAUTOINSTALLINFO](parserautoinstallinfo.md) implementata nella dll del parser. La funzione **ParserAutoInstallInfo** identifica il numero di parser nella dll e usa una matrice di strutture [PF \_ PARSERINFO](pf-parserinfo.md) per descrivere ogni parser.

\_È necessario allocare la struttura PF PARSERDLLINFO usando **HeapAlloc**.



| Per informazioni su                                               | Vedere                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor.        | [Parser](parsers.md)                                                      |
| I punti di ingresso inclusi nella DLL del parser.               | [Architettura DLL parser](parser-dll-architecture.md)                      |
| L'implementazione di **ParserAutoInstallInfo**  include un esempio. | [Implementazione di ParserAutoIstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> </dl>

 

 




