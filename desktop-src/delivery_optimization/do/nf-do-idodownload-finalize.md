---
title: Metodo IDODownload::Finalize
description: Finalizza il download.
keywords:
- Metodo IDODownload::Finalize
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 620b8cf1671c18f2e4a79a798fac366d61c9e09f5a83ecda2c1ade531c6a558a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636035"
---
# <a name="idodownloadfinalize-method"></a>Metodo IDODownload::Finalize

Finalizza il download. Una volta finalizzato, un download non può essere ripreso chiamando **Start.**

## <a name="syntax"></a>Sintassi

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | Do.h |
