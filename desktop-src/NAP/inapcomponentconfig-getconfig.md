---
title: Metodo GetConfig INapComponentConfig (NapCommon. h)
description: Recupera la configurazione del componente convalida integrità sistema (convalida integrità sistema).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- Metodo GetConfig NAP
- Metodo GetConfig NAP, interfaccia INapComponentConfig
- Interfaccia NAP di INapComponentConfig, metodo GetConfig
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
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478443"
---
# <a name="inapcomponentconfiggetconfig-method"></a>Metodo INapComponentConfig:: GetConfig

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **GetConfig** recupera la configurazione del componente convalida integrità sistema (convalida integrità sistema).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bCount* \[ out\]
</dt> <dd>

Dimensione, in byte, del BLOB di configurazione *dei dati* .

</dd> <dt>

*dati* \[ di out\]
</dt> <dd>

Puntatore all'indirizzo dei dati di configurazione del componente di convalida integrità di sistema.

> [!Note]  
> I dati di configurazione esportati da un computer x86 usando il metodo **GetConfig** possono essere importati in un computer x64 usando il metodo [**Seconfig**](inapcomponentconfig-setconfig.md) e viceversa. Di conseguenza, i dati di configurazione devono essere in un formato indipendente dall'architettura, ad esempio XML. L'utilizzo di XML anziché di un flusso di byte rende più semplice l'utilizzo dei dati di configurazione in architetture diverse. Gli elementi XML utilizzati nei dati di configurazione sono determinati dall'implementatore.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Il parametro data deve essere allocato dal chiamato (implementatore del componente) utilizzando **CoTaskMemAlloc** e liberato dal chiamante utilizzando **CoTaskMemFree**.

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

[**INapComponentConfig:: Seconfig**](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





