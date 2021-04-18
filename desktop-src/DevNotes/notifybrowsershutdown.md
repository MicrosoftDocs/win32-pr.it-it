---
description: Libera i caricatori di classi Java che potrebbero essere stati usati durante l'esplorazione degli Apple.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: NotifyBrowserShutdown (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327845"
---
# <a name="notifybrowsershutdown-function"></a>NotifyBrowserShutdown (funzione)

Libera i caricatori di classi Java che potrebbero essere stati usati durante l'esplorazione degli Apple.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpvReserved* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **\_ OK**. In caso contrario, il valore restituito è un codice di errore.

## <a name="remarks"></a>Commenti

Quando il conteggio delle finestre del browser raggiunge lo zero in modalità Web integrata, questa funzione libera i caricatori di classi Java. Quando l'utente inizia a esplorare di nuovo gli Apple, la VM Java scaricherà i file di classe più recenti.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
