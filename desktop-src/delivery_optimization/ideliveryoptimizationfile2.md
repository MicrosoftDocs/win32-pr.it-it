---
title: Interfaccia IDeliveryOptimizationFile2
description: IDeliveryOptimizationFile2 supporta l'impostazione e il recupero di proprietà facoltative dei file.
keywords:
- Interfaccia IDeliveryOptimizationFile2
- Interfaccia IDeliveryOptimizationFile2, descritta
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048133"
---
# <a name="ideliveryoptimizationfile2-interface"></a>Interfaccia IDeliveryOptimizationFile2

**IDeliveryOptimizationFile2** supporta l'impostazione e il recupero di proprietà facoltative dei file. 

## <a name="members"></a>Membri

L'interfaccia **IDeliveryOptimizationFile2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationFile2** dispone anche di questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDeliveryOptimizationFile2** dispone di questi metodi.

| Metodo                                                 | Descrizione                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**GetProperty**](ideliveryoptimizationfile2-getproperty.md)  | Questo metodo restituisce una singola proprietà del file DO. |
| [**SetProperty**](ideliveryoptimizationfile2-setproperty.md)  | Questo metodo imposta una singola proprietà del file DO.    |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato      | Solo app desktop Windows 10 versione 1803 \[\]                                    |
| Server minimo supportato      | Windows Server, versione 1709 \[ solo per le app desktop\]                                |
| Intestazione                        | Deliveryoptimization. h                                                            |
| IDL                           | DeliveryOptimization. idl                                                          |
| Libreria                       | Dosvc. lib                                                                         |
| DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 viene definito come 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
