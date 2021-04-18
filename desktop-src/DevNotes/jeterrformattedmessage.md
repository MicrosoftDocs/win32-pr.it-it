---
description: Recupera un identificatore del codice di errore (IDA) e crea la stringa di visualizzazione finale quando vengono forniti un errore Jet e informazioni estese sull'errore.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: JetErrFormattedMessage (funzione)
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
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324702"
---
# <a name="jeterrformattedmessage-function"></a>JetErrFormattedMessage (funzione)

Recupera un identificatore del codice di errore (IDA) e crea la stringa di visualizzazione finale quando vengono forniti un errore Jet e informazioni estese sull'errore.

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

Numero di errore Jet utilizzato per cercare e formattare il messaggio di errore visualizzabile.

</dd> <dt>

*pExtendedErrorInfo* 
</dt> <dd>

Tutte le informazioni sull'errore Jet, inclusi il nome del database, il nome della tabella e qualsiasi informazione secondaria sugli errori.

</dd> <dt>

*pIda* 
</dt> <dd>

Puntatore a IDA associato al codice di errore specifico.

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

Se la funzione ha esito positivo, restituisce **Jet \_ errSuccess**. in caso contrario, restituisce un messaggio di errore formattato che indica la causa specifica dell'errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
