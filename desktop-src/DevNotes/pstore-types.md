---
description: Tipi di dati per i Archiviazione protetti.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Tipi PStore (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6def89ea4beb5d27a98cb8e6f44fc12271de7d1642b236f31f4979ed26b54a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538451"
---
# <a name="pstore-types"></a>Tipi PStore

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Tipi di dati per i Archiviazione protetti.


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

**PST \_ ACCESSMODE**
</dt> <dd>

Definisce la modalità di lettura o scrittura della regola di accesso.

</dd> <dt>

**PST \_ ACCESSCLAUSETYPE**
</dt> <dd>

Definisce il tipo di clausola della regola di accesso.

</dd> <dt>

**PST \_ KEY**
</dt> <dd>

Definisce la chiave per l'elemento archiviato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl> |



 

 
