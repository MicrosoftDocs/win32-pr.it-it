---
description: Recupera le informazioni associate a un sottotipo.
ms.assetid: 3daf5f37-9e7f-4ce1-bd35-d7e3c2ef5c28
title: 'Metodo IPStore:: GetSubtypeInfo (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetSubtypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: db7cb02d1c21b8bb1717514a6347339065e4f112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330868"
---
# <a name="ipstoregetsubtypeinfo-method"></a>Metodo IPStore:: GetSubtypeInfo

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Recupera le informazioni associate a un sottotipo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSubtypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in] const GUID          *pSubtype,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
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

*pType* \[ in\]
</dt> <dd>

Puntatore a un GUID che identifica il tipo di dati dell'archiviazione.

</dd> <dt>

*pSubtype* \[ in\]
</dt> <dd>

Puntatore a un GUID che identifica il sottotipo di dati dell'archiviazione.

</dd> <dt>

*ppInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura [**\_ TYPEINFO PST**](pst-typeinfo.md) .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Riservato: deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT** . Il valore PST \_ E \_ OK indica che la funzione ha avuto esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**\_TYPEINFO PST**](pst-typeinfo.md)
</dt> </dl>

 

 
