---
description: Contiene informazioni sulla clausola di accesso per l'archiviazione protetta.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: PST_ACCESSCLAUSE struttura (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: e5933b762ac19ac188e2d7253e86482caae968abd58ecb02087c32657d250216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386181"
---
# <a name="pst_accessclause-structure"></a>Struttura \_ PST ACCESSCLAUSE

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Contiene informazioni sulla clausola di accesso per l'archiviazione protetta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione della struttura.

</dd> <dt>

**ClauseType**
</dt> <dd>

Tipo di dati a cui punta il **membro pbClauseData.** Per altre informazioni, vedere [**Tipi PStore**](pstore-types.md).

</dd> <dt>

**cbClauseData**
</dt> <dd>

Dimensioni dei dati a cui punta il **membro pbClauseData.**

</dd> <dt>

**pbClauseData**
</dt> <dd>

Puntatore ai dati della clausola di accesso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**REGOLA \_ DI ACCESSO PST**](pst-accessrule.md)
</dt> </dl>

 

 
