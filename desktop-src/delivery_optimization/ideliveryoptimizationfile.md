---
title: Interfaccia IDeliveryOptimizationFile
description: Implementare l'interfaccia IDeliveryOptimizationFile per identificare lo stato di un file specifico.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Interfaccia IDeliveryOptimizationFile
- Interfaccia IDeliveryOptimizationFile, descritta
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301434"
---
# <a name="ideliveryoptimizationfile-interface"></a>Interfaccia IDeliveryOptimizationFile

Implementare l'interfaccia **IDeliveryOptimizationFile** per identificare lo stato di un file specifico.

## <a name="members"></a>Membri

L'interfaccia **IDeliveryOptimizationFile** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationFile** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDeliveryOptimizationFile** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**GetStats**](ideliveryoptimizationfile-getstats.md) | Restituisce le statistiche di download e caricamento per un file specifico.<br/> |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato      | Solo app desktop Windows 10 versione 1709 \[\]                                   |
| Server minimo supportato      | Windows Server, versione 1709 \[ solo per le app desktop\]                               |
| Intestazione                        | Deliveryoptimization. h                                                           |
| IDL                           | DeliveryOptimization. idl                                                         |
| Libreria                       | Dosvc. lib                                                                        |
| DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile viene definito come B76B9699-E99E-4101-803F-A20E325D93E2 |
