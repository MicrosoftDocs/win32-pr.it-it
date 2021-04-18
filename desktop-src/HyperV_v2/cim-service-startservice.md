---
description: Inserisce il servizio nello stato avviato.
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: Metodo StartService della classe CIM_Service (gestione di Hyper-V)
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
ms.openlocfilehash: 73b89f7fc789639fb45acbde61da4c7962650177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307767"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a>Metodo StartService della classe CIM_Service (gestione di Hyper-V)

Inserisce il servizio nello stato avviato.

> [!Note]
>
> La semantica di questo metodo si sovrappone al metodo **RequestStateChange** ereditato da [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md). Questo metodo viene mantenuto perché è stato ampiamente implementato e la semplice semantica di "avvio" è comoda da usare.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio CIM**](cim-service.md)
</dt> </dl>

 

 




