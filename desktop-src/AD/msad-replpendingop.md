---
title: Classe MSAD_ReplPendingOp
description: Rappresenta la \_ struttura op REPL di DS \_ , che descrive un'attività di replica attualmente in esecuzione o in attesa di esecuzione.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- Classe MSAD_ReplPendingOp Active Directory
- Classe MSAD_ReplPendingOp Active Directory, descritta
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400635"
---
# <a name="msad_replpendingop-class"></a>\_Classe MSAD ReplPendingOp

Rappresenta la [**struttura \_ \_ op REPL di DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) , che descrive un'attività di replica attualmente in esecuzione o in attesa di esecuzione. Questa struttura viene restituita dalla funzione [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a>Members

La **classe \_ ReplPendingOp di MSAD** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ReplPendingOp di MSAD** dispone di queste proprietà.

<dl> <dt>

**DsaAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene l'indirizzo di rete specifico del trasporto del server remoto associato a questa operazione. **Null** se non è presente alcun server remoto associato a questa operazione.

</dd> <dt>

**DsaDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il percorso X. 500 del DSA associato al server remoto che corrisponde a questa operazione. **Null** se nessun server remoto corrisponde a questa operazione.

</dd> <dt>

**DsaObjGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore dell'attributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) dell'oggetto DSA identificato dalla proprietà **DsaDN** .

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il percorso X. 500 del contesto dei nomi (NC) associato a questa operazione.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene l'attributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) del NC identificato dalla proprietà **NamingContextDN** .

</dd> <dt>

**OpStartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene l'ora in cui è stata avviata l'operazione. **Null** se l'operazione è ancora in coda.

</dd> <dt>

**Opzioni**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il set di flag che fornisce dati aggiuntivi sull'operazione. Il contenuto di questo membro è determinato dal valore della proprietà **optype** .

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**\_sincronizzazione del \_ \_ tipo op REPL DS \_**


</dt> <dd>

Contiene zero o una combinazione di uno o più valori di **DS \_ REPSYNC \_ \** _ come definito per il parametro _Options * in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**\_aggiunta del \_ \_ tipo op REPL DS \_**


</dt> <dd>

Contiene zero o una combinazione di uno o più valori di **DS \_ REPADD \_ \** _ come definito per il parametro _Options * in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**\_eliminazione del \_ \_ tipo op REPL DS \_**


</dt> <dd>

Contiene zero o una combinazione di uno o più valori di **DS \_ REPDEL \_ \** _ come definito per il parametro _Options * in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**\_ \_ \_ modifica tipo op REPL \_ di DS**


</dt> <dd>

Contiene zero o una combinazione di uno o più valori di **DS \_ REPMOD \_ \** _ come definito per il parametro _Options * in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**\_ \_ \_ refs aggiornamento del tipo \_ op \_ di DS repl**


</dt> <dd>

Contiene zero o una combinazione di uno o più valori di **DS \_ REPSUPD \_ \** _ come definito per il parametro _Options * in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).

</dd> </dl>

</dd> <dt>

**OpType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore del [**\_ \_ \_ tipo op REPL di DS**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) che indica il tipo di operazione rappresentata da questa classe.

</dd> <dt>

**PositionInQ**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene la posizione di questa operazione nella coda.

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene la priorità di questa operazione. Le attività con priorità più alta vengono eseguite per prime. La priorità viene calcolata dal server in base al tipo di operazione rappresentata da questa classe e ai parametri dell'operazione.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene l'ID dell'operazione, che è univoco per computer e per avvio.

</dd> <dt>

**TimeEnqueued**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene l'ora in cui l'operazione è stata aggiunta alla coda.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\MicrosoftActiveDirectory radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

