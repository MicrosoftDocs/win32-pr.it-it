---
title: Interfaccia IDeliveryOptimizationJob (Deliveryoptimization. h)
description: Usare l'interfaccia IDeliveryOptimizationJob per scaricare gli intervalli di un file.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Interfaccia IDeliveryOptimizationJob
- Interfaccia IDeliveryOptimizationJob, descritta
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119754"
---
# <a name="ideliveryoptimizationjob-interface"></a>Interfaccia IDeliveryOptimizationJob

Usare l'interfaccia **IDeliveryOptimizationJob** per scaricare gli intervalli di un file.

## <a name="members"></a>Membri

L'interfaccia **IDeliveryOptimizationJob** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationJob** dispone anche di questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDeliveryOptimizationJob** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**AddFileWithRanges**](ideliveryoptimizationjob-addfilewithranges.md) | Aggiunge un file a un processo di download e specifica gli intervalli del file che si desidera scaricare.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob viene definito come EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



 

