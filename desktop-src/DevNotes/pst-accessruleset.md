---
description: Identifica il set di regole di accesso per i dati di archiviazione protetti.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: Struttura PST_ACCESSRULESET (PStore. h)
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
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331341"
---
# <a name="pst_accessruleset-structure"></a>\_Struttura ACCESSRULESET PST

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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

Numero di regole nella matrice **rgRules** .

</dd> <dt>

**rgRules**
</dt> <dd>

Puntatore a una matrice di strutture [**\_ ACCESSRULE PST**](pst-accessrule.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ACCESSRULE PST**](pst-accessrule.md)
</dt> <dt>

[**CreateSubtype**](ipstore-createsubtype.md)
</dt> </dl>

 

 
