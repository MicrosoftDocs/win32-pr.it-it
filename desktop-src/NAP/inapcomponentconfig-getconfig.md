---
title: Metodo GetConfig INapComponentConfig (NapCommon.h)
description: Recupera la configurazione del componente shv (System Health Validator).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- Metodo GetConfig NAP
- Metodo GetConfig NAP, interfaccia INapComponentConfig
- Interfaccia INapComponentConfig NAP, metodo GetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dc5495df10e3a5ff3907941644c5558aea35d29b52c8773fb56314c4a8620c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134499"
---
# <a name="inapcomponentconfiggetconfig-method"></a>Metodo INapComponentConfig::GetConfig

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo GetConfig** recupera la configurazione del componente shv (System Health Validator).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bCount* \[ Cambio\]
</dt> <dd>

Dimensione, in byte, del BLOB *di configurazione* dei dati.

</dd> <dt>

*dati* \[ Cambio\]
</dt> <dd>

Puntatore all'indirizzo dei dati di configurazione del componente SHV.

> [!Note]  
> I dati di configurazione esportati da un computer x86 usando il metodo **GetConfig** possono essere importati in un computer x64 usando il metodo [**SetConfig**](inapcomponentconfig-setconfig.md) e viceversa. Pertanto, i dati di configurazione devono essere in un formato indipendente dall'architettura, ad esempio XML. L'uso di XML anziché di un flusso di byte semplifica l'uso dei dati di configurazione in architetture diverse. Gli elementi XML utilizzati nei dati di configurazione sono determinati dall'implementatore.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei codici di errore seguenti in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Il parametro di dati deve essere allocato dal chiamato (implementatore del componente) usando **CoTaskMemAlloc** e liberato dal chiamante usando **CoTaskMemFree.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





