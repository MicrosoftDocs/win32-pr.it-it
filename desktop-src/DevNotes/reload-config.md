---
description: Ricarica una configurazione IME dal registro HKCU, solo in giapponese.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: reload_config funzione
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
ms.openlocfilehash: 343003156c2f93788ac87004657a21d3e9b31a47ff4585374836488642de3240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571621"
---
# <a name="reload_config-function"></a>Funzione reload \_ config

Ricarica una configurazione IME dal registro HKCU, solo in giapponese.

## <a name="syntax"></a>Sintassi


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE** se ha esito positivo; In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Se in HKCU non è presente alcun valore del Registro di sistema, la funzione di configurazione **reload \_** scrive i dati iniziali nel Registro di sistema.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt> </dl> |



 

 
