---
description: Sospende i processi del pacchetto se sono in esecuzione.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: Metodo IPackageDebugSettings::Suspend
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
ms.openlocfilehash: 0517ce3cca6a8e74f19b053897511062cefa252297d3a0e6633d4678c0deaa95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822814"
---
# <a name="ipackagedebugsettingssuspend-method"></a>Metodo IPackageDebugSettings::Suspend

Sospende i processi del pacchetto se sono in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*packageFullName* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Nome completo del pacchetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                            | Descrizione                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione completata.<br/>              |
| <dl> <dt>**E \_ ILLEGAL \_ STATECHANGE**</dt> </dl> | Il processo non è attualmente in esecuzione.<br/> |



 

## <a name="remarks"></a>Commenti

Ogni processo riceve [**l'evento Suspending.**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) Può essere utile per gli sviluppatori illustrare in che modo le app rispondono a questo evento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
