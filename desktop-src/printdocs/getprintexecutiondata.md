---
description: GetPrintExecutionData recupera il contesto di stampa corrente.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Funzione GetPrintExecutionData (Winspool.h)
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
ms.openlocfilehash: 0bbe08e82fb8f753d6e4fd23776618cb5f555b390434fdd0feddd231aaebc635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971350"
---
# <a name="getprintexecutiondata-function"></a>Funzione GetPrintExecutionData

**GetPrintExecutionData** recupera il contesto di stampa corrente.

> [!Note]  
> Questa funzione è destinata all'uso da parte dei driver della stampante in esecuzione nel contesto dello spooler di stampa.

 

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve l'indirizzo della [**struttura PRINT \_ EXECUTION \_**](print-execution-data.md) DATA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se la funzione ha esito positivo. in caso **contrario, FALSE.** Se il valore restituito è **FALSE,** chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere lo stato dell'errore.

## <a name="remarks"></a>Commenti

I driver della stampante devono chiamare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) nel modulo winspool.drv per ottenere l'indirizzo della funzione **GetPrintExecutionData** perché **GetPrintExecutionData** non è supportato in Windows Vista o nelle versioni precedenti di Windows.

**GetPrintExecutionData** ha esito negativo solo se il valore di *pData* è **NULL.**

Il valore del **membro clientAppPID** di [**PRINT EXECUTION \_ \_ DATA**](print-execution-data.md) è significativo solo se il valore del contesto è **PRINT EXECUTION CONTEXT \_ \_ \_ WOW64.**  Se il valore di **context** non è **PRINT EXECUTION CONTEXT \_ \_ \_ WOW64,** il valore **di clientAppPID** è 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Getlasterror**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**CONTESTO \_ DI ESECUZIONE DELLA \_ STAMPA**](print-execution-context.md)
</dt> <dt>

[**STAMPARE I \_ DATI DI \_ ESECUZIONE**](print-execution-data.md)
</dt> </dl>

 

