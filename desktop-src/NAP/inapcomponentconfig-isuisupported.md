---
title: Metodo INapComponentConfig IsUISupported (NapCommon.h)
description: Specifica se il componente supporta un'interfaccia utente personalizzata.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Metodo IsUISupported nap
- Metodo IsUISupported NAP , interfaccia INapComponentConfig
- Interfaccia INapComponentConfig NAP , metodo IsUISupported
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
ms.openlocfilehash: 5e343b037e4f77b4c1e342ffa78278854b11d714e09e9e57188d83fc9f93a180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134489"
---
# <a name="inapcomponentconfigisuisupported-method"></a>Metodo INapComponentConfig::IsUISupported

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo IsUISupported** specifica se il componente supporta un'interfaccia utente personalizzata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isSupported* \[ Cambio\]
</dt> <dd>

Puntatore a un oggetto BOOL impostato su **TRUE se** il componente supporta un'interfaccia utente personalizzata e FALSE in caso **contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei codici di errore seguenti in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

L'interfaccia utente personalizzata di un componente deve essere avviata usando [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





