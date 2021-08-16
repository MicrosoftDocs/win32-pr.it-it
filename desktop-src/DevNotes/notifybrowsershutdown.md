---
description: Libera i caricatori di classe Java che potrebbero essere stati utilizzati durante l'esplorazione delle applet.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: Funzione NotifyBrowserShutdown
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
ms.openlocfilehash: 60f361d8f9963081c4af2a840a01eb29f9946eb064cad2335f95b3622932add1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826817"
---
# <a name="notifybrowsershutdown-function"></a>Funzione NotifyBrowserShutdown

Libera i caricatori di classe Java che potrebbero essere stati utilizzati durante l'esplorazione delle applet.

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

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**. In caso contrario, il valore restituito è un codice di errore.

## <a name="remarks"></a>Commenti

Quando il numero di finestre del browser raggiunge zero in modalità Web integrata, questa funzione libera i caricatori di classe Java. Quando l'utente avvia nuovamente l'esplorazione delle applet, la macchina virtuale Java scaricherà i file di classe più recenti.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
