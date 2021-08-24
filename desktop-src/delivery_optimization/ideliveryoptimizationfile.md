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
ms.openlocfilehash: 880cc982d32e2a81b4263c3cba55331ea5524643adfc8483ed96465154d47cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635741"
---
# <a name="ideliveryoptimizationfile-interface"></a>Interfaccia IDeliveryOptimizationFile

Implementare **l'interfaccia IDeliveryOptimizationFile** per identificare lo stato di un file specifico.

## <a name="members"></a>Membri

**L'interfaccia IDeliveryOptimizationFile** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationFile** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDeliveryOptimizationFile** include questi metodi.



| Metodo                                                 | Descrizione                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**GetStats**](ideliveryoptimizationfile-getstats.md) | Restituisce le statistiche di download e caricamento per un file specifico.<br/> |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato      | Windows 10, solo app desktop versione 1709 \[\]                                   |
| Server minimo supportato      | Windows Server, solo app desktop versione 1709 \[\]                               |
| Intestazione                        | Deliveryoptimization.h                                                           |
| Idl                           | DeliveryOptimization.idl                                                         |
| Libreria                       | Dosvc.lib                                                                        |
| DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile è definito come B76B9699-E99E-4101-803F-A20E325D93E2 |
