---
title: Metodo INapComponentConfig IsUISupported (NapCommon. h)
description: Specifica se il componente supporta un'interfaccia utente personalizzata.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- NAP metodo IsUISupported
- Metodo IsUISupported NAP, interfaccia INapComponentConfig
- Interfaccia INapComponentConfig NAP, metodo IsUISupported
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301582"
---
# <a name="inapcomponentconfigisuisupported-method"></a>Metodo INapComponentConfig:: IsUISupported

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **IsUISupported** specifica se il componente supporta un'interfaccia utente personalizzata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*supportato* \[ out\]
</dt> <dd>

Puntatore a un BOOL che è impostato su **true** se il componente supporta un'interfaccia utente personalizzata e **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

L'interfaccia utente personalizzata di un componente deve essere avviata con [**INapComponentConfig:: InvokeUI**](inapcomponentconfig-invokeui.md).

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

[**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





