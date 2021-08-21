---
description: La funzione DeleteExtractedFiles elimina i file estratti dalla funzione Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: Funzione DeleteExtractedFiles
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
ms.openlocfilehash: 500de4df41c82f1956f50abcc25dc84f11484b693dc8d1a5f8bc53ab556ade0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162092"
---
# <a name="deleteextractedfiles-function"></a>Funzione DeleteExtractedFiles

\[Questa funzione non è più supportata, quindi non è possibile garantirne il comportamento.\]

La **funzione DeleteExtractedFiles** elimina i file estratti dalla [**funzione Extract.**](extract.md)

## <a name="syntax"></a>Sintassi


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ps* 
</dt> <dd>

Puntatore a una [**struttura SESSION**](session.md) che contiene informazioni sulla sessione corrente.

Questa funzione libera la memoria nel **membro pFileList** di questa struttura e imposta **pFileList** su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Estrazione**](extract.md)
</dt> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

 
