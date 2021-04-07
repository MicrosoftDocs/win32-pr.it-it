---
title: Metodo INapComponentConfig InvokeUI (NapCommon. h)
description: Avvia un'interfaccia utente personalizzata per un componente del servizio di convalida dell'integrità di sistema (convalida integrità sistema).
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- NAP metodo InvokeUI
- Metodo InvokeUI NAP, interfaccia INapComponentConfig
- Interfaccia INapComponentConfig NAP, metodo InvokeUI
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964016"
---
# <a name="inapcomponentconfiginvokeui-method"></a>Metodo INapComponentConfig:: InvokeUI

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **InvokeUI** avvia un'interfaccia utente personalizzata per un componente del servizio di convalida dell'integrità di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Handle per la finestra padre o proprietario. È necessario specificare un handle di finestra valido.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>       | Il servizio di convalida dell'integrità di sistema non supporta un'interfaccia utente personalizzata.<br/>               |



 

## <a name="remarks"></a>Commenti

Questa chiamata al metodo deve essere bloccata fino alla chiusura dell'interfaccia utente di convalida integrità di sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





