---
description: Apre un elemento per più accessi.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'Metodo IPStore:: OpenItem (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324279"
---
# <a name="ipstoreopenitem-method"></a>Metodo IPStore:: OpenItem

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Apre un elemento per più accessi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ di in\]
</dt> <dd>

Specifica se il tipo è locale o associato solo all'utente che ha creato il computer.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt> </dl>    | L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt> </dl> | L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.<br/> |



 

</dd> <dt>

*pItemType* \[ in\]
</dt> <dd>

Puntatore a un GUID che identifica il tipo di dati dell'elemento da aprire.

</dd> <dt>

*pItemSubtype* \[ in\]
</dt> <dd>

Puntatore a un GUID che indica il sottotipo di elemento da aprire.

</dd> <dt>

*szItemName* \[ in\]
</dt> <dd>

Stringa che contiene il nome dell'elemento da aprire.

</dd> <dt>

*ModeFlags* \[ in\]
</dt> <dd>

Descrive le modalità di accesso a cui si riferisce un set specificato di clausole di accesso. Per altre informazioni, vedere [**tipi di PStore**](pstore-types.md).



| Valore                                                                                                                                                                                                         | Significato                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**Pst \_ Leggi**</dt> <dt>0x0001</dt> </dl>    | Modalità di accesso in lettura.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**Pst \_ Scrivi**</dt> <dt>0x0002</dt> </dl> | Modalità di accesso in scrittura.<br/> |



 

</dd> <dt>

*pProomptInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura [**\_ PROMPTINFO PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Riservato: deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT** . Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.

## <a name="remarks"></a>Commenti

Per aprire un elemento nel database di archiviazione protetta, l'uso di **OpenItem** richiede la chiusura finale con [**IPStore:: CloseItem**](ipstore-closeitem.md) per impedire una perdita di memoria.

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

 

 
