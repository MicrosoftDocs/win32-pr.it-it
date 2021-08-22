---
description: Posiziona il servizio nello stato avviato.
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: Metodo StartService della classe CIM_Service (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c0e30adbece838cb913f215abedc4aa86a2762d00f046a54bf2717eaeecdb56e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561811"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a>Metodo StartService della classe CIM_Service (gestione Hyper-V)

Posiziona il servizio nello stato avviato.

> [!Note]
>
> La semantica di questo metodo si sovrappone al **metodo RequestStateChange** ereditato da [**CIM \_ EnabledLogicalElement.**](cim-enabledlogicalelement.md) Questo metodo viene mantenuto perché è stato ampiamente implementato e la semantica di avvio semplice è comoda da usare.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.

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

 

 




