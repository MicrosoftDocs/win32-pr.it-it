---
description: Il metodo FindCard cerca il smart card e apre una connessione valida.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: Metodo ISCardLocate::FindCard (Scardmgr.h)
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
ms.openlocfilehash: a0db06f9dcafd211f628eb7cd0be9ed2f800b6f1b980d8e2320cd82b2849d386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014241"
---
# <a name="iscardlocatefindcard-method"></a>Metodo ISCardLocate::FindCard

\[Il **metodo FindCard** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo FindCard** cerca il [*smart card*](../secgloss/s-gly.md) e apre una connessione valida.

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

*ShareMode* \[ Pollici\]
</dt> <dd>

Modalità in cui condividere o meno l'smart card quando viene aperta una connessione.



| Valore                                                                                                                                            | Significato                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Esclusivo**</dt> </dl> | Nessun altro usa questa connessione al smart card.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**condiviso**</dt> </dl>          | Altre applicazioni possono usare questa connessione.<br/>        |



 

</dd> <dt>

*Protocolli* \[ Pollici\]
</dt> <dd>

Protocollo da utilizzare per la connessione alla scheda.

T0

T1

RAW

T0 \| T1

</dd> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Specifica quando viene [*visualizzata l'interfaccia*](../secgloss/u-gly.md) utente:



| Valore                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**INTERFACCIA \_ UTENTE MINIMA SC DLG \_ \_**</dt> </dl> | Visualizza la finestra di dialogo solo se la scheda cercata dall'applicazione chiamante non è individuata e disponibile per l'uso in un lettore. In questo modo la scheda può essere trovata, connessa (tramite un meccanismo interno della finestra di dialogo o usando le funzioni di callback dell'utente) e restituita all'applicazione chiamante.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ NO \_ UI**</dt> </dl>                | Non determina la visualizzazione dell'interfaccia utente, indipendentemente dal risultato della ricerca.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**INTERFACCIA \_ UTENTE DI SC DLG \_ FORCE \_**</dt> </dl>       | Determina la visualizzazione dell'interfaccia utente indipendentemente dal risultato della ricerca.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*ppCardInfo* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a una struttura di dati che contiene o restituisce informazioni sul smart card aperto, [*se*](../secgloss/s-gly.md)ha esito positivo. Sarà NULL **se** l'operazione non è riuscita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                        |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido in *ppCardInfo*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                            |



 

## <a name="remarks"></a>Commenti

Per impostare i criteri di ricerca della ricerca, chiamare [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) per specificare i smart card della scheda.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardLocate**](iscardlocate.md).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardLocate è definito come \_ 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
