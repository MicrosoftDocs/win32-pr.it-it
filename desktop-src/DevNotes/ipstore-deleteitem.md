---
description: Elimina l'elemento specificato dall'archivio protetto.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: Metodo IPStore::D eleteItem (Pstore.h)
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
ms.openlocfilehash: e99a2ec9b39b035b4a4af24aa18c2936decd399043cc507ed0bf279c5696fd53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667452"
---
# <a name="ipstoredeleteitem-method"></a>Metodo IPStore::D eleteItem

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

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

Puntatore a un **GUID** che identifica il tipo di dati dell'elemento da eliminare.

</dd> <dt>

*pItemSubType* \[ Pollici\]
</dt> <dd>

GUID **che** indica il sottotipo di elemento da eliminare.

</dd> <dt>

*szItemName* \[ Pollici\]
</dt> <dd>

Stringa contenente il nome dell'elemento da eliminare.

</dd> <dt>

*pPromptInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ PROMPTINFO PST.**](pst-promptinfo.md)

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Specifica l'interfaccia utente e i comportamenti di sicurezza per l'operazione di eliminazione.



| Valore                                                                                                                                                                                                                                             | Significato                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_ NESSUNA \_ MIGRAZIONE \_ DELL'INTERFACCIA**</dt> <dt>0X00000010</dt> </dl> | Non visualizzare l'interfaccia utente a meno che non sia necessaria una password personalizzata.<br/> |



 

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

 

 
