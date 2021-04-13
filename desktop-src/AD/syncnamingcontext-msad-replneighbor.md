---
title: Metodo SyncNamingContext della classe MSAD_ReplNeighbor
description: Chiama la funzione DsReplicaSync che sincronizza un contesto dei nomi di destinazione con una delle relative origini.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Active Directory del metodo SyncNamingContext
- Metodo SyncNamingContext Active Directory, classe MSAD_ReplNeighbor
- Classe MSAD_ReplNeighbor Active Directory, metodo SyncNamingContext
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691bd3e943f491ba93d867097ac0167c97be6108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478286"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a>Metodo SyncNamingContext della classe MSAD \_ ReplNeighbor

Chiama la funzione [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) che sincronizza un contesto dei nomi di destinazione con una delle relative origini.

## <a name="syntax"></a>Sintassi


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Opzioni* \[ di in\]
</dt> <dd>

Dati aggiuntivi che determinano la modalità di elaborazione della richiesta da parte del metodo. Questo parametro può essere una combinazione dei valori seguenti.

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**\_ \_ Aggiungi \_ riferimento a DS REPSYNC**


</dt> <dd>

Fa in modo che il Directory System Agent di origine (DSA) verifichi che il DSA locale sia presente nell'elenco replicate di origine. Se il DSA locale non è presente, viene aggiunto. In questo modo si garantisce che l'origine invii le notifiche di modifica.

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ REPSYNC \_ tutte le \_ origini**


</dt> <dd>

Questo valore non è supportato.

**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Sincronizza da tutte le origini.

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**\_ \_ operazione asincrona REPSYNC \_ DS**


</dt> <dd>

Esegue questa operazione in modo asincrono.

**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Obbligatorio quando si usa **DS \_ REPSYNC \_ tutte le \_ origini**.

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**\_forza REPSYNC \_ DS**


</dt> <dd>

Viene sincronizzato anche se il collegamento è attualmente disabilitato.

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ REPSYNC \_ completo**


</dt> <dd>

Viene sincronizzato a partire dal primo numero di sequenza di aggiornamento (USN).

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**\_messaggistica tra \_ siti DS \_ REPSYNC**


</dt> <dd>

Viene sincronizzato utilizzando ISM.

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ REPSYNC \_ No \_ scarto**


</dt> <dd>

Non rimuove questa richiesta di sincronizzazione, anche se è in sospeso una sincronizzazione simile.

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ REPSYNC \_ periodica**


</dt> <dd>

Indica che questa operazione è una richiesta di sincronizzazione periodica pianificata dall'amministratore.

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ REPSYNC \_ urgente**


</dt> <dd>

Indica che questa operazione è una notifica di un aggiornamento contrassegnato come urgente.

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ REPSYNC \_ scrivibile**


</dt> <dd>

Indica che la replica è scrivibile. Se questo flag non è impostato, la replica è di sola lettura.

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

[**\_REPLNEIGHBOR MSAD**](msad-replneighbor.md)
</dt> </dl>

 

 





