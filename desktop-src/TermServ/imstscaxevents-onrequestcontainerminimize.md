---
title: Metodo IMsTscAxEvents OnRequestContainerMinimize
description: Chiamato quando l'utente preme il pulsante Riduci a icona sulla barra delle connessioni in modalità schermo intero. L'attivazione di questo evento è una richiesta che l'applicazione contenitore è ridotta a icona.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRequestContainerMinimize
- Metodo OnRequestContainerMinimize Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRequestContainerMinimize
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
ms.openlocfilehash: 85387e3b156eed29dc7068eac84280be521a934e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400734"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a>Metodo IMsTscAxEvents:: OnRequestContainerMinimize

Chiamato quando l'utente preme il pulsante **Riduci a icona** sulla barra delle connessioni in modalità schermo intero. L'attivazione di questo evento è una richiesta che l'applicazione contenitore è ridotta a icona.

## <a name="syntax"></a>Sintassi


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo verrà chiamato solo se la modalità a schermo intero gestita dal contenitore è abilitata. per ulteriori informazioni, vedere [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) .

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

 

 





