---
description: Legge l'elemento di dati specificato dall'archiviazione protetta.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: Metodo IPStore::ReadItem (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 516eb55772e375d09d3b134dee456c090cf11d6ef0d10905f99a822b1df0d9e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001490"
---
# <a name="ipstorereaditem-method"></a>Metodo IPStore::ReadItem

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Legge l'elemento di dati specificato dall'archiviazione protetta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Area di archiviazione del provider.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ KEY \_ CURRENT \_ USER**</dt> <dt>0x00000000</dt> </dl>    | L'archiviazione viene gestita nella sezione utente corrente del Registro di sistema.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CHIAVE \_ DEL \_ COMPUTER**</dt> LOCALE <dt>0x00000001</dt> </dl> | L'archiviazione viene gestita nella sezione del computer locale del Registro di sistema.<br/> |



 

</dd> <dt>

*pItemType* \[ Pollici\]
</dt> <dd>

Puntatore a un GUID che identifica il tipo di dati dell'elemento da leggere.

</dd> <dt>

*pItemSubtype* \[ Pollici\]
</dt> <dd>

Puntatore a un GUID che identifica il sottotipo di dati dell'elemento da leggere.

</dd> <dt>

*szItemName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa contenente il nome assegnato all'elemento di dati archiviato.

</dd> <dt>

*cbData* \[ Pollici\]
</dt> <dd>

Valore **DWORD** che indica le dimensioni del buffer che contiene l'elemento di dati archiviato.

</dd> <dt>

*pbData* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che contiene l'elemento di dati archiviato.

</dd> <dt>

*pPromptInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ PROMPTINFO PST.**](pst-promptinfo.md)

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Specifica l'interfaccia utente e i comportamenti di sicurezza per l'operazione di lettura.

I valori del flag possono essere combinati con un OR logico.



| Valore                                                                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ ITEMDATA \_ SENZA**</dt> <dt>RESTRIZIONI</dt> 0x00000004 </dl> | Specifica che il flusso di dati non è sicuro. Per impostazione predefinita, le chiamate all'elemento sono sicure.<br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <dt>**PST \_ Prompt \_ QUERY**</dt> <dt>0x00000008</dt> </dl>                            | Specifica che la conferma deve essere restituita in seguito all'esito positivo. Se l'interfaccia utente è abilitata, viene restituito un esito positivo di **PST \_ E \_ OK.** Se l'interfaccia utente non è abilitata, viene restituito il valore **PST \_ E ITEM \_ \_ EXISTS.**<br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_ NO \_ UI \_ MIGRATION**</dt> <dt>0x00000010</dt> </dl>                  | Non visualizzare l'interfaccia utente a meno che non sia necessaria una password personalizzata.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un **valore HRESULT.** Il valore **PST \_ E \_ OK** indica che la funzione ha avuto esito positivo.

## <a name="remarks"></a>Commenti

Se **ReadItem** viene completato correttamente, l'applicazione è responsabile di liberare il buffer di dati restituito usando la [**funzione CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Archivio IP**](ipstore.md)
</dt> <dt>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)
</dt> </dl>

 

 
