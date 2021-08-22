---
title: Metodo InvokeUIForMachine INapComponentConfig2 (NapCommon.h)
description: Viene implementato dai validator di integrità del sistema in base alle esigenze per gestire la configurazione remota direttamente nel computer specificato. Questo metodo avvia un'interfaccia utente di gestione della configurazione.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Metodo InvokeUIForMachine NAP
- Metodo InvokeUIForMachine NAP, interfaccia INapComponentConfig2
- Interfaccia INapComponentConfig2 NAP, metodo InvokeUIForMachine
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8321425cf878bd9b3d8702f73fa464ae069420cd0e59f57e2500151fda01b191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940189"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a>Metodo INapComponentConfig2::InvokeUIForMachine

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo InvokeUIForMachine** viene implementato dai validator di integrità del sistema (SHV) in base alle esigenze per gestire la configurazione remota direttamente nel computer specificato. Questo metodo avvia un'interfaccia utente di gestione della configurazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ Pollici\]
</dt> <dd>

Handle per la finestra padre o proprietaria. È necessario specificare un handle di finestra valido.

</dd> <dt>

*machineName* \[ Pollici\]
</dt> <dd>

Puntatore a un [**oggetto CountedString che**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contiene il nome del computer del client di Protezione accesso alla rete.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo o uno dei codici di Windows standard.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





