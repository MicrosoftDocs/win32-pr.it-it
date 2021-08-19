---
title: Metodo SyncNamingContext della classe MSAD_ReplNeighbor
description: Chiama la funzione DsReplicaSync che sincronizza un contesto dei nomi di destinazione con una delle relative origini.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Metodo SyncNamingContext Active Directory
- Metodo SyncNamingContext Active Directory, MSAD_ReplNeighbor classe
- MSAD_ReplNeighbor classe Active Directory , metodo SyncNamingContext
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
ms.openlocfilehash: 2b96dd7363b5c2a48a6c25826d8c2752c181bc9125955b6c73d5532eb2665514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024669"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a>Metodo SyncNamingContext della classe MSAD \_ ReplNeighbor

Chiama la [**funzione DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) che sincronizza un contesto dei nomi di destinazione con una delle relative origini.

## <a name="syntax"></a>Sintassi


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Opzioni* \[ Pollici\]
</dt> <dd>

Dati aggiuntivi che determinano il modo in cui il metodo elabora la richiesta. Questo parametro può essere una combinazione dei valori seguenti.

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**INFORMAZIONI DI RIFERIMENTO SU \_ DS REPSYNC \_ \_ ADD**


</dt> <dd>

Fa in modo che l'agente del sistema di directory di origine (DSA) verifichi che il DSA locale sia presente nell'elenco replica-a di origine. Se il DSA locale non è presente, viene aggiunto. Ciò garantisce che l'origine invii notifiche di modifica.

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ REPSYNC \_ ALL \_ SOURCES**


</dt> <dd>

Questo valore non è supportato.

**Windows Server 2008 R2, Windows Server 2008 e Windows Server 2003:** Esegue la sincronizzazione da tutte le origini.

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**OPERAZIONE \_ ASINCRONA DI DS REPSYNC \_ \_**


</dt> <dd>

Esegue questa operazione in modo asincrono.

**Windows Server 2008 R2, Windows Server 2008 e Windows Server 2003:** Obbligatorio quando si **usa DS \_ REPSYNC \_ ALL \_ SOURCES**.

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**FORZA \_ REPSYNC DS \_**


</dt> <dd>

Esegue la sincronizzazione anche se il collegamento è attualmente disabilitato.

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ REPSYNC \_ FULL**


</dt> <dd>

Esegue la sincronizzazione a partire dal primo numero di sequenza di aggiornamento (USN).

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**MESSAGGISTICA TRA SITI DI DS \_ REPSYNC \_ \_**


</dt> <dd>

Esegue la sincronizzazione usando un ISM.

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ REPSYNC \_ NO \_ DISCARD**


</dt> <dd>

Non rimuove questa richiesta di sincronizzazione, anche se è in sospeso una sincronizzazione simile.

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ REPSYNC \_ PERIODIC**


</dt> <dd>

Indica che questa operazione è una richiesta di sincronizzazione periodica pianificata dall'amministratore.

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ REPSYNC \_ URGENT**


</dt> <dd>

Indica che questa operazione è una notifica di un aggiornamento contrassegnato come urgente.

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ REPSYNC \_ SCRIVIBILE**


</dt> <dd>

Indica che questa replica è scrivibile. Se questo flag non è impostato, la replica è di sola lettura.

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

[**MSAD \_ ReplNeighbor**](msad-replneighbor.md)
</dt> </dl>

 

 





