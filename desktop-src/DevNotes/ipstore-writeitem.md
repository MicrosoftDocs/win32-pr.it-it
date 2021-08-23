---
description: Scrive un elemento di dati nell'archiviazione protetta.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: Metodo IPStore::WriteItem (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d8af896d2aca8ae218ba06f94cb0e2ef5f86fc4122acf3463356f5fea3dafd1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955890"
---
# <a name="ipstorewriteitem-method"></a>Metodo IPStore::WriteItem

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Scrive un elemento di dati nell'archiviazione protetta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Area di archiviazione del provider.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHIAVE \_ UTENTE \_ CORRENTE**</dt> <dt>0x00000000</dt> </dl>    | L'archiviazione viene mantenuta nella sezione utente corrente del Registro di sistema.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CHIAVE \_ COMPUTER \_ LOCALE**</dt> <dt>0x00000001</dt> </dl> | L'archiviazione viene mantenuta nella sezione del computer locale del Registro di sistema.<br/> |



 

</dd> <dt>

*pItemType* \[ Pollici\]
</dt> <dd>

Puntatore a un **GUID che** identifica il tipo di dati dell'elemento di dati da scrivere.

</dd> <dt>

*pItemSubtype* \[ Pollici\]
</dt> <dd>

Puntatore a un **GUID che** identifica il sottotipo di dati dell'elemento di dati da scrivere.

</dd> <dt>

*szItemName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa contenente il nome assegnato all'elemento di dati archiviato.

</dd> <dt>

*cbData* \[ Cambio\]
</dt> <dd>

Puntatore a un **valore DWORD** che indica le dimensioni del buffer che contiene l'elemento di dati archiviato.

</dd> <dt>

*ppbData* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che contiene l'elemento di dati da scrivere.

</dd> <dt>

*pProomptInfo* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura \_ PST PROMPTINFO.**](pst-promptinfo.md)

</dd> <dt>

*dwDefaultConfirmationStyle* \[ Pollici\]
</dt> <dd>

Stile di conferma predefinito.



| Valore                                                                                                                                                                                                                             | Significato                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <dt>**PST \_ IMPOSTAZIONE \_ PREDEFINITA DI CF**</dt> <dt>0x00000000</dt> </dl> | Consente all'utente di scegliere lo stile di conferma. <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <dt>**PST \_ Cf \_ NONE**</dt> <dt>0x00000001</dt> </dl>          | Forza la creazione di elementi invisibile all'utente. <br/>                      |



 

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Interfaccia utente e comportamenti di sicurezza per l'operazione di scrittura.



| Valore                                                                                                                                                                                                                                                              | Significato                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <dt>**PST \_ NO \_ OVERWRITE**</dt> <dt>0x00000002</dt> </dl>                            | Specifica che l'elemento deve essere creato nell'archiviazione protetta. La sovrascrittura di un elemento esistente non è consentita.<br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ OGGETTO \_ ITEMDATA**</dt> <dt>SENZA RESTRIZIONI 0x00000004</dt> </dl> | Specifica che il flusso di dati non è sicuro. Per impostazione predefinita, le chiamate all'elemento sono sicure.<br/>                         |



 

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
</dt> <dt>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)
</dt> </dl>

 

 
