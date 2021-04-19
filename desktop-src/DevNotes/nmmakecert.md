---
description: Consente di creare un certificato utente da utilizzare con la conferenza di NetMeeting.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: NmMakeCert (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329888"
---
# <a name="nmmakecert-function"></a>NmMakeCert (funzione)

Consente di creare un certificato utente da utilizzare con la conferenza di NetMeeting.

## <a name="syntax"></a>Sintassi


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szFirstName* 
</dt> <dd>

Nome dell'utente.

</dd> <dt>

*szLastName* 
</dt> <dd>

Cognome dell'utente.

</dd> <dt>

*szEmailName* 
</dt> <dd>

Nome dell'indirizzo di posta elettronica dell'utente.

</dd> <dt>

*szCity* 
</dt> <dd>

la città dell'utente.

</dd> <dt>

*szCountry* 
</dt> <dd>

Paese o area geografica dell'utente.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Valore che indica la modalità di creazione del certificato. I valori possibili sono i seguenti.



| Valore                                                                                                                                                                                                                                                            | Significato                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <dt>**Nmmkcert \_ F \_ \_ solo pulizia**</dt> <dt>0x00000004</dt> </dl>    | Eliminare il certificato precedente senza crearne uno nuovo. <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <dt>**Nmmkcert \_ F \_ DELETEOLDCERT**</dt> <dt>0x00000001</dt> </dl>  | Eliminare il certificato precedente creato in precedenza con questa funzione. <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <dt>**Nmmkcert \_ F \_ \_ computer locale**</dt> <dt>0x00000002</dt> </dl> | Creare il certificato nell'archivio certificati del computer locale. <br/>    |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 se la funzione ha esito positivo e-1 se la funzione ha esito negativo.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Nmmkcert.dll</dt> </dl> |



 

 
