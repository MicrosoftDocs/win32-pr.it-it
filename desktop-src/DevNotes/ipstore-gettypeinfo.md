---
description: Recupera le informazioni associate a un tipo.
ms.assetid: 27a283a5-8924-4a2f-8f58-e673a424e28a
title: Metodo IPStore::GetTypeInfo (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetTypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 67098a4f40fcfcc2ef0fedfcfd8d2ee48139e9c9687e53dd9ba0afb89fd1b983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079821"
---
# <a name="ipstoregettypeinfo-method"></a>Metodo IPStore::GetTypeInfo

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Recupera le informazioni associate a un tipo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO **ppInfo,
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

*ppInfo* \[ Pollici\]
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

 

 
