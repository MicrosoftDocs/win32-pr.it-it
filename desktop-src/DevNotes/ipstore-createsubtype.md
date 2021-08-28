---
description: Crea il sottotipo specificato all'interno del tipo specificato.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: Metodo IPStore::CreateSubtype (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: da82d1edac78fab26f47be5bc333558355d04c3627342ece904a4005e9ebfa2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749991"
---
# <a name="ipstorecreatesubtype-method"></a>Metodo IPStore::CreateSubtype

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Crea il sottotipo specificato all'interno del tipo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSubtype(
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

Specifica l'area di archiviazione del provider.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ KEY \_ CURRENT \_ USER**</dt> <dt>0x00000000</dt> </dl>    | L'archiviazione viene gestita nella sezione utente corrente del Registro di sistema.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CHIAVE \_ COMPUTER \_ LOCALE**</dt> <dt>0x00000001</dt> </dl> | L'archiviazione viene gestita nella sezione del computer locale del Registro di sistema.<br/> |



 

</dd> <dt>

*pType* \[ Pollici\]
</dt> <dd>

Puntatore a un **GUID che** identifica il tipo di dati dell'archiviazione.

</dd> <dt>

*pSubtype* \[ Pollici\]
</dt> <dd>

Puntatore a un **GUID che** identifica il sottotipo di dati dell'archiviazione.

</dd> <dt>

*pInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ TYPEINFO PST.**](pst-typeinfo.md)

</dd> <dt>

*pRules* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ PST ACCESSRULESET.**](pst-accessruleset.md)

**Windows XP:** Questo parametro viene ignorato.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Riservato; deve essere impostato su zero.

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

[**SET \_ DI REGOLE DI ACCESSO PST**](pst-accessruleset.md)
</dt> <dt>

[**PST \_ TYPEINFO**](pst-typeinfo.md)
</dt> </dl>

 

 
