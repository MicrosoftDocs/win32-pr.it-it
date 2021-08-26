---
description: Ottiene IMFDXGIDeviceManager dal sink Microsoft Media Foundation rendering video.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: Metodo IMFDXGIDeviceManagerSource::GetManager
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 9e42e42e88dfa2acec9061a54f3a8fcc96128ad5aee6ff004e49f6dd10062074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957832"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a>Metodo IMFDXGIDeviceManagerSource::GetManager

Ottiene [**IMFDXGIDeviceManager dal**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) sink Microsoft Media Foundation rendering video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PpManager* \[ Cambio\]
</dt> <dd>

Oggetto [**IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| per app UWP\]<br/>                       |
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFDXGIDeviceManagerSource**](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




