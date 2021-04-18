---
description: Inizializza una tabella di stringhe.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: pSetupStringTableInitializeEx (funzione)
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
ms.openlocfilehash: d40f221656da4cada610e7254b392bb2bd627a14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325201"
---
# <a name="psetupstringtableinitializeex-function"></a>pSetupStringTableInitializeEx (funzione)

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

*ExtraDataSize* \[ in\]
</dt> <dd>

Dimensioni dell'oggetto dati aggiuntivo.

</dd> <dt>

*Riservato* \[ in\]
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
