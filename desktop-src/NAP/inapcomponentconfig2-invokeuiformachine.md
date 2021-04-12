---
title: Metodo INapComponentConfig2 InvokeUIForMachine (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) in base alle esigenze per gestire la configurazione remota direttamente nel computer specificato. Questo metodo avvia un'interfaccia utente di gestione della configurazione.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- NAP metodo InvokeUIForMachine
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
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119646"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a>Metodo INapComponentConfig2:: InvokeUIForMachine

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **InvokeUIForMachine** viene implementato da convalida integrità sistema (SHV) in base alle esigenze per gestire la configurazione remota direttamente nel computer specificato. Questo metodo avvia un'interfaccia utente di gestione della configurazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Handle per la finestra padre o proprietario. È necessario specificare un handle di finestra valido.

</dd> <dt>

*nomecomputer* \[ in\]
</dt> <dd>

Puntatore a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente il nome del computer del client di protezione accesso alla rete.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o uno dei codici di errore standard di Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





