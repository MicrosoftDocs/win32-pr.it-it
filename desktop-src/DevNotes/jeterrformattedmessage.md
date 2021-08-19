---
description: Recupera un identificatore di codice di errore (IDA) e crea la stringa di visualizzazione finale quando vengono forniti un errore Jet e informazioni estese sull'errore.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: Funzione JetErrFormattedMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8b0fa6eb0ac4bc29e5657d3e58d9be1c27188a0faf7c7d68281ceca239dea8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955780"
---
# <a name="jeterrformattedmessage-function"></a>Funzione JetErrFormattedMessage

Recupera un identificatore di codice di errore (IDA) e crea la stringa di visualizzazione finale quando vengono forniti un errore Jet e informazioni estese sull'errore.

## <a name="syntax"></a>Sintassi


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
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

Numero di errore jet utilizzato per cercare e formattare il messaggio di errore visualizzabile.

</dd> <dt>

*pExtendedErrorInfo* 
</dt> <dd>

Tutte le informazioni sugli errori jet, inclusi il nome del database, il nome della tabella e le eventuali informazioni sugli errori secondari.

</dd> <dt>

*Pida* 
</dt> <dd>

Puntatore all'IDA associato al codice di errore specifico.

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

Puntatore all'identificatore di contesto associato al file della Guida.

</dd> <dt>

*pwszHelp/file* 
</dt> <dd>

Puntatore a un puntatore al file che spiega l'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **JET \_ errSuccess;** in caso contrario, restituisce un messaggio di errore formattato che indica il motivo specifico dell'errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
