---
title: Interfaccia IBackgroundCopyJob5 (Deliveryoptimization.h)
description: Usare questa interfaccia per eseguire query o impostare diversi comportamenti facoltativi di un processo.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- Interfaccia IBackgroundCopyJob5
- Interfaccia IBackgroundCopyJob5, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 593f06f74dde7e6891417871cd16dc3730ef005fb90a0a1b6cf5377fda7ebcd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461971"
---
# <a name="ibackgroundcopyjob5-interface"></a>Interfaccia IBackgroundCopyJob5

Usare questa interfaccia per eseguire query o impostare diversi comportamenti facoltativi di un processo.

Per ottenere questa interfaccia, chiamare il **metodo IBackgroundCopyJob::QueryInterface** usando `__uuidof(IBackgroundCopyJob5)` come identificatore di interfaccia.

## <a name="members"></a>Membri

**L'interfaccia IBackgroundCopyJob5** eredita da [**IBackgroundCopyJob**](ibackgroundcopyjob-.md). **IBackgroundCopyJob5** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IBackgroundCopyJob5** include questi metodi.



| Metodo                                                 | Descrizione                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**Getproperty**](ibackgroundcopyjob5-getproperty.md) | Metodo generico per ottenere le proprietà del processo DO.<br/> |
| [**SetProperty**](ibackgroundcopyjob5-setproperty.md) | Metodo generico per l'impostazione delle proprietà del processo DO.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 definito come E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





