---
description: Restituisce un'interfaccia per l'enumerazione dei sottotipi dei tipi attualmente registrati nel database protetto.
ms.assetid: 07cc43ce-2191-4b20-b23d-d96d15aa8dea
title: Metodo IPStore::EnumSubtypes (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumSubtypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: cc124375b6f7282d6ae8f05269b3b3408a81089193da8028c7720c274987e4f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827134"
---
# <a name="ipstoreenumsubtypes-method"></a>Metodo IPStore::EnumSubtypes

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Restituisce un'interfaccia per l'enumerazione dei sottotipi dei tipi attualmente registrati nel database protetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumSubtypes(
  [in]       PST_KEY          Key,
  [in] const GUID             *pType,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Specifica se il tipo è locale per il computer o associato solo all'utente che crea.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHIAVE \_ UTENTE \_ CORRENTE**</dt> <dt>0x00000000</dt> </dl>    | L'archiviazione viene mantenuta nella sezione utente corrente del Registro di sistema.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CHIAVE \_ DEL \_ COMPUTER**</dt> LOCALE <dt>0x00000001</dt> </dl> | L'archiviazione viene mantenuta nella sezione del computer locale del Registro di sistema.<br/> |



 

</dd> <dt>

*pType* \[ Pollici\]
</dt> <dd>

Puntatore a un GUID che identifica il tipo di dati della risorsa di archiviazione.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Riservato: deve essere impostato su zero.

</dd> <dt>

*ppenum* \[ Pollici\]
</dt> <dd>

Puntatore a [**un'interfaccia IEnumPStoreTypes**](ienumpstoretypes.md) usata per enumerare i sottotipi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un **valore HRESULT.** Il valore **PST \_ E \_ OK** indica che la funzione ha avuto esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
