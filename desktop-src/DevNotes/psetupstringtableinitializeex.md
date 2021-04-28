---
description: 'Funzione pSetupStringTableInitializeEx: inizializza una tabella di stringhe.'
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: Funzione pSetupStringTableInitializeEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 78ee96e7e366fdff821e8202300ff28de0a14af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096649"
---
# <a name="psetupstringtableinitializeex-function"></a>Funzione pSetupStringTableInitializeEx

\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]

Inizializza una tabella di stringhe.

## <a name="syntax"></a>Sintassi


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ExtraDataSize* \[ Pollici\]
</dt> <dd>

Dimensioni dell'oggetto dati aggiuntivo.

</dd> <dt>

*Riservato* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
