---
description: Legge l'elemento dati specificato dall'archivio protetto.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'Metodo IPStore:: ReadItem (PStore. h)'
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
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331665"
---
# <a name="ipstorereaditem-method"></a>Metodo IPStore:: ReadItem

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Legge l'elemento dati specificato dall'archivio protetto.

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

Puntatore a un GUID che identifica il tipo di dati dell'elemento da leggere.

</dd> <dt>

*pItemSubtype* \[ in\]
</dt> <dd>

Puntatore a un GUID che identifica il sottotipo di dati dell'elemento da leggere.

</dd> <dt>

*szItemName* \[ in\]
</dt> <dd>

Puntatore a una stringa che contiene il nome assegnato all'elemento di dati archiviato.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

**Valore DWORD** che indica le dimensioni del buffer che contiene l'elemento dati archiviato.

</dd> <dt>

*pbData* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene l'elemento di dati archiviato.

</dd> <dt>

*pPromptInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura [**\_ PROMPTINFO PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Specifica l'interfaccia utente e i comportamenti di sicurezza per l'operazione di lettura.

I valori dei flag possono essere combinati con un OR logico.



| Valore                                                                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**Pst \_ 0x00000004 \_ ItemData senza restrizioni**</dt> <dt></dt> </dl> | Specifica che il flusso di dati non è sicuro. Per impostazione predefinita, le chiamate agli elementi sono sicure.<br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <dt>**Pst \_ Richiedi \_ query**</dt> <dt>0x00000008</dt> </dl>                            | Specifica che la conferma viene restituita al completamento dell'operazione. Se l'interfaccia utente è abilitata, viene restituito un esito positivo di **pst \_ E \_ OK** . Se l'interfaccia utente non è abilitata, viene restituito un valore di **pst \_ E \_ Item \_** .<br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**Pst \_ Nessuna \_ \_ migrazione dell'interfaccia utente**</dt> <dt>0x00000010</dt> </dl>                  | Non visualizzare l'interfaccia utente a meno che non sia necessaria una password personalizzata.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT** . Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.

## <a name="remarks"></a>Commenti

Se **ReadItem** viene completato correttamente, l'applicazione deve liberare il buffer di dati restituito tramite la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .

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

 

 
