---
title: Metodo IDOManager::EnumDownloads
description: Recupera un puntatore a interfaccia a un oggetto enumeratore utilizzato per enumerare i download esistenti.
keywords:
- Metodo IDOManager::EnumDownloads
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5442196b95e654755b4f84fe85375afb8f5b9372ddae453ca4ddffb567882fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543828"
---
# <a name="idomanagerenumdownloads-method"></a>Metodo IDOManager::EnumDownloads

Recupera un puntatore a interfaccia a un oggetto enumeratore utilizzato per enumerare i download esistenti.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a>Parametri

`category`

Facoltativo. Nome della proprietà da utilizzare come categoria da enumerare. Il `nullptr` passaggio recupererà tutti i download esistenti. Le proprietà seguenti sono supportate come categoria.

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`ppEnum`

Indirizzo di un puntatore a interfaccia **a IEnumUnknown,** usato per enumerare i download esistenti. Il contenuto dell'enumeratore dipende dal valore della *categoria*. I download inclusi nell'interfaccia di enumerazione sono quelli creati in precedenza dallo stesso chiamante per questa funzione. 

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | Do.h |
