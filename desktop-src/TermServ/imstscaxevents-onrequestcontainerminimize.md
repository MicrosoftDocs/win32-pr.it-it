---
title: Metodo IMsTscAxEvents OnRequestContainerMinimize
description: Chiamato quando l'utente preme il pulsante Riduci a icona sulla barra di connessione in modalità schermo intero. L'attivazione di questo evento è una richiesta ridotta al minimo dall'applicazione contenitore.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Metodo OnRequestContainerMinimize Servizi Desktop remoto
- Metodo OnRequestContainerMinimize Servizi Desktop remoto , interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnRequestContainerMinimize
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 344bd85d8d224a5901517c55c8e0a95c854ed246e74a9d0c8def1eebae515305
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125061"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a>Metodo IMsTscAxEvents::OnRequestContainerMinimize

Chiamato quando l'utente preme il **pulsante Riduci** a icona sulla barra di connessione in modalità schermo intero. L'attivazione di questo evento è una richiesta ridotta al minimo dall'applicazione contenitore.

## <a name="syntax"></a>Sintassi


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo verrà chiamato solo se è abilitata la modalità schermo intero gestita dal contenitore. Per altre informazioni, vedere [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen.**](imstscadvancedsettings-containerhandledfullscreen.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





