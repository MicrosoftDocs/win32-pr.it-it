---
description: Scrive un elemento di dati in un archivio protetto.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'Metodo IPStore:: WriteItem (PStore. h)'
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
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331467"
---
# <a name="ipstorewriteitem-method"></a>Metodo IPStore:: WriteItem

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Scrive un elemento di dati in un archivio protetto.

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

*Chiave* \[ di in\]
</dt> <dd>

Area di archiviazione del provider.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt> </dl>    | L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt> </dl> | L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.<br/> |



 

</dd> <dt>

*pItemType* \[ in\]
</dt> <dd>

Puntatore a un **GUID** che identifica il tipo di dati dell'elemento di dati in fase di scrittura.

</dd> <dt>

*pItemSubtype* \[ in\]
</dt> <dd>

Puntatore a un **GUID** che identifica il sottotipo di dati dell'elemento di dati da scrivere.

</dd> <dt>

*szItemName* \[ in\]
</dt> <dd>

Puntatore a una stringa che contiene il nome assegnato all'elemento di dati archiviato.

</dd> <dt>

*cbData* \[ out\]
</dt> <dd>

Puntatore a un **valore DWORD** che indica le dimensioni del buffer che contiene l'elemento dati archiviato.

</dd> <dt>

*ppbData* \[ out\]
</dt> <dd>

Puntatore a un buffer contenente l'elemento di dati in fase di scrittura.

</dd> <dt>

*pProomptInfo* \[ in\]
</dt> <dd>

Puntatore a una [**struttura \_ PROMPTINFO PST**](pst-promptinfo.md) .

</dd> <dt>

*dwDefaultConfirmationStyle* \[ in\]
</dt> <dd>

Stile di conferma predefinito.



| Valore                                                                                                                                                                                                                             | Significato                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <dt>**Pst \_ 0x00000000 \_ predefinito CF**</dt> <dt></dt> </dl> | Consente all'utente di scegliere lo stile di conferma. <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <dt>**Pst \_ CF \_ None**</dt> <dt>0x00000001</dt> </dl>          | Forza la creazione di elementi invisibile all'utente. <br/>                      |



 

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

L'interfaccia utente e i comportamenti di sicurezza per l'operazione di scrittura.



| Valore                                                                                                                                                                                                                                                              | Significato                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <dt>**Pst \_ Nessuna \_ sovrascrittura**</dt> <dt>0x00000002</dt> </dl>                            | Specifica che l'elemento deve essere creato nell'archivio protetto. La sovrascrittura di un elemento esistente non è consentita.<br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**Pst \_ 0x00000004 \_ ItemData senza restrizioni**</dt> <dt></dt> </dl> | Specifica che il flusso di dati non è sicuro. Per impostazione predefinita, le chiamate agli elementi sono sicure.<br/>                         |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT** . Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**\_PROMPTINFO PST**](pst-promptinfo.md)
</dt> </dl>

 

 
