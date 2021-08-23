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
ms.openlocfilehash: 7b02d1f617f7e558acd9c0423dd785c84e0175f195ee0085b2fdc79d66054683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628921"
---
# <a name="session-object-windows-installer"></a>Oggetto Session (Windows Installer)

**L'oggetto Session** controlla il processo di installazione. Apre il database del programma di installazione, che contiene le tabelle e i dati di installazione. Questo oggetto è associato a un set standard di funzioni di azione, ognuna delle quali esegue operazioni specifiche sui dati di una o più tabelle. È possibile aggiungere azioni personalizzate aggiuntive per determinate installazioni di prodotti. La funzione del motore di base è un sequencer che recupera record sequenziali da una tabella di sequenza designata, valuta qualsiasi espressione di condizione specificata ed esegue l'azione designata. Le azioni non riconosciute dal motore vengono rinviate all'oggetto gestore dell'interfaccia utente per l'elaborazione, in genere sequenze di finestre di dialogo.

Si noti che un **solo oggetto Session** può essere aperto da un singolo processo.

## <a name="members"></a>Membri

**L'oggetto Session** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Session** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DoAction**](session-doaction.md)                   | Esegue l'azione specificata. <br/>                                                                                                                                                                                                                                |
| [**EvaluateCondition**](session-evaluatecondition.md) | Valuta un'espressione logica contenente simboli e valori e restituisce un intero dell'enumerazione msiEvaluateConditionErrorEnum.<br/>                                                                                                                          |
| [**FeatureInfo**](session-featureinfo.md)             | Restituisce un [**oggetto FeatureInfo**](featureinfo-object.md) contenente informazioni descrittive per la funzionalità specificata.<br/>                                                                                                                                       |
| [**FormatRecord**](session-formatrecord.md)           | Restituisce una stringa formattata dai dati del modello e del record.<br/>                                                                                                                                                                                                      |
| [**Messaggio**](session-message.md)                     | Esegue le operazioni di registrazione abilitate e rinvia l'esecuzione all'oggetto gestore dell'interfaccia utente associato al motore.<br/>                                                                                                                                              |
| [**Sequenza**](session-sequence.md)                   | Apre una query sulla tabella specificata, ordinando le azioni in base ai numeri nella colonna Sequenza. Per ogni riga recuperata, viene chiamato il [**metodo DoAction,**](session-doaction.md) a condizione che qualsiasi espressione di condizione fornita non restituirà False.<br/> |
| [**SetInstallLevel**](session-setinstalllevel.md)     | Imposta il livello di installazione per l'installazione corrente su un valore specificato e ricalcola gli stati Seleziona e Installato per tutte le funzionalità.<br/>                                                                                                                    |



 

### <a name="properties"></a>Proprietà

**L'oggetto Session** ha queste proprietà.



| Proprietà                                                                  | Tipo di accesso           | Descrizione                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComponentCosts**](session-componentcosts.md)<br/>               |                       | Restituisce un [**oggetto RecordList**](recordlist-object.md) che enumera lo spazio su disco per ogni unità necessaria per installare un componente.<br/>                                  |
| [**ComponentCurrentState**](session-componentcurrentstate.md)<br/> |                       | Restituisce lo stato corrente installato del componente designato.<br/>                                                                                                |
| [**ComponentRequestState**](session-componentrequeststate.md)<br/> |                       | Ottiene o richiede una modifica dello stato Azione di una riga nella tabella Component.<br/>                                                                               |
| [**Database**](session-database.md)<br/>                           |                       | Restituisce il database per la sessione di installazione corrente.<br/>                                                                                                      |
| [**FeatureCost**](session-featurecost.md)<br/>                     |                       | Restituisce la quantità totale di spazio su disco (in unità di 512 byte) richiesta dalla funzionalità specificata e dalle relative funzionalità padre (fino alla radice della tabella Funzionalità).<br/> |
| [**FeatureCurrentState**](session-featurecurrentstate.md)<br/>     |                       | Restituisce lo stato corrente installato della funzionalità designata.<br/>                                                                                                  |
| [**FeatureRequestState**](session-featurerequeststate.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o richiede una modifica nello stato Seleziona del record e dei sottorecord di una funzionalità.<br/>                                                                          |
| [**FeatureValidStates**](session-featurevalidstates.md)<br/>       |                       | Restituisce un intero che rappresenta i flag di bit con ogni bit pertinente che rappresenta uno stato di installazione valido per la funzionalità specificata.<br/>                             |
| [**Programma di installazione**](session-installer.md)<br/>                         |                       | Restituisce l'oggetto del programma di installazione attivo.<br/>                                                                                                                            |
| [**Language (oggetto Session)**](session-language.md)<br/>          |                       | Rappresenta l'identificatore di lingua numerico utilizzato dalla sessione di installazione corrente.<br/>                                                                            |
| [**Mode**](session-mode.md)<br/>                                   |                       | Questa proprietà è un valore che rappresenta il flag di modalità designato per la sessione di installazione corrente.<br/>                                                            |
| [**ProductProperty**](session-productproperty.md)<br/>             |                       | Rappresenta il valore stringa di una proprietà del programma di installazione denominata.<br/>                                                                                                      |
| [**Proprietà (oggetto Session)**](session-session.md)<br/>           | Lettura/Scrittura<br/> | Recupera le proprietà del prodotto dal database del prodotto.<br/>                                                                                                         |
| [**SourcePath**](session-sourcepath.md)<br/>                       |                       | Fornisce il percorso completo della cartella designata nel supporto di origine o nell'immagine del server.<br/>                                                                            |
| [**Targetpath**](session-targetpath.md)<br/>                       | Lettura/Scrittura<br/> | Fornisce il percorso completo della cartella designata nell'unità di destinazione dell'installazione.<br/>                                                                               |
| [**VerifyDiskSpace**](session-verifydiskspace.md)<br/>             |                       | Restituisce true se lo spazio su disco è sufficiente e false se il disco è pieno.<br/>                                                                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession è definito \_ come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Esempi di scripting del programma di installazione](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




