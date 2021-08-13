---
title: DO_DOWNLOAD_STATUS struttura
description: Usato per ottenere lo stato di un download specifico.
keywords:
- DO_DOWNLOAD_STATUS struttura
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8775b7daf55d58698d00bcaa2820b909e302933c9f407d1cb6416d6b095a872b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543735"
---
# <a name="do_download_status-structure"></a>DO_DOWNLOAD_STATUS struttura

La **DO_DOWNLOAD_STATUS** struttura viene usata per ottenere lo stato di un download specifico. Viene ottenuto chiamando la **funzione IDODownload::GetStatus.**

## <a name="syntax"></a>Sintassi
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a>Members

`BytesTotal`

Numero totale di byte da scaricare.

`BytesTransferred`

Numero di byte già scaricati.

`State`

Stato di download corrente definito **dall'enumerazione DODownloadState.**

`Error`

Informazioni sull'errore (se presenti) associate al download corrente.

`ExtendedError`

Informazioni sull'errore estese (se presenti) associate al download corrente.

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, solo applicazioni Win32 versione 1809 \[\] |
| **Intestazione** | Do.h |
