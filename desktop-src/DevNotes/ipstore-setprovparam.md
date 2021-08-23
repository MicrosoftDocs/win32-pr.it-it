---
description: Imposta le informazioni sui parametri specificati.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: Metodo IPStore::SetProvParam (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9ec106cd4558ddab7fd8bc430088f1bd7d721d7122f77166dfe0da7de35f1787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749721"
---
# <a name="ipstoresetprovparam-method"></a>Metodo IPStore::SetProvParam

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Imposta le informazioni sui parametri specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwParam* \[ Pollici\]
</dt> <dd>

Contiene **PST PP FLUSH \_ \_ \_ PW CACHE \_ per** scaricare la cache delle password utente.

</dd> <dt>

*cbData* \[ Pollici\]
</dt> <dd>

Lunghezza della password nel buffer.

</dd> <dt>

*pbData* 
</dt> <dd>

Puntatore a un buffer che contiene la password dell'utente. Deve essere impostato su **NULL.**

</dd> <dt>

*dwFlags* 
</dt> <dd>

Riservato: deve essere impostato su zero.

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
</dt> </dl>

 

 
