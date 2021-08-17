---
title: Metodo INapComponentConfig3 GetConfigFromID (NapCommon.h)
description: Viene implementato dai validator di integrità del sistema per fornire un modo per ottenere i dati di configurazione per un ID di configurazione specifico.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Metodo GetConfigFromID nap
- Metodo GetConfigFromID NAP , interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP, metodo GetConfigFromID
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 638704b5706b68b67f854a6a52b6c845be3fb757b596e9f5425f315c7d679fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368388"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a>Metodo INapComponentConfig3::GetConfigFromID

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo GetConfigFromID** viene implementato dai validator dell'integrità del sistema per fornire un modo per ottenere i dati di configurazione per un ID di configurazione specifico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*configID* \[ Pollici\]
</dt> <dd>

Valore che rappresenta la configurazione. Se *ConfigID* è **0,** shv deve restituire i dati di configurazione predefiniti in *outdata*.

</dd> <dt>

*count* \[ Cambio\]
</dt> <dd>

Dimensioni, in byte, dei dati di configurazione restituiti in *outdata.*

</dd> <dt>

*outdata* \[ Cambio\]
</dt> <dd>

In caso di restituzione, matrice BYTE contenente i dati di configurazione rappresentati da *ConfigID.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei codici di errore seguenti in base al risultato di questa operazione.



| Codice restituito                                                                                                    | Descrizione                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | L'operazione è riuscita.<br/> |
| <dl> <dt>**CONFIGURAZIONE \_ DI PROTEZIONE ACCESSO ALLA RETE E \_ \_ SHV NON \_ \_ TROVATA**</dt> </dl> | *Impossibile trovare ConfigID.*<br/>  |



 

## <a name="remarks"></a>Commenti

Per poter chiamare questo metodo, è necessario usare il metodo [**NewConfig**](inapcomponentconfig3-newconfig.md) per allocare i dati di configurazione per *ConfigID.*

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

 

 





