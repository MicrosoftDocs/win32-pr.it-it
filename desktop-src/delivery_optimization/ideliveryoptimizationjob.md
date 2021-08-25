---
title: Interfaccia IDeliveryOptimizationJob (Deliveryoptimization.h)
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
ms.openlocfilehash: 71f978be993e21ad487af5469327b5f66804166a7e5247dffb841f7815b2279e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895681"
---
# <a name="ideliveryoptimizationjob-interface"></a>Interfaccia IDeliveryOptimizationJob

Usare **l'interfaccia IDeliveryOptimizationJob** per scaricare gli intervalli di un file.

## <a name="members"></a>Membri

**L'interfaccia IDeliveryOptimizationJob** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationJob** include anche questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDeliveryOptimizationJob** include questi metodi.



| Metodo                                                                  | Descrizione                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**AddFileWithRanges**](ideliveryoptimizationjob-addfilewithranges.md) | Aggiunge un file a un processo di download e specifica gli intervalli del file da scaricare.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob è definito come EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



 

