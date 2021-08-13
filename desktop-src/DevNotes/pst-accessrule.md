---
description: Descrive una regola per l'accesso agli elementi archiviati nell'archiviazione protetta.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: PST_ACCESSRULE struttura (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 26b4df38c5e5599c13cc52a75c58ea019d786eaa971c8ac3a67a7a8c15651075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667057"
---
# <a name="pst_accessrule-structure"></a>Struttura \_ PST ACCESSRULE

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Descrive una regola per l'accesso agli elementi archiviati nell'archiviazione protetta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione della struttura.

</dd> <dt>

**AccessModeFlags**
</dt> <dd>

Modalità di accesso a cui si riferiscono un set specificato di clausole di accesso.



| Valore                                                                                                                                                                                                         | Significato                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**PST \_ LEGGERE**</dt> <dt>0x0001</dt> </dl>    | Modalità di accesso in lettura.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**PST \_ WRITE**</dt> <dt>0x0002</dt> </dl> | Modalità di accesso in scrittura.<br/> |



 

</dd> <dt>

**cClauses**
</dt> <dd>

Numero di strutture nella matrice **rgClauses.**

</dd> <dt>

**rgClauses**
</dt> <dd>

Puntatore a una matrice di [**strutture \_ PST ACCESSCLAUSE.**](pst-accessclause.md)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACCESSO \_ PSTCLAUSE**](pst-accessclause.md)
</dt> <dt>

[**SET \_ DI REGOLE DI ACCESSO PST**](pst-accessruleset.md)
</dt> </dl>

 

 
