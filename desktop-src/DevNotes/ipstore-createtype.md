---
description: Crea il tipo specificato con il nome specificato.
ms.assetid: eb85477c-d750-46d2-8b32-450f672e7601
title: Metodo IPStore::CreateType (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7064cd07c0af99cbb325457217c2679757837be3ac1f5d80977cd2bb222f6b75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667519"
---
# <a name="ipstorecreatetype-method"></a>Metodo IPStore::CreateType

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Crea il tipo specificato con il nome specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateType(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO pInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Specifica se il tipo è locale al computer o associato solo all'utente che crea.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ KEY \_ CURRENT \_ USER**</dt> <dt>0x00000000</dt> </dl>    | L'archiviazione viene gestita nella sezione utente corrente del Registro di sistema.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CHIAVE \_ DEL \_ COMPUTER**</dt> LOCALE <dt>0x00000001</dt> </dl> | L'archiviazione viene gestita nella sezione del computer locale del Registro di sistema.<br/> |



 

</dd> <dt>

*pType* \[ Pollici\]
</dt> <dd>

Puntatore a un **GUID che** identifica il tipo di dati dell'archiviazione.

</dd> <dt>

*pInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ TYPEINFO PST**](pst-typeinfo.md) che contiene il nome del tipo di dati.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Riservato: deve essere impostato su zero.

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

[**Archivio IP**](ipstore.md)
</dt> <dt>

[**PST \_ TYPEINFO**](pst-typeinfo.md)
</dt> </dl>

 

 
