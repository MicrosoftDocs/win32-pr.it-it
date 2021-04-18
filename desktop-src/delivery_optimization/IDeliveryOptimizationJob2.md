---
title: Interfaccia IDeliveryOptimizationJob2
description: 'Altre informazioni su: interfaccia IDeliveryOptimizationJob2'
keywords:
- Interfaccia IDeliveryOptimizationJob2
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305008"
---
# <a name="ideliveryoptimizationjob2-interface"></a>Interfaccia IDeliveryOptimizationJob2

IDeliveryOptimizationJob2 consente di aggiungere un singolo file al processo di download e di recuperare immediatamente il file. Questa interfaccia supporta anche l'impostazione e il recupero di proprietà facoltative del processo.

## <a name="members"></a>Membri

L'interfaccia **IDeliveryOptimizationJob2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationJob2** dispone anche di questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDeliveryOptimizationJob2** dispone di questi metodi.

| Metodo                                              | Descrizione                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [**AddFile**](ideliveryoptimizationjob2-addfile.md) | Il metodo AddFile aggiunge un singolo file a un processo DO esistente.         |
| [**GetProperty**](ideliveryoptimizationjob2-getproperty.md) | Il metodo AddFile aggiunge un singolo file a un processo DO esistente. |
| [**SetProperty**](ideliveryoptimizationjob2-setproperty.md) | Questo metodo non è utilizzato.                                       |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato | Solo app desktop Windows 10 versione 1803 \[\]                                   |
| Server minimo supportato | Windows Server, versione 1709 \[ solo per le app desktop\]                               |
| Intestazione                   | Deliveryoptimization. h                                                           |
| IDL                      | DeliveryOptimization. idl                                                         |
| Libreria                  | Dosvc. lib                                                                        |
| DLL                      | Dosvc.dll                                                                        |
| IID                      | IID_IDeliveryOptimizationJob2 viene definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |
