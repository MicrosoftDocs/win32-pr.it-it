---
title: Identificatori dei diritti di accesso (Fwpmu.h)
description: Windows Filtering Platform (WFP) usa i diritti di accesso Win32 standard più un set di diritti di accesso specifici del WFP incorporati nella piattaforma di filtro.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6deee82b792f525814ac4c841da8a848e4f7b978720755c82f93a9569ba21ca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951379"
---
# <a name="access-right-identifiers"></a>Identificatori dei diritti di accesso

Windows Filtering Platform (WFP) usa i diritti di accesso [Win32 standard](/windows/desktop/SecAuthZ/standard-access-rights) e un set di diritti di accesso specifici del WFP incorporati nella piattaforma di filtro. Questi diritti di accesso vengono usati solo per proteggere gli oggetti in modalità utente. I chiamanti in modalità kernel ignorano tutti i controlli di accesso.

Gli identificatori dei diritti di accesso specifici del WFP sono i seguenti.

<dl> <dt>

<span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ ADD**
</dt> <dd> <dl> <dt>



Aggiungere un oggetto alla Base Filtering Engine (BFE). Questo diritto di accesso è necessario per chiamare funzioni [**Fwpm \* Add0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM ACTRL ADD LINK (AGGIUNGI COLLEGAMENTO FWPM \_ \_ \_ ACTRL)**
</dt> <dd> <dl> <dt>



Aggiungere un oggetto a cui viene fatto riferimento tramite un collegamento. Ad esempio, questo diritto di accesso è necessario per i callout a cui si fa riferimento tramite GUID.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN**
</dt> <dd> <dl> <dt>



Avviare una transazione di sola lettura. Questo diritto di accesso è necessario per chiamare [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN**
</dt> <dd> <dl> <dt>



Avviare una transazione di lettura/scrittura. Questo diritto di accesso è necessario per chiamare [**FwpmTransactionBegin0 per**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) una transazione di lettura/scrittura.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ CLASSIFY**
</dt> <dd> <dl> <dt>



Classificare rpc (Remote Procedure Call). Questo diritto di accesso è necessario per il run-time RPC per applicare filtri RPC.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**Enumerazione \_ ACTRL FWPM \_**
</dt> <dd> <dl> <dt>



Enumerare. Questo diritto di accesso è necessario per chiamare le [**funzioni \* CreateEnumHandle0 di Fwpm.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) Per enumerare un oggetto, il chiamante richiede anche l'accesso FWPM \_ ACTRL \_ READ all'oggetto.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ OPEN**
</dt> <dd> <dl> <dt>



Aprire una sessione nel motore di filtro. Questo diritto di accesso è necessario per chiamare [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ READ**
</dt> <dd> <dl> <dt>



Lettura. Questo diritto di accesso è necessario per chiamare le [**funzioni \* Fwpm GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) e [**Fwpm \* GetByKey0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0)


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**STATISTICHE DI LETTURA \_ FWPM ACTRL \_ \_**
</dt> <dd> <dl> <dt>



Leggere le statistiche. Questo diritto di accesso è necessario per chiamare [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) e [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ SUBSCRIBE**
</dt> <dd> <dl> <dt>



Eseguire la sottoscrizione. Questo diritto di accesso è necessario per chiamare le [**funzioni Fwpm \* SubscribeChanges0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) Per ricevere una notifica per un oggetto, un sottoscrittore richiede anche l'accesso FWPM \_ ACTRL \_ READ all'oggetto.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ WRITE**
</dt> <dd> <dl> <dt>



Opzioni del motore di scrittura. Questo diritto di accesso è necessario per chiamare [**FwpmEngineSetOption0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM \_ GENERIC \_ READ**
</dt> <dd> <dl> <dt>



DIRITTI STANDARD \_ \_ LETTURA \| FWPM \_ ACTRL BEGIN READ \_ \_ \_ TXN \| FWPM \_ ACTRL \_ CLASSIFY \| FWPM \_ ACTRL OPEN \_ \| FWPM \_ ACTRL READ \_ \| FWPM ACTRL READ FWPM \_ ACTRL READ \_ \_ STATS


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**ESECUZIONE GENERICA FWPM \_ \_**
</dt> <dd> <dl> <dt>



STANDARD \_ RIGHTS \_ EXECUTE \| FWPM \_ ACTRL \_ ENUM \| FWPM \_ ACTRL \_ SUBSCRIBE


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**SCRITTURA GENERICA FWPM \_ \_**
</dt> <dd> <dl> <dt>



DIRITTI STANDARD \_ \_ WRITE DELETE \| \| FWPM \_ ACTRL ADD \_ \| FWPM \_ ACTRL ADD LINK \_ \_ \| FWPM \_ ACTRL BEGIN WRITE \_ \_ \_ TXN \| FWPM \_ ACTRL \_ WRITE


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ GENERIC \_ ALL**
</dt> <dd> <dl> <dt>



DIRITTI STANDARD RICHIESTI \_ \_ \| FWPM \_ ACTRL \_ ADD \| FWPM \_ ACTRL \_ ADD LINK \_ \| FWPM \_ ACTRL BEGIN READ \_ \_ \_ TXN \| FWPM \_ ACTRL BEGIN WRITE \_ \_ \_ TXN \| FWPM \_ ACTRL \_ CLASSIFY \| FWPM \_ ACTRL \_ ENUM \| FWPM \_ ACTRL OPEN \_ \| FWPM \_ ACTRL READ \_ \| FWPM \_ ACTRL READ \_ \_ STATS \| FWPM \_ ACTRL SUBSCRIBE \_ \| FWPM \_ ACTRL \_ WRITE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Filtro del modello di controllo di accesso della piattaforma](access-control.md)
</dt> <dt>

[Diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

