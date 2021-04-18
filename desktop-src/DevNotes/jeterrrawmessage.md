---
description: Recupera un identificatore del codice di errore (IDA) e una stringa di messaggio non formattato quando viene fornito un errore Jet.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: JetErrRawMessage (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324797"
---
# <a name="jeterrrawmessage-function"></a>JetErrRawMessage (funzione)

Recupera un identificatore del codice di errore (IDA) e una stringa di messaggio non formattato quando viene fornito un errore Jet.

## <a name="syntax"></a>Sintassi


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Err* 
</dt> <dd>

Errore Jet che corrisponde alle informazioni ottenute.

</dd> <dt>

*pIda* 
</dt> <dd>

Puntatore a IDA.

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

Punta a un puntatore al file che spiega l'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **Jet \_ errSuccess**. in caso contrario, restituisce un messaggio di errore non formattato che indica il motivo specifico dell'errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
