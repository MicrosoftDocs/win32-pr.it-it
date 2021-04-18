---
title: Metodo INapComponentConfig3 SetConfigToID (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per fornire un modo per impostare i dati di configurazione per un ID configurazione specifico.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- NAP metodo SetConfigToID
- Metodo SetConfigToID NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP, metodo SetConfigToID
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302719"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a>Metodo INapComponentConfig3:: SetConfigToID

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **SetConfigToID** viene implementato da convalida integrità sistema (SHV) per fornire un modo per impostare i dati di configurazione per un ID configurazione specifico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*configID* \[ in\]
</dt> <dd>

Valore che rappresenta la configurazione. *ConfigID* viene assegnato dal servizio Server dei criteri di rete ed è univoco all'interno del servizio di convalida dell'integrità di sistema. Se *ConfigID* è 0, viene impostata la configurazione predefinita del servizio di convalida dell'integrità di sistema.

</dd> <dt>

*numero* \[ di in\]
</dt> <dd>

Dimensione, in byte, dei dati di configurazione nei *dati*.

</dd> <dt>

*dati* \[ di in\]
</dt> <dd>

In input, matrice di BYTE che contiene i dati di configurazione impostati su *ConfigID*.

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

 

 





