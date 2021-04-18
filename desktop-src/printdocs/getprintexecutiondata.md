---
description: GetPrintExecutionData Recupera il contesto di stampa corrente.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Funzione GetPrintExecutionData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318379"
---
# <a name="getprintexecutiondata-function"></a>GetPrintExecutionData (funzione)

**GetPrintExecutionData** Recupera il contesto di stampa corrente.

> [!Note]  
> Questa funzione è destinata all'utilizzo da parte di driver della stampante eseguiti nel contesto dello spooler di stampa.

 

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve l'indirizzo della struttura dei [**\_ \_ dati di esecuzione di stampa**](print-execution-data.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se la funzione ha esito positivo; in caso contrario, **false**. Se il valore restituito è **false**, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere lo stato di errore.

## <a name="remarks"></a>Commenti

I driver della stampante devono chiamare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) nel modulo winspool. DRV per ottenere l'indirizzo della funzione **GetPrintExecutionData** , perché **GetPrintExecutionData** non è supportato in Windows Vista o nelle versioni precedenti di Windows.

**GetPrintExecutionData** ha esito negativo solo se il valore di *pData* è **null**.

Il valore del membro **clientAppPID** dei [**dati di \_ esecuzione \_ di stampa**](print-execution-data.md) è significativo solo se il valore di **context** è il contesto di **esecuzione di stampa \_ \_ \_ WOW64**. Se il valore di **context** non è **il \_ contesto di esecuzione di stampa \_ \_ WOW64**, il valore di **clientAppPID** è 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**\_contesto di esecuzione di stampa \_**](print-execution-context.md)
</dt> <dt>

[**STAMPA \_ dati di esecuzione \_**](print-execution-data.md)
</dt> </dl>

 

