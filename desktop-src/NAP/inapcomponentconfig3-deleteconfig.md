---
title: Metodo INapComponentConfig3 DeleteConfig (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per fornire un modo per eliminare i dati di configurazione per un ID configurazione specifico.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- NAP metodo DeleteConfig
- Metodo DeleteConfig NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP, metodo DeleteConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740946"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a>INapComponentConfig3::D Metodo eleteConfig

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **DeleteConfig** viene implementato da convalida integrità sistema (SHV) per fornire un modo per eliminare i dati di configurazione per un ID configurazione specifico. È possibile riutilizzare l'ID dopo l'eliminazione dei dati di configurazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*configID* 
</dt> <dd>

Valore che rappresenta i dati di configurazione da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                                    | Descrizione                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | L'operazione è riuscita.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                   | *ConfigID* è 0 (un valore riservato per la configurazione predefinita).<br/> |
| <dl> <dt>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ non \_ trovata**</dt> </dl> | *ConfigID* non è stato trovato.<br/>                                       |



 

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

 

 





