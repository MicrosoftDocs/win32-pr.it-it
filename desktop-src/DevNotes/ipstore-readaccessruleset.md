---
description: Legge le regole di accesso per un tipo specificato.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'Metodo IPStore:: ReadAccessRuleSet (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f69c206bde67c2ddf9ed87ba0c50633ab9c15bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330429"
---
# <a name="ipstorereadaccessruleset-method"></a>Metodo IPStore:: ReadAccessRuleSet

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Questo metodo non è implementato.\]

Legge le regole di accesso per un tipo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ di in\]
</dt> <dd>

Riservato.

</dd> <dt>

*pType* \[ in\]
</dt> <dd>

Riservato.

</dd> <dt>

*pSubtype* \[ in\]
</dt> <dd>

Riservato.

</dd> <dt>

*pInfo* \[ in\]
</dt> <dd>

Riservato.

</dd> <dt>

*ppRules* \[ in\]
</dt> <dd>

Riservato.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Le chiamate a questo metodo avranno sempre esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
