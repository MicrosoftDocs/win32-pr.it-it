---
description: Restituisce il puntatore a interfaccia di un sottotipo per l'enumerazione degli elementi nel database di archiviazione protetto.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: Metodo IPStore::EnumItems (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0b0ea4976dcfdfe2a099362e9a937ac69144bd678965c6a308cb96fed2a3c88b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001511"
---
# <a name="ipstoreenumitems-method"></a>Metodo IPStore::EnumItems

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Restituisce il puntatore a interfaccia di un sottotipo per l'enumerazione degli elementi nel database di archiviazione protetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Specifica se il tipo è locale per il computer o associato solo all'utente che crea.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHIAVE \_ UTENTE \_ CORRENTE**</dt> <dt>0x00000000</dt> </dl>    | L'archiviazione viene mantenuta nella sezione utente corrente del Registro di sistema.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CHIAVE \_ COMPUTER \_ LOCALE**</dt> <dt>0x00000001</dt> </dl> | L'archiviazione viene mantenuta nella sezione del computer locale del Registro di sistema.<br/> |



 

</dd> <dt>

*pItemType* \[ Pollici\]
</dt> <dd>

Puntatore a un **GUID che** identifica il tipo di dati dell'elemento da enumerare.

</dd> <dt>

*pItemSubtype* \[ Pollici\]
</dt> <dd>

Puntatore a un **GUID che** identifica il sottotipo di dati dell'elemento da enumerare.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Riservato: deve essere impostato su zero.

</dd> <dt>

*ppenum* \[ Pollici\]
</dt> <dd>

Puntatore a un puntatore a [**un'interfaccia IEnumPStoreItems.**](ienumpstoreitems.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore **PST \_ E \_ OK** indica che la funzione ha avuto esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
