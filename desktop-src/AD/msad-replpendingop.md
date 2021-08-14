---
title: MSAD_ReplPendingOp classe
description: Rappresenta la struttura DS REPL OP, che descrive un'attività di replica attualmente in esecuzione \_ \_ o in sospeso.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- MSAD_ReplPendingOp classe Active Directory
- MSAD_ReplPendingOp classe Active Directory , descritto
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
ms.openlocfilehash: 164c5ebe672a52bb399727940e5e51b98904f7db322cc362425dabda25f547a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186076"
---
# <a name="msad_replpendingop-class"></a>Classe \_ MSAD ReplPendingOp

Rappresenta la [**struttura DS \_ REPL \_ OP,**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) che descrive un'attività di replica attualmente in esecuzione o in sospeso. Questa struttura viene restituita [**dalla funzione DsReplicaGetInfo.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)

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

La **classe MSAD \_ ReplPendingOp** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MSAD \_ ReplPendingOp** ha queste proprietà.

<dl> <dt>

**DsaAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene l'indirizzo di rete specifico del trasporto del server remoto associato a questa operazione. **NULL** se non è presente alcun server remoto associato a questa operazione.

</dd> <dt>

**DsaDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il percorso X.500 dell'oggetto DSA associato al server remoto che corrisponde a questa operazione. **NULL** se nessun server remoto corrisponde a questa operazione.

</dd> <dt>

**DsaObjGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore [**dell'attributo objectGuid**](/windows/desktop/ADSchema/a-objectguid) dell'oggetto DSA identificato dalla **proprietà DsaDN.**

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il percorso X.500 del contesto dei nomi (NC) associato a questa operazione.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene [**l'attributo objectGuid**](/windows/desktop/ADSchema/a-objectguid) del NC identificato dalla **proprietà NamingContextDN.**

</dd> <dt>

**OpStartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene l'ora di avvio dell'operazione. **NULL** se questa operazione è ancora presente nella coda.

</dd> <dt>

**Opzioni**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il set di flag che fornisce dati aggiuntivi sull'operazione. Il contenuto di questo membro è determinato dal valore della **proprietà OpType.**

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS \_ REPL \_ OP \_ TYPE \_ SYNC**


</dt> <dd>

Contiene zero o una combinazione di uno o più valori **DS \_ \_ \* REPSYNC* _ definiti per il parametro _Options* in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS \_ REPL \_ OP \_ TYPE \_ ADD**


</dt> <dd>

Contiene zero o una combinazione di uno o più valori **DS \_ \_ \* REPADD* _ definiti per il parametro _Options* in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS \_ REPL \_ OP \_ TYPE \_ DELETE**


</dt> <dd>

Contiene zero o una combinazione di uno o più valori **DS \_ \_ \* REPDEL* _ definiti per il parametro _Options* in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS \_ REPL \_ OP \_ TYPE \_ MODIFY**


</dt> <dd>

Contiene zero o una combinazione di uno o più valori **DS \_ REPMOD \_ \** _ definiti per il parametro _Options* in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS \_ REPL \_ OP \_ TYPE \_ UPDATE \_ REFS**


</dt> <dd>

Contiene zero o una combinazione di uno o più valori **DS \_ \_ \* REPSUPD* _ definiti per il parametro _Options* in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).

</dd> </dl>

</dd> <dt>

**OpType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il [**valore DS \_ REPL \_ OP \_ TYPE**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) che indica il tipo di operazione rappresentato da questa classe.

</dd> <dt>

**PositionInQ**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene la posizione di questa operazione nella coda.

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene la priorità di questa operazione. Le attività con priorità più alta vengono eseguite per prime. La priorità viene calcolata dal server in base al tipo di operazione rappresentato da questa classe e ai parametri dell'operazione.

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene l'ID dell'operazione, univoco per computer e per avvio.

</dd> <dt>

**TimeEnqueued**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene l'ora in cui questa operazione è stata aggiunta alla coda.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

