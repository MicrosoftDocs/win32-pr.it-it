---
description: Il metodo FindCard cerca la smart card e apre una connessione valida.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'Metodo ISCardLocate:: FindCard (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf3cf05ff6e6040d5cac2bde161fa2eea07d5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311617"
---
# <a name="iscardlocatefindcard-method"></a>Metodo ISCardLocate:: FindCard

\[Il metodo **FindCard** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **FindCard** cerca la [*Smart Card*](../secgloss/s-gly.md) e apre una connessione valida.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SHAREMODE* \[ in\]
</dt> <dd>

Modalità in cui condividere o non condividere la smart card quando viene aperta una connessione.



| Valore                                                                                                                                            | Significato                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**ESCLUSIVO**</dt> </dl> | Nessun altro usa questa connessione alla smart card.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**CONDIVISO**</dt> </dl>          | Questa connessione può essere utilizzata da altre applicazioni.<br/>        |



 

</dd> <dt>

*Protocolli* \[ di in\]
</dt> <dd>

Protocollo da usare per la connessione alla scheda.

T0

T1

RAW

T0 \| T1

</dd> <dt>

*è* \[ in\]
</dt> <dd>

Specifica quando viene visualizzata l' [*interfaccia utente*](../secgloss/u-gly.md) :



| Valore                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**\_ \_ interfaccia utente minima di SC DLG \_**</dt> </dl> | Visualizza la finestra di dialogo solo se la scheda cercata dall'applicazione chiamante non si trova e non è disponibile per l'utilizzo in un lettore. Ciò consente di trovare la scheda, connessa (tramite un meccanismo interno della finestra di dialogo o usando le funzioni di callback utente) e restituita all'applicazione chiamante.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ Nessuna \_ interfaccia utente**</dt> </dl>                | Non comporta la visualizzazione dell'interfaccia utente, indipendentemente dal risultato della ricerca.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**\_ \_ interfaccia utente Force SC DLG \_**</dt> </dl>       | Causa la visualizzazione dell'interfaccia utente indipendentemente dal risultato della ricerca.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*ppCardInfo* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura di dati che contiene o restituisce informazioni sulla [*Smart Card*](../secgloss/s-gly.md)aperta, in caso di esito positivo. Sarà **null** se l'operazione non è riuscita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                        |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *ppCardInfo*.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                            |



 

## <a name="remarks"></a>Commenti

Per impostare i criteri di ricerca della ricerca, chiamare [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) per specificare i nomi delle schede della smart card.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardLocate**](iscardlocate.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate è definito come 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
