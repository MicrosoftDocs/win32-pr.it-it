---
description: Riprende i processi del pacchetto se sono attualmente sospesi.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'Metodo IPackageDebugSettings:: Resume'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307075"
---
# <a name="ipackagedebugsettingsresume-method"></a>Metodo IPackageDebugSettings:: Resume

Riprende i processi del pacchetto se sono attualmente sospesi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PackageFullName* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Nome completo del pacchetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Ogni processo riceve l'evento di [**ripresa**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) . Può essere utile per gli sviluppatori esaminare il modo in cui le app rispondono a questo evento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| IDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
