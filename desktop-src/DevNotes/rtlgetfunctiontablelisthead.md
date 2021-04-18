---
description: Consente a un debugger di esaminare le informazioni sulla tabella della funzione dinamica.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: RtlGetFunctionTableListHead (funzione)
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
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330959"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>RtlGetFunctionTableListHead (funzione)

\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]

Consente a un debugger di esaminare le informazioni sulla tabella della funzione dinamica.

## <a name="syntax"></a>Sintassi


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'inizio dell'elenco della tabella di funzioni.

## <a name="remarks"></a>Commenti

Si noti che il file di intestazione di Windows Driver Kit (WDK) Ntdef. h è necessario per alcune definizioni. La libreria di importazione associata, Ntdll. lib, è disponibile in WDK. È anche possibile usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire un collegamento dinamico a Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
