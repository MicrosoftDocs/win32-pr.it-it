---
description: Descrive una regola per l'accesso agli elementi archiviati in un archivio protetto.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: Struttura PST_ACCESSRULE (PStore. h)
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
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331343"
---
# <a name="pst_accessrule-structure"></a>\_Struttura ACCESSRULE PST

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Descrive una regola per l'accesso agli elementi archiviati in un archivio protetto.

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

Modalità di accesso a cui si riferisce un set specificato di clausole di accesso.



| Valore                                                                                                                                                                                                         | Significato                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**Pst \_ Leggi**</dt> <dt>0x0001</dt> </dl>    | Modalità di accesso in lettura.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**Pst \_ Scrivi**</dt> <dt>0x0002</dt> </dl> | Modalità di accesso in scrittura.<br/> |



 

</dd> <dt>

**cClauses**
</dt> <dd>

Numero di strutture nella matrice **rgClauses** .

</dd> <dt>

**rgClauses**
</dt> <dd>

Puntatore a una matrice di strutture [**\_ ACCESSCLAUSE PST**](pst-accessclause.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ACCESSCLAUSE PST**](pst-accessclause.md)
</dt> <dt>

[**\_ACCESSRULESET PST**](pst-accessruleset.md)
</dt> </dl>

 

 
