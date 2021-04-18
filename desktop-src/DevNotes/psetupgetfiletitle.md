---
description: Recupera il titolo del file per il percorso del file specificato.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: pSetupGetFileTitle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325097"
---
# <a name="psetupgetfiletitle-function"></a>pSetupGetFileTitle (funzione)

\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]

Recupera il titolo del file per il percorso del file specificato.

## <a name="syntax"></a>Sintassi


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FilePath* \[ in\]
</dt> <dd>

Percorso del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Puntatore a una stringa che riceve il titolo del file.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
