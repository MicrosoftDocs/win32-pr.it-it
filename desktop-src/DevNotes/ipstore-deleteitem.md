---
description: Elimina l'elemento specificato dall'archivio protetto.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: Metodo IPStore::D eleteItem (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331293"
---
# <a name="ipstoredeleteitem-method"></a>IPStore::D Metodo eleteItem

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Elimina l'elemento specificato dall'archivio protetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
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

Puntatore a un **GUID** che identifica il tipo di dati dell'elemento da eliminare.

</dd> <dt>

*pItemSubType* \[ in\]
</dt> <dd>

**GUID** che indica il sottotipo di elemento da eliminare.

</dd> <dt>

*szItemName* \[ in\]
</dt> <dd>

Stringa che contiene il nome dell'elemento da eliminare.

</dd> <dt>

*pPromptInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura [**\_ PROMPTINFO PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Specifica l'interfaccia utente e i comportamenti di sicurezza per l'operazione di eliminazione.



| Valore                                                                                                                                                                                                                                             | Significato                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**Pst \_ Nessuna \_ \_ migrazione dell'interfaccia utente**</dt> <dt>0x00000010</dt> </dl> | Non visualizzare l'interfaccia utente a meno che non sia necessaria una password personalizzata.<br/> |



 

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

 

 
