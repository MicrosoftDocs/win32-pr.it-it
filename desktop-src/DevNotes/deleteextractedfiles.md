---
description: La funzione DeleteExtractedFiles Elimina i file estratti dalla funzione Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: DeleteExtractedFiles (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327451"
---
# <a name="deleteextractedfiles-function"></a>DeleteExtractedFiles (funzione)

\[Questa funzione non è più supportata, pertanto non è possibile garantirne il comportamento.\]

La funzione **DeleteExtractedFiles** Elimina i file estratti dalla funzione [**Extract**](extract.md) .

## <a name="syntax"></a>Sintassi


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ps* 
</dt> <dd>

Puntatore a una struttura di [**sessione**](session.md) che contiene informazioni sulla sessione corrente.

Questa funzione libera la memoria nel membro **pFileList** della struttura e imposta **pFileList** su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Estrarre**](extract.md)
</dt> <dt>

[**SESSIONE**](session.md)
</dt> </dl>

 

 
