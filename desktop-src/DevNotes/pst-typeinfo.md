---
description: Descrive un tipo o un sottotipo.
ms.assetid: 4b6b77d9-54ea-4101-9c8b-e525f9aa3816
title: Struttura PST_TYPEINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_TYPEINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: fc78d0570ff2e5cf66a9048d64143149564a51c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331714"
---
# <a name="pst_typeinfo-structure"></a>\_Struttura TYPEINFO PST

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Descrive un tipo o un sottotipo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD  cbSize;
  LPWSTR szDisplayName;
} PST_TYPEINFO, *PPST_TYPEINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione della struttura.

</dd> <dt>

**szDisplayName**
</dt> <dd>

Puntatore a una stringa di caratteri wide che rappresenta il nome visualizzato per il tipo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateSubtype**](ipstore-createsubtype.md)
</dt> <dt>

[**CreateType**](ipstore-createtype.md)
</dt> <dt>

[**GetSubtypeInfo**](ipstore-getsubtypeinfo.md)
</dt> <dt>

[**GetTypeInfo**](ipstore-gettypeinfo.md)
</dt> </dl>

 

 
