---
title: Metodo ExecuteKCC della classe MSAD_DomainController
description: Chiama la funzione DsReplicaConsistencyCheck, che richiama il controllo di coerenza delle informazioni (KCC, Knowledge Consistency Checker) per verificare la topologia di replica.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Metodo ExecuteKCC Active Directory
- Metodo ExecuteKCC Active Directory , MSAD_DomainController classe
- MSAD_DomainController classe Active Directory , metodo ExecuteKCC
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
ms.openlocfilehash: 48295638f105b79ea24a55965ca3ec75ee0ad6b9982c74664f8bfecdd0681cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189619"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>Metodo ExecuteKCC della classe MsAD \_ DomainController

Chiama la [**funzione DsReplicaConsistencyCheck,**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) che richiama il controllo di coerenza delle informazioni (KCC, Knowledge Consistency Checker) per verificare la topologia di replica.

## <a name="syntax"></a>Sintassi


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TaskID* \[ Pollici\]
</dt> <dd>

Attività che deve essere eseguita da KCC. **Servizi di dominio \_ KCC \_ TASKID \_ UPDATE \_ TOPOLOGY** è l'unico valore attualmente supportato.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Set di flag che modificano il comportamento **del metodo ExecuteKCC.** Questo parametro può essere zero o una combinazione di uno o più dei valori seguenti.

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS \_ KCC \_ FLAG \_ ASYNC \_ OP**


</dt> <dd>

L'attività viene accodata e quindi la funzione viene restituita senza attendere il completamento dell'attività.

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS \_ KCC \_ FLAG \_ DAMPED**


</dt> <dd>

L'attività non verrà aggiunta alla coda se un'altra attività in coda verrà eseguita a breve.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSAD \_ DomainController**](msad-domaincontroller.md)
</dt> </dl>

 

 





