---
description: Paces the service in the stopped state.
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: Metodo StopService della classe CIM_Service (gestione di Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b36cab1054e99ac306fb1b21fe9f08e0820974a0883e90655a180b07035b7f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647584"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a>Metodo StopService della classe CIM_Service (gestione di Hyper-V)

Paces the service in the stopped state.

> [!Note]
>
> La semantica di questo metodo si sovrappone al **metodo RequestStateChange** ereditato da [**CIM \_ EnabledLogicalElement.**](cim-enabledlogicalelement.md) Questo metodo viene mantenuto perché è stato ampiamente implementato e la semplice semantica di arresto è comoda da usare.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Servizio \_ CIM**](cim-service.md)
</dt> </dl>

 

 




