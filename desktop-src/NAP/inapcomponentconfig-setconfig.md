---
title: Metodo Seconfig INapComponentConfig (NapCommon. h)
description: Imposta la configurazione del componente convalida integrità sistema (convalida integrità sistema).
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Metodo di configurazione NAP
- Metodo di configurazione NAP, interfaccia INapComponentConfig
- Interfaccia INapComponentConfig NAP, metodo Seconfig
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
ms.openlocfilehash: 7a1f3d557517ec27f9537a7cbcd46be9e2cd107e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519285"
---
# <a name="inapcomponentconfigsetconfig-method"></a>Metodo INapComponentConfig:: Seconfig

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **Seconfig** imposta la configurazione del componente convalida integrità sistema (convalida integrità sistema).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bCount* \[ in\]
</dt> <dd>

Dimensione, in byte, del BLOB di configurazione *dei dati* .

</dd> <dt>

*dati* \[ di in\]
</dt> <dd>

Puntatore ai dati di configurazione del componente di convalida integrità di sistema.

> [!Note]  
> I dati di configurazione esportati da un computer x86 usando il metodo [**GetConfig**](inapcomponentconfig-getconfig.md) possono essere importati in un computer x64 usando il metodo **Seconfig** e viceversa. Di conseguenza, i dati di configurazione devono essere in un formato indipendente dall'architettura, ad esempio XML. L'utilizzo di XML anziché di un flusso di byte rende più semplice l'utilizzo dei dati di configurazione in architetture diverse. Gli elementi XML utilizzati nei dati di configurazione sono determinati dall'implementatore.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Le informazioni sul controllo delle versioni dei componenti devono essere incluse nel BLOB di configurazione *dati* . Le informazioni sul controllo delle versioni possono essere utilizzate durante la migrazione da una versione di convalida integrità di sistema a un'altra.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapConponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





