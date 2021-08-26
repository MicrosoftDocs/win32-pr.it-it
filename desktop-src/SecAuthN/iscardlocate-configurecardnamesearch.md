---
description: Il metodo ConfigureCardNameSearch specifica i nomi delle schede da usare nella ricerca del smart card.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: Metodo ISCardLocate::ConfigureCardNameSearch (Scardmgr.h)
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
ms.openlocfilehash: e49b7653a434f54bfa706aea0bde63048d6b511e5143ade34f0b4e8225a6042b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014267"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a>Metodo ISCardLocate::ConfigureCardNameSearch

\[Il **metodo ConfigureCardNameSearch** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ConfigureCardNameSearch** specifica i nomi delle schede da usare nella ricerca dell'smart card [*.*](../secgloss/s-gly.md)

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

*pCardNames* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice sicura di nomi di scheda di Automazione in formato BSTR.

</dd> <dt>

*pGroupNames* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice sicura di automazione di nomi di gruppi di schede/lettori in formato BSTR da aggiungere alla ricerca.

</dd> <dt>

*bstrTitle* \[ Pollici\]
</dt> <dd>

Titolo della finestra di dialogo per il controllo comune di ricerca.

</dd> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Specifica quando viene [*visualizzata l'interfaccia*](../secgloss/u-gly.md) utente.



| Valore                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**INTERFACCIA \_ UTENTE MINIMA SC DLG \_ \_**</dt> </dl> | Visualizza la finestra di dialogo solo se la scheda cercata dall'applicazione chiamante non è individuata e disponibile per l'uso in un lettore. In questo modo la scheda può essere trovata, connessa (tramite un meccanismo interno della finestra di dialogo o usando le funzioni di callback dell'utente) e restituita all'applicazione chiamante.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ NO \_ UI**</dt> </dl>                | Non determina la visualizzazione dell'interfaccia utente, indipendentemente dal risultato della ricerca.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**INTERFACCIA \_ UTENTE DI SC DLG \_ FORCE \_**</dt> </dl>       | Determina la visualizzazione dell'interfaccia utente indipendentemente dal risultato della ricerca.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                                         |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido in *pCardNames* *o pGroupNames*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                                             |



 

## <a name="remarks"></a>Commenti

Per individuare il [*smart card,*](../secgloss/s-gly.md)chiamare [**FindCard**](iscardlocate-findcard.md).

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

[**FindCard**](iscardlocate-findcard.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
