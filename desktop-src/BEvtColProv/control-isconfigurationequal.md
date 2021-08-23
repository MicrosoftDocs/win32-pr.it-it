---
description: Confrontare l'argomento con la configurazione attiva dell'agente di raccolta.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Metodo IsConfigurationEqual della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 6facd4f885eb1eb992f95bf4432e32704f7472d8125cb1022f7a6baf5cf591d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579671"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a>Metodo IsConfigurationEqual della classe Control

Confrontare l'argomento con la configurazione attiva dell'agente di raccolta.

## <a name="syntax"></a>Sintassi


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Configurazione* \[ Pollici\]
</dt> <dd>

Configurazione da confrontare con la configurazione attiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

<dl> <dt>


</dt> <dd>

0

Errore

</dd> <dt>


</dt> <dd>

1

Operazione completata

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Radice \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




