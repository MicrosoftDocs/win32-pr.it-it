---
description: L'oggetto Session controlla il processo di installazione.
ms.assetid: 013959d9-900c-45f7-b742-17b0365d6107
title: Oggetto Session (Windows Installer)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c391249d5ccc58fe9a947c9db761a77521c9776d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333043"
---
# <a name="session-object-windows-installer"></a>Oggetto Session (Windows Installer)

L'oggetto **Session** controlla il processo di installazione. Viene aperto il database del programma di installazione che contiene i dati e le tabelle di installazione. Questo oggetto è associato a un set standard di funzioni di azione, ciascuna delle quali esegue operazioni specifiche sui dati di una o più tabelle. È possibile aggiungere azioni personalizzate aggiuntive per le installazioni di prodotti particolari. La funzione del motore di base è un sequencer che recupera i record sequenziali da una tabella di sequenza designata, valuta qualsiasi espressione di condizione specificata ed esegue l'azione designata. Le azioni non riconosciute dal motore sono rinviate all'oggetto gestore dell'interfaccia utente per l'elaborazione, in genere sequenze di finestre di dialogo.

Si noti che solo un oggetto **sessione** può essere aperto da un singolo processo.

## <a name="members"></a>Membri

L'oggetto **sessione** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **Session** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DoAction**](session-doaction.md)                   | Esegue l'azione specificata. <br/>                                                                                                                                                                                                                                |
| [**EvaluateCondition**](session-evaluatecondition.md) | Valuta un'espressione logica contenente i simboli e i valori e restituisce un Integer dell'enumerazione msiEvaluateConditionErrorEnum.<br/>                                                                                                                          |
| [**FeatureInfo**](session-featureinfo.md)             | Restituisce un oggetto [**FeatureInfo**](featureinfo-object.md) che contiene informazioni descrittive per la funzionalità specificata.<br/>                                                                                                                                       |
| [**FormatRecord**](session-formatrecord.md)           | Restituisce una stringa formattata dai dati del modello e del record.<br/>                                                                                                                                                                                                      |
| [**Messaggio**](session-message.md)                     | Esegue tutte le operazioni di registrazione abilitate e rinvia l'esecuzione all'oggetto gestore dell'interfaccia utente associato al motore.<br/>                                                                                                                                              |
| [**Sequenza**](session-sequence.md)                   | Apre una query sulla tabella specificata, ordinando le azioni in base ai numeri nella colonna sequenza. Per ogni riga recuperata, viene chiamato il metodo [**DoAction**](session-doaction.md) , purché le espressioni di condizione fornite non restituiscono false.<br/> |
| [**SetInstallLevel**](session-setinstalllevel.md)     | Imposta il livello di installazione per l'installazione corrente su un valore specificato e Ricalcola gli stati selezionati e installati per tutte le funzionalità.<br/>                                                                                                                    |



 

### <a name="properties"></a>Proprietà

L'oggetto **Session** dispone di queste proprietà.



| Proprietà                                                                  | Tipo di accesso           | Descrizione                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComponentCosts**](session-componentcosts.md)<br/>               |                       | Restituisce un oggetto di [**record**](recordlist-object.md) che enumera lo spazio su disco per unità richiesta per l'installazione di un componente.<br/>                                  |
| [**ComponentCurrentState**](session-componentcurrentstate.md)<br/> |                       | Restituisce lo stato corrente installato del componente designato.<br/>                                                                                                |
| [**ComponentRequestState**](session-componentrequeststate.md)<br/> |                       | Ottiene o richiede una modifica nello stato dell'azione di una riga nella tabella dei componenti.<br/>                                                                               |
| [**Database**](session-database.md)<br/>                           |                       | Restituisce il database per la sessione di installazione corrente.<br/>                                                                                                      |
| [**FeatureCost**](session-featurecost.md)<br/>                     |                       | Restituisce la quantità totale di spazio su disco, in unità di 512 byte, richiesta dalla funzionalità specificata e dalle relative funzionalità padre (fino alla radice della tabella delle funzionalità).<br/> |
| [**FeatureCurrentState**](session-featurecurrentstate.md)<br/>     |                       | Restituisce lo stato di installazione corrente della funzionalità designata.<br/>                                                                                                  |
| [**FeatureRequestState**](session-featurerequeststate.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o richiede una modifica nello stato di selezione del record e dei sottorecord di una funzionalità.<br/>                                                                          |
| [**FeatureValidStates**](session-featurevalidstates.md)<br/>       |                       | Restituisce un Integer che rappresenta i flag di bit con ogni bit pertinente che rappresenta uno stato di installazione valido per la funzionalità specificata.<br/>                             |
| [**Programma di installazione**](session-installer.md)<br/>                         |                       | Restituisce l'oggetto del programma di installazione attivo.<br/>                                                                                                                            |
| [**Language (oggetto Session)**](session-language.md)<br/>          |                       | Rappresenta l'identificatore di lingua numerico utilizzato dalla sessione di installazione corrente.<br/>                                                                            |
| [**Modalità**](session-mode.md)<br/>                                   |                       | Questa proprietà è un valore che rappresenta il flag della modalità designata per la sessione di installazione corrente.<br/>                                                            |
| [**ProductProperty**](session-productproperty.md)<br/>             |                       | Rappresenta il valore stringa di una proprietà del programma di installazione denominata.<br/>                                                                                                      |
| [**Proprietà (oggetto Session)**](session-session.md)<br/>           | Lettura/Scrittura<br/> | Recupera le proprietà del prodotto dal database del prodotto.<br/>                                                                                                         |
| [**SourcePath**](session-sourcepath.md)<br/>                       |                       | Fornisce il percorso completo della cartella designata nel supporto di origine o nell'immagine server.<br/>                                                                            |
| [**TargetPath**](session-targetpath.md)<br/>                       | Lettura/Scrittura<br/> | Fornisce il percorso completo della cartella designata nell'unità di destinazione dell'installazione.<br/>                                                                               |
| [**VerifyDiskSpace**](session-verifydiskspace.md)<br/>             |                       | Restituisce true se è disponibile spazio su disco sufficiente e false se il disco è pieno.<br/>                                                                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




