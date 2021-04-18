---
title: Struttura DO_DOWNLOAD_STATUS
description: Utilizzato per ottenere lo stato di un download specifico.
keywords:
- Struttura DO_DOWNLOAD_STATUS
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
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299299"
---
# <a name="do_download_status-structure"></a>Struttura DO_DOWNLOAD_STATUS

La struttura **DO_DOWNLOAD_STATUS** viene utilizzata per ottenere lo stato di un download specifico. Viene ottenuto chiamando la funzione **IDODownload:: GetStatus** .

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

Stato di download corrente in base a quanto definito dall'enumerazione **DODownloadState** .

`Error`

Informazioni sull'errore, se esistenti, associate al download corrente.

`ExtendedError`

Informazioni estese sull'errore, se esistenti, associate al download corrente.

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |
