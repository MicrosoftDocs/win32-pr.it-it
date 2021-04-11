---
description: Il metodo ConfigureCardNameSearch specifica i nomi delle schede da usare nella ricerca della smart card.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'Metodo ISCardLocate:: ConfigureCardNameSearch (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232038"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a>Metodo ISCardLocate:: ConfigureCardNameSearch

\[Il metodo **ConfigureCardNameSearch** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **ConfigureCardNameSearch** specifica i nomi delle schede da usare nella ricerca della [*Smart Card*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCardNames* \[ in\]
</dt> <dd>

Puntatore a una matrice di nomi di schede sicura di automazione in formato BSTR.

</dd> <dt>

*pGroupNames* \[ in\]
</dt> <dd>

Puntatore a una matrice sicura di automazione dei nomi dei gruppi di schede/Reader nel formato BSTR da aggiungere alla ricerca.

</dd> <dt>

*bstrTitle* \[ in\]
</dt> <dd>

Titolo della finestra di dialogo per il controllo comune di ricerca.

</dd> <dt>

*è* \[ in\]
</dt> <dd>

Specifica quando viene visualizzata l' [*interfaccia utente*](../secgloss/u-gly.md) .



| Valore                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**\_ \_ interfaccia utente minima di SC DLG \_**</dt> </dl> | Visualizza la finestra di dialogo solo se la scheda cercata dall'applicazione chiamante non si trova e non è disponibile per l'utilizzo in un lettore. Ciò consente di trovare la scheda, connessa (tramite un meccanismo interno della finestra di dialogo o usando le funzioni di callback utente) e restituita all'applicazione chiamante.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ Nessuna \_ interfaccia utente**</dt> </dl>                | Non comporta la visualizzazione dell'interfaccia utente, indipendentemente dal risultato della ricerca.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**\_ \_ interfaccia utente Force SC DLG \_**</dt> </dl>       | Causa la visualizzazione dell'interfaccia utente indipendentemente dal risultato della ricerca.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                                         |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *pCardNames* o *pGroupNames*.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                                             |



 

## <a name="remarks"></a>Commenti

Per individuare la [*Smart Card*](../secgloss/s-gly.md), chiamare [**FindCard**](iscardlocate-findcard.md).

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

[**FindCard**](iscardlocate-findcard.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
