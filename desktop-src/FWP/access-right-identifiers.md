---
title: Identificatori Right di accesso (Fwpmu. h)
description: Windows Filtering Platform (WFP) utilizza i diritti di accesso Win32 standard e un set di diritti di accesso specifici di WFP incorporati nella piattaforma di filtro.
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
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964891"
---
# <a name="access-right-identifiers"></a>Identificatori Right di accesso

Windows Filtering Platform (WFP) utilizza i [diritti di accesso Win32 standard](/windows/desktop/SecAuthZ/standard-access-rights) e un set di diritti di accesso specifici di WFP incorporati nella piattaforma di filtro. Questi diritti di accesso vengono usati per proteggere gli oggetti solo in modalità utente. I chiamanti in modalità kernel ignorano tutti i controlli di accesso.

Gli identificatori corretti di accesso specifici di WFP sono i seguenti.

<dl> <dt>

<span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**\_aggiunta FWPM ACTRL \_**
</dt> <dd> <dl> <dt>



Aggiungere un oggetto al motore di filtro di base (BFE). Questo diritto di accesso è necessario per chiamare le [**funzioni \* Add0 di Fwpm**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) .


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Aggiungi \_ collegamento**
</dt> <dd> <dl> <dt>



Aggiungere un oggetto a cui si fa riferimento tramite un collegamento. Ad esempio, questo diritto di accesso è necessario per i callout a cui viene fatto riferimento tramite GUID.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ transazione**
</dt> <dd> <dl> <dt>



Inizia una transazione di sola lettura. Questo diritto di accesso è necessario per chiamare [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ transazione**
</dt> <dd> <dl> <dt>



Inizia una transazione di lettura/scrittura. Questo diritto di accesso è necessario per chiamare [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) per una transazione di lettura/scrittura.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_classificazione FWPM ACTRL \_**
</dt> <dd> <dl> <dt>



Classificazione RPC (Remote Procedure Call). Questo diritto di accesso è necessario per la fase di esecuzione RPC per applicare i filtri RPC.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**\_enumerazione FWPM ACTRL \_**
</dt> <dd> <dl> <dt>



Enumerare. Questo diritto di accesso è necessario per chiamare le [**funzioni \* CreateEnumHandle0 di Fwpm**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) . Per enumerare un oggetto, il chiamante deve anche \_ \_ avere l'accesso in lettura ACTRL FWPM all'oggetto.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ aperto**
</dt> <dd> <dl> <dt>



Aprire una sessione del motore di filtro. Questo diritto di accesso è necessario per chiamare [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ Read**
</dt> <dd> <dl> <dt>



Lettura. Questo diritto di accesso è necessario per chiamare le funzioni [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) e [**Fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) .


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_ \_ statistiche leggere FWPM \_ ACTRL**
</dt> <dd> <dl> <dt>



Leggere le statistiche. Questo diritto di accesso è necessario per chiamare [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) e [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**sottoscrizione di FWPM \_ ACTRL \_**
</dt> <dd> <dl> <dt>



Eseguire la sottoscrizione. Questo diritto di accesso è necessario per chiamare le [**funzioni \* SubscribeChanges0 di Fwpm**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) . Per ricevere una notifica per un oggetto, un Sottoscrittore deve \_ \_ avere anche l'accesso in lettura a FWPM ACTRL per l'oggetto.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**\_scrittura FWPM ACTRL \_**
</dt> <dd> <dl> <dt>



Opzioni del motore di scrittura. Questo diritto di accesso è necessario per chiamare [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**\_lettura generica FWPM \_**
</dt> <dd> <dl> <dt>



\_diritti standard \_ letti \| FWPM \_ ACTRL \_ Begin \_ Read \_ transazione \| FWPM \_ ACTRL \_ classifica \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM \_ ACTRL \_ Read \_ Statistics


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**\_esecuzione generica FWPM \_**
</dt> <dd> <dl> <dt>



\_diritti standard \_ Execute \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ Subscribe


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**\_scrittura generica FWPM \_**
</dt> <dd> <dl> <dt>



\_Rights \_ Write \| ( \| FWPM) \_ ACTRL \_ Aggiungi \| FWPM ACTRL Aggiungi \_ \_ \_ collegamento \| FWPM \_ ACTRL \_ Begin \_ Write \_ transazione \| \_ \_ FWPM ACTRL Write


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ generico \_ All**
</dt> <dd> <dl> <dt>



\_diritti standard \_ necessari \| FWPM \_ ACTRL \_ Aggiungi \| FWPM \_ ACTRL \_ Aggiungi \_ collegamento \| FWPM \_ ACTRL \_ Begin \_ Read \_ transazione \| FWPM \_ ACTRL \_ Begin \_ Write \_ transazione FWPM ACTRL \| \_ \_ classifica \| FWPM \_ ACTRL enum FWPM ACTRL \_ \| \_ \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM \_ ACTRL \_ Read \_ Statistics \| FWPM ACTRL Subscribe FWPM \_ \_ \| \_ ACTRL \_ Write


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modello di controllo di accesso della piattaforma filtro Windows](access-control.md)
</dt> <dt>

[Diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

