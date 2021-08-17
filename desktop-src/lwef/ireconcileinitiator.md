---
title: Interfaccia IReconcileInitiator
description: Espone metodi che forniscono al riconciliatore di valigetta i mezzi per notificare all'iniziatore lo stato di avanzamento, per impostare un oggetto di terminazione e per richiedere una determinata versione di un documento. L'iniziatore è responsabile dell'implementazione di questa interfaccia.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Interfaccia IReconcileInitiator Funzionalità dell'ambiente Windows legacy
- Interfaccia IReconcileInitiator Legacy Windows Environment Features , descritta
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff81862e5ff0b27b75f952749957e6559306257240f2a02aca5f34e3efc870cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749141"
---
# <a name="ireconcileinitiator-interface"></a>Interfaccia IReconcileInitiator

Espone metodi che forniscono al riconciliatore di valigetta i mezzi per notificare all'iniziatore lo stato di avanzamento, per impostare un oggetto di terminazione e per richiedere una determinata versione di un documento. L'iniziatore è responsabile dell'implementazione di questa interfaccia.

## <a name="members"></a>Membri

**L'interfaccia IReconcileInitiator** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IReconcileInitiator** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IReconcileInitiator** include questi metodi.



| Metodo                                                                 | Descrizione                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | Imposta l'oggetto tramite il quale l'iniziatore può terminare in modo asincrono una riconciliazione. Un riconciliatore di valigetta imposta in genere questo oggetto per le riconciliazioni lunghe o che coinvolgono l'interazione dell'utente. <br/>                                                                                              |
| [**SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | Indica la quantità di avanzamento che il riconciliatore di valige ha effettuato per completare la riconciliazione. La quantità è una frazione e viene calcolata come quoziente dei parametri *ulProgress* e *ulProgressMax.* I riconciliatori devono chiamare questo metodo periodicamente durante il processo di riconciliazione. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                   |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.0 o successiva)</dt> </dl> |



 

