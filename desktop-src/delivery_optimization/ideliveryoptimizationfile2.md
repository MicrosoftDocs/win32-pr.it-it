---
title: Interfaccia IDeliveryOptimizationFile2
description: IDeliveryOptimizationFile2 supporta l'impostazione e il recupero di proprietà di file facoltative.
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
ms.openlocfilehash: ed7409635444885b662688ce94c300aae6e62186dd76bd7278b3e7445ef50c90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542046"
---
# <a name="ideliveryoptimizationfile2-interface"></a>Interfaccia IDeliveryOptimizationFile2

**IDeliveryOptimizationFile2** supporta l'impostazione e il recupero di proprietà di file facoltative. 

## <a name="members"></a>Membri

**L'interfaccia IDeliveryOptimizationFile2** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationFile2** include anche questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDeliveryOptimizationFile2** include questi metodi.

| Metodo                                                 | Descrizione                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**Getproperty**](ideliveryoptimizationfile2-getproperty.md)  | Questo metodo restituisce una singola proprietà del file DO. |
| [**SetProperty**](ideliveryoptimizationfile2-setproperty.md)  | Questo metodo imposta una singola proprietà del file DO.    |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato      | Windows 10, solo app desktop versione 1803 \[\]                                    |
| Server minimo supportato      | Windows Server, solo app desktop versione 1709 \[\]                                |
| Intestazione                        | Deliveryoptimization.h                                                            |
| Idl                           | DeliveryOptimization.idl                                                          |
| Libreria                       | Dosvc.lib                                                                         |
| DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 è definito come 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
