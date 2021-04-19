---
description: Recupera una stringa di messaggio non formattata quando viene fornito un identificatore del codice di errore (IDA).
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: JetErrIDARawMessage (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332277"
---
# <a name="jeterridarawmessage-function"></a>JetErrIDARawMessage (funzione)

Recupera una stringa di messaggio non formattata quando viene fornito un identificatore del codice di errore (IDA).

## <a name="syntax"></a>Sintassi


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ida* 
</dt> <dd>

Numero che esegue il mapping a un codice di errore specifico e viene visualizzato all'utente.

</dd> <dt>

*pMessage* 
</dt> <dd>

Puntatore al messaggio di errore.

</dd> <dt>

*cbMessage* 
</dt> <dd>

Conteggio del numero di byte nel messaggio di errore.

</dd> <dt>

*pcbActual* 
</dt> <dd>

Puntatore al numero effettivo di byte letti.

</dd> <dt>

*pContextId* 
</dt> <dd>

Puntatore all'identificatore di contesto associato al file della guida.

</dd> <dt>

*pwszHelp/file* 
</dt> <dd>

Puntatore a un puntatore al file che spiega l'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **Jet \_ errSuccess**. in caso contrario, restituisce un messaggio non formattato che indica il motivo specifico dell'errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
