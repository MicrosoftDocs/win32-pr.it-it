---
description: Ricarica una configurazione IME dal registro di sistema HKCU, solo nell'IME giapponese.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: funzione reload_config
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: bc9d0d026359036d8847ebaa2542f778de4d5767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332655"
---
# <a name="reload_config-function"></a>ricarica \_ funzione di configurazione

Ricarica una configurazione IME dal registro di sistema HKCU, solo nell'IME giapponese.

## <a name="syntax"></a>Sintassi


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Se non è presente alcun valore del registro di sistema in HKCU, la funzione di **ricaricamento della \_ configurazione** scrive i dati iniziali nel registro di sistema.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt> </dl> |



 

 
