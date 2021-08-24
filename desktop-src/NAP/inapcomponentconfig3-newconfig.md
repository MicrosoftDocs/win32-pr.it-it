---
title: Metodo INapComponentConfig3 NewConfig (NapCommon.h)
description: Viene implementato dai validator dell'integrità del sistema per fornire un modo per creare dati di configurazione per un ID di configurazione specifico.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Metodo NewConfig NAP
- Metodo NewConfig NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP , metodo NewConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff87f55218d8c84b1cb95a75e1801783e57b17288c36057323589ab44a47d3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891341"
---
# <a name="inapcomponentconfig3newconfig-method"></a>Metodo INapComponentConfig3::NewConfig

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo NewConfig** viene implementato dai validator dell'integrità del sistema per fornire un modo per creare dati di configurazione per un ID di configurazione specifico. Quando viene chiamata questa funzione, un'istanza shv deve allocare nuovi dati di configurazione e popolarlo con una copia dei dati di configurazione predefiniti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*configID* 
</dt> <dd>

Valore che rappresenta la configurazione. *ConfigID* viene assegnato dal servizio Server dei criteri di rete ed è univoco all'interno del server dei criteri di rete.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei codici di errore seguenti in base al risultato di questa operazione.



| Codice restituito                                                                                                 | Descrizione                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | L'operazione è riuscita.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                | *ConfigID* è 0 (un valore riservato per la configurazione predefinita).<br/>                  |
| <dl> <dt>**CONFIGURAZIONE \_ DI PROTEZIONE ACCESSO ALLA RETE E \_ \_ SHV \_ ESISTENTE**</dt> </dl> | *ConfigID* esiste già. L'elenco di ID noti al server dei criteri di rete è diverso da SHV.<br/> |



 

## <a name="remarks"></a>Commenti

Dopo aver creato la nuova configurazione da **NewConfig,** è necessario usare i metodi [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)e [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) per modificare la configurazione in base alle esigenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





