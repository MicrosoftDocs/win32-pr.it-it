---
title: Metodo SetConfig INapComponentConfig (NapCommon.h)
description: Imposta la configurazione del componente di convalida dell'integrità del sistema.
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Metodo SetConfig nap
- Metodo SetConfig NAP, interfaccia INapComponentConfig
- Interfaccia INapComponentConfig NAP, metodo SetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b3ecf455c591985a5e8778e49495351bd1b4aba83e9d29fe2b25d7d406a507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940199"
---
# <a name="inapcomponentconfigsetconfig-method"></a>Metodo INapComponentConfig::SetConfig

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo SetConfig** imposta la configurazione del componente shv (System Health Validator).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bCount* \[ Pollici\]
</dt> <dd>

Dimensioni, in byte, del BLOB *di configurazione* dei dati.

</dd> <dt>

*dati* \[ Pollici\]
</dt> <dd>

Puntatore ai dati di configurazione del componente SHV.

> [!Note]  
> I dati di configurazione esportati da un computer x86 usando il [**metodo GetConfig**](inapcomponentconfig-getconfig.md) possono essere importati in un computer x64 usando il **metodo SetConfig** e viceversa. Pertanto, i dati di configurazione devono essere in un formato indipendente dall'architettura, ad esempio XML. L'uso di XML anziché di un flusso di byte semplifica l'uso dei dati di configurazione in architetture diverse. Gli elementi XML usati nei dati di configurazione sono determinati dall'implementatore.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei codici di errore seguenti in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Le informazioni sul controllo delle versioni dei componenti devono essere incluse nel BLOB *di configurazione* dei dati. Le informazioni sul controllo delle versioni possono essere usate durante la migrazione da una versione SHV a un'altra.

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

[**INapConponentConfig::GetConfig**](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





