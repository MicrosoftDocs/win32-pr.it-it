---
description: Scrive le regole di accesso per il tipo specificato.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: Metodo IPStore::WriteAccessRuleset (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: a21fac6df5ab4d87e55d71e45f5698251ca4f82b6c93de1072c2ae5bcd7236aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955900"
---
# <a name="ipstorewriteaccessruleset-method"></a>Metodo IPStore::WriteAccessRuleset

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Questo metodo non è implementato.\]

Scrive le regole di accesso per il tipo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> <dt>

*pType* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> <dt>

*pSubtype* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> <dt>

*pInfo* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> <dt>

*pRules* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Le chiamate a questo metodo avranno sempre esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Archivio IP**](ipstore.md)
</dt> </dl>

 

 
