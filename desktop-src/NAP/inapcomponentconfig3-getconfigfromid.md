---
title: Metodo INapComponentConfig3 GetConfigFromID (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per fornire un modo per ottenere i dati di configurazione per un ID configurazione specifico.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- NAP metodo GetConfigFromID
- Metodo GetConfigFromID NAP, interfaccia INapComponentConfig3
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
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740938"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a>Metodo INapComponentConfig3:: GetConfigFromID

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **GetConfigFromID** viene implementato da convalida integrità sistema (SHV) per fornire un modo per ottenere i dati di configurazione per un ID configurazione specifico.

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

*configID* \[ in\]
</dt> <dd>

Valore che rappresenta la configurazione. Se *ConfigID* è **0**, il servizio di convalida dell'integrità di sistema deve restituire i dati di configurazione predefiniti in *OutData*.

</dd> <dt>

*numero* \[ di out\]
</dt> <dd>

Dimensione, in byte, dei dati di configurazione restituiti in *OutData*.

</dd> <dt>

*dati OutData* \[ out\]
</dt> <dd>

Al ritorno, matrice di BYTE che contiene i dati di configurazione rappresentati da *ConfigID*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                                    | Descrizione                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | L'operazione è riuscita.<br/> |
| <dl> <dt>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ non \_ trovata**</dt> </dl> | *ConfigID* non è stato trovato.<br/>  |



 

## <a name="remarks"></a>Commenti

Il metodo [**NewConfig**](inapcomponentconfig3-newconfig.md) deve essere usato per allocare i dati di configurazione per *ConfigID* prima di poter chiamare questo metodo.

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

 

 





