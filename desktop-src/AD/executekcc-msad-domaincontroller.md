---
title: Metodo ExecuteKCC della classe MSAD_DomainController
description: Chiama la funzione DsReplicaConsistencyCheck, che richiama il controllo di coerenza informazioni (KCC) per verificare la topologia di replica.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Active Directory del metodo ExecuteKCC
- Metodo ExecuteKCC Active Directory, classe MSAD_DomainController
- Classe MSAD_DomainController Active Directory, metodo ExecuteKCC
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301944"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>Metodo ExecuteKCC della \_ classe DomainController MSAD

Chiama la funzione [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) , che richiama il controllo di coerenza informazioni (KCC) per verificare la topologia di replica.

## <a name="syntax"></a>Sintassi


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TaskId* \[ in\]
</dt> <dd>

Attività che deve essere eseguita dal KCC. Servizi di **dominio Active Directory \_ La \_ \_ \_ topologia di aggiornamento taskId di KCC** è l'unico valore attualmente supportato.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Set di flag che modificano il comportamento del metodo **ExecuteKCC** . Questo parametro può essere zero o una combinazione di uno o più dei valori seguenti.

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS \_ KCC \_ flag \_ Async \_ op**


</dt> <dd>

L'attività viene accodata, quindi la funzione restituisce senza attendere il completamento dell'attività.

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**\_flag KCC \_ DS \_ smorzato**


</dt> <dd>

L'attività non verrà aggiunta alla coda se un'altra attività accodata verrà eseguita a breve.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\MicrosoftActiveDirectory radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSAD \_ DomainController**](msad-domaincontroller.md)
</dt> </dl>

 

 





