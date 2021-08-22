---
description: Consente a un debugger di esaminare le informazioni della tabella di funzioni dinamiche.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: Funzione RtlGetFunctionTableListHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ff41aca0d268083132fd1a45371b0bb1ca026e5e6d693619ba1e2c2f9f2dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666731"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>Funzione RtlGetFunctionTableListHead

\[Questa funzione può essere modificata o rimossa da Windows senza ulteriori comunicazioni.\]

Consente a un debugger di esaminare le informazioni della tabella di funzioni dinamiche.

## <a name="syntax"></a>Sintassi


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'inizio dell'elenco di tabelle delle funzioni.

## <a name="remarks"></a>Commenti

Si noti che il file di intestazione Windows Driver Kit (WDK) Ntdef.h è necessario per alcune definizioni. La libreria di importazione associata, Ntdll.lib, è disponibile nel WDK. È anche possibile usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
