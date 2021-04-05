---
description: Sospende i processi del pacchetto se sono attualmente in esecuzione.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'Metodo IPackageDebugSettings:: Suspend'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751495"
---
# <a name="ipackagedebugsettingssuspend-method"></a>Metodo IPackageDebugSettings:: Suspend

Sospende i processi del pacchetto se sono attualmente in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Suspend(
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

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                            | Descrizione                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Operazione completata.<br/>              |
| <dl> <dt>**E \_ STATECHANGE non valido \_**</dt> </dl> | Il processo non è attualmente in esecuzione.<br/> |



 

## <a name="remarks"></a>Commenti

Ogni processo riceve l'evento di [**sospensione**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) . Può essere utile per gli sviluppatori esaminare il modo in cui le app rispondono a questo evento.

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

 

 
