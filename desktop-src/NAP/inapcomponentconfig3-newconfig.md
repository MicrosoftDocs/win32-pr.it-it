---
title: Metodo INapComponentConfig3 NewConfig (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per fornire un modo per creare i dati di configurazione per un ID configurazione specifico.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- NAP metodo NewConfig
- Metodo NewConfig NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP, metodo NewConfig
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
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119403"
---
# <a name="inapcomponentconfig3newconfig-method"></a>Metodo INapComponentConfig3:: NewConfig

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **NewConfig** viene implementato da convalida integrità sistema (SHV) per fornire un modo per creare i dati di configurazione per un ID configurazione specifico. Quando questa funzione viene chiamata, un servizio di convalida dell'integrità di sistema deve allocare nuovi dati di configurazione e popolarli con una copia dei dati di configurazione predefiniti.

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

Valore che rappresenta la configurazione. *ConfigID* viene assegnato dal servizio Server dei criteri di rete ed è univoco all'interno del servizio di convalida dell'integrità di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                                 | Descrizione                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | L'operazione è riuscita.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                | *ConfigID* è 0 (un valore riservato per la configurazione predefinita).<br/>                  |
| <dl> <dt>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ esistente**</dt> </dl> | *ConfigID* esiste già. L'elenco di ID noto a server dei criteri di servizio è diverso da quello di convalida integrità di sistema.<br/> |



 

## <a name="remarks"></a>Commenti

Dopo la creazione della nuova configurazione da parte di **NewConfig**, è consigliabile usare i metodi [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)e [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) per modificare la configurazione in base alle esigenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





