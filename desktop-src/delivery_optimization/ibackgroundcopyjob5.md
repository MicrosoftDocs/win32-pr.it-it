---
title: Interfaccia IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Usare questa interfaccia per eseguire una query o impostare diversi comportamenti facoltativi di un processo.
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
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120867"
---
# <a name="ibackgroundcopyjob5-interface"></a>Interfaccia IBackgroundCopyJob5

Usare questa interfaccia per eseguire una query o impostare diversi comportamenti facoltativi di un processo.

Per ottenere questa interfaccia, chiamare il metodo **Metodo ibackgroundcopyjob:: QueryInterface** usando `__uuidof(IBackgroundCopyJob5)` come identificatore di interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IBackgroundCopyJob5** eredita da [**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md). **IBackgroundCopyJob5** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IBackgroundCopyJob5** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyjob5-getproperty.md) | Metodo generico per ottenere le proprietà del processo.<br/> |
| [**SetProperty**](ibackgroundcopyjob5-setproperty.md) | Metodo generico per l'impostazione delle proprietà del processo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 viene definito come E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





