---
title: Interfaccia IReconcileInitiator
description: Espone i metodi che forniscono il riconciliatore della valigetta con i mezzi per notificare all'iniziatore lo stato di avanzamento, per impostare un oggetto di terminazione e per richiedere una versione specifica di un documento. L'Initiator è responsabile dell'implementazione di questa interfaccia.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IReconcileInitiator
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IReconcileInitiator, descritte
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
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741599"
---
# <a name="ireconcileinitiator-interface"></a>Interfaccia IReconcileInitiator

Espone i metodi che forniscono il riconciliatore della valigetta con i mezzi per notificare all'iniziatore lo stato di avanzamento, per impostare un oggetto di terminazione e per richiedere una versione specifica di un documento. L'Initiator è responsabile dell'implementazione di questa interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IReconcileInitiator** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IReconcileInitiator** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IReconcileInitiator** dispone di questi metodi.



| Metodo                                                                 | Descrizione                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | Imposta l'oggetto tramite il quale l'iniziatore può terminare in modo asincrono una riconciliazione. Un riconciliatore di valigetta imposta in genere questo oggetto per le riconciliazioni che sono lunghe o coinvolgono l'interazione dell'utente. <br/>                                                                                              |
| [**SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | Indica la quantità di avanzamento apportata dal riconciliatore della valigetta verso il completamento della riconciliazione. La quantità è una frazione e viene calcolata come quoziente dei parametri *ulProgress* e *ulProgressMax* . I riconciliatori devono chiamare questo metodo periodicamente durante il processo di riconciliazione. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                   |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,0 o successiva)</dt> </dl> |



 

