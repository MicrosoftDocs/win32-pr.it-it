---
description: Contiene informazioni sulla clausola Access per l'archiviazione protetta.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: Struttura PST_ACCESSCLAUSE (PStore. h)
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
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325199"
---
# <a name="pst_accessclause-structure"></a>\_Struttura ACCESSCLAUSE PST

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Contiene informazioni sulla clausola Access per l'archiviazione protetta.

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

Tipo di dati a cui fa riferimento il membro **pbClauseData** . Per altre informazioni, vedere [**tipi di PStore**](pstore-types.md).

</dd> <dt>

**cbClauseData**
</dt> <dd>

Dimensione dei dati a cui fa riferimento il membro **pbClauseData** .

</dd> <dt>

**pbClauseData**
</dt> <dd>

Puntatore ai dati della clausola di accesso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ACCESSRULE PST**](pst-accessrule.md)
</dt> </dl>

 

 
