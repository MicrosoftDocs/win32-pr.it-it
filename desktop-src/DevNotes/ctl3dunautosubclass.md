---
description: Disattiva la sottoclasse automatica.
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Ctl3dUnAutoSubclass (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 1250deb16307400898c92d36b9dda214115ec01d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332100"
---
# <a name="ctl3dunautosubclass-function"></a>Ctl3dUnAutoSubclass (funzione)

Disattiva la sottoclasse automatica.

## <a name="syntax"></a>Sintassi


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se la funzione ha esito positivo; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
