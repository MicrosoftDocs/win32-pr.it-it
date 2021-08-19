---
title: Metodo INapComponentConfig3 SetConfigToID (NapCommon.h)
description: Viene implementato dai validator di integrità del sistema per fornire un modo per impostare i dati di configurazione per un ID di configurazione specifico.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Metodo SetConfigToID Nap
- Metodo SetConfigToID NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 Nap, metodo SetConfigToID
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
ms.openlocfilehash: 010fdc6cbb236a113e4f1804d3a4780c0e6a72f89b1f03bf90f1d99a92dc2bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781081"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a>Metodo INapComponentConfig3::SetConfigToID

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo SetConfigToID** viene implementato dai validator di integrità del sistema per fornire un modo per impostare i dati di configurazione per un ID di configurazione specifico.

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

*configID* \[ Pollici\]
</dt> <dd>

Valore che rappresenta la configurazione. *ConfigID* viene assegnato dal servizio Server dei criteri di rete ed è univoco all'interno della shv. Se *ConfigID* è 0, viene impostata la configurazione predefinita di SHV.

</dd> <dt>

*count* \[ Pollici\]
</dt> <dd>

Dimensioni, in byte, dei dati di configurazione nei *dati*.

</dd> <dt>

*dati* \[ Pollici\]
</dt> <dd>

Nell'input, matrice BYTE che contiene il set di dati di configurazione su *ConfigID*.

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

 

 





