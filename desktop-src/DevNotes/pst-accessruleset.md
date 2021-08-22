---
description: Identifica il set di regole di accesso per i dati di archiviazione protetti.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: PST_ACCESSRULESET struttura (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 9695af01c6f0ffb33fe20a112659444011ad9c18812b8d2fd885641635c6b4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666977"
---
# <a name="pst_accessruleset-structure"></a>Struttura \_ PST ACCESSRULESET

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Identifica il set di regole di accesso per i dati di archiviazione protetti.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione della struttura.

</dd> <dt>

**cRules**
</dt> <dd>

Numero di regole nella matrice **rgRules.**

</dd> <dt>

**rgRules**
</dt> <dd>

Puntatore a una matrice di [**strutture \_ ACCESSRULE PST.**](pst-accessrule.md)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**REGOLA \_ DI ACCESSO PST**](pst-accessrule.md)
</dt> <dt>

[**CreateSubtype**](ipstore-createsubtype.md)
</dt> </dl>

 

 
