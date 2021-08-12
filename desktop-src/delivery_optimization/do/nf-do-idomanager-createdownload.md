---
title: Metodo IDOManager::CreateDownload
description: Crea un nuovo download.
keywords:
- Metodo IDOManager::CreateDownload
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 87b78afdf5687bb60efb77815898274a8fb405f588f28b263eb1b01a752a9bc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543838"
---
# <a name="idomanagercreatedownload-method"></a>Metodo IDOManager::CreateDownload

Crea un nuovo download.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a>Parametri

`download`

Indirizzo di un puntatore a **interfaccia IDODownload.**

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [.](/windows/desktop/com/com-error-codes-10)

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, solo applicazioni Win32 versione 1809 \[\] |
| **Intestazione** | Do.h |
