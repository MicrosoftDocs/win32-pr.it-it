---
description: La struttura PF \_ PARSERDLLINFO definisce i parser che si trovano nella DLL del parser.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: PF_PARSERDLLINFO struttura (Netmon.h)
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
ms.openlocfilehash: caaafeb9883ad514366f91f3834354fbd5ac0850400e61594a5307c4533e0960
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962851"
---
# <a name="pf_parserdllinfo-structure"></a>Struttura PF \_ PARSERDLLINFO

La **struttura PF \_ PARSERDLLINFO** definisce i parser che si trovano nella DLL del parser.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**nParser**
</dt> <dd>

Numero di parser nella DLL del parser.

</dd> <dt>

**ParserInfo**
</dt> <dd>

Matrice di [strutture PF \_ PARSERINFO](pf-parserinfo.md) che descrivono ogni parser nella DLL del parser.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura PF \_ PARSERDLLINFO** viene restituita dalla funzione di esportazione [ParserAutoInstallInfo](parserautoinstallinfo.md) implementata nella DLL del parser. La **funzione ParserAutoInstallInfo** identifica il numero di parser nella DLL e usa una matrice di [strutture PF \_ PARSERINFO](pf-parserinfo.md) per descrivere ogni parser.

La struttura PF \_ PARSERDLLINFO deve essere allocata usando **HeapAlloc**.



| Per informazioni su                                               | Vedere                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor.        | [Parser](parsers.md)                                                      |
| Punti di ingresso inclusi nella DLL del parser.               | [Architettura della DLL del parser](parser-dll-architecture.md)                      |
| Come implementare **ParserAutoInstallInfo**  include un esempio. | [Implementazione di ParserAutoIstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> </dl>

 

 




