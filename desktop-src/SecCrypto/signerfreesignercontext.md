---
description: Libera una \_ struttura del contesto del firmatario allocata da una chiamata precedente alla funzione SignerSignEx.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: SignerFreeSignerContext (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314691"
---
# <a name="signerfreesignercontext-function"></a>SignerFreeSignerContext (funzione)

La funzione **SignerFreeSignerContext** libera una struttura del [**\_ contesto del firmatario**](signer-context.md) allocata da una chiamata precedente alla funzione [**SignerSignEx**](signersignex.md) .

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSignerContext* \[ in\]
</dt> <dd>

Puntatore alla struttura del [**\_ contesto del firmatario**](signer-context.md) da liberare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce S \_ OK.

Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**contesto del FIRMATARIo \_**](signer-context.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
