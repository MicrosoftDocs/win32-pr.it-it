---
description: Un handle HRECOCONTEXT viene usato per aggiungere input penna al contesto, eseguire il riconoscimento input penna (in modo sincrono o asincrono), recuperare il risultato del riconoscimento e recuperare le alternative.
ms.assetid: 509188e2-28af-4915-bc76-ee451133398f
title: Handle HRECOCONTEXT (Recapis.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9be012cc624553ae9573dc361c364d4ef61ec4c6d72fbf7c3eb2168c3ccb290
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935541"
---
# <a name="hrecocontext-handle"></a>HRECOCONTEXT Handle

Un handle **HRECOCONTEXT** viene usato per aggiungere input penna al contesto, eseguire il riconoscimento input penna (in modo sincrono o asincrono), recuperare il risultato del riconoscimento e recuperare le alternative.

Il motivo principale per cui si hanno handle di contesto del riconoscimento è la distinzione tra input penna. Ad esempio, è possibile creare un'applicazione con due finestre, l'utente può usare l'input penna in entrambe le finestre. Non si vuole che l'input penna della prima finestra sia misto all'input penna della seconda finestra quando si chiede al sistema di riconoscimento di riconoscere l'input penna di una delle finestre. In questo tipo di applicazione si creano due contesti di riconoscimento (uno per ogni finestra) e si aggiungono tratti in arrivo nella finestra 1 nel contesto di riconoscimento 1 e tratti dalla finestra 2 al contesto di riconoscimento 2. Per restituire i risultati del riconoscimento, chiamare il processo nel contesto di riconoscimento 1 o nel contesto di riconoscimento 2 a seconda che si desiderino i risultati per la finestra 1 o 2.

L'handle di contesto del riconoscitore può essere qualsiasi elemento desiderato. Ma in genere si tratta di un indice in una matrice globale di strutture. Le strutture possono contenere tutti i tratti immessi e tutte le variabili che il riconoscimento usa per quella particolare parte dell'input penna (ad esempio, la struttura a reticolo interno o lo stato di riconoscimento corrente). Una struttura può contenere tutte le informazioni necessarie al riconoscimento e all'uso per una particolare parte dell'input penna.

Per ottenere un handle **HRECOCONTEXT,** chiamare la [**funzione CreateContext.**](/windows/desktop/api/recapis/nf-recapis-createcontext)


```C++
typedef HANDLE HRECOCONTEXT;
```



## <a name="remarks"></a>Commenti

Di seguito sono riportate le **funzioni HRECOCONTEXT**



| Funzione                                                            | Descrizione                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStroke**](/windows/desktop/api/recapis/nf-recapis-addstroke)                                      | Aggiunge un tratto input penna al contesto del riconoscimento.<br/>                                                                                                                                                                                                    |
| [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange)                          | Arresta l'elaborazione dell'input penna da parte del riconoscimento perché è in corso l'aggiunta o l'eliminazione di un nuovo tratto.<br/>                                                                                                                                                         |
| [**Oggetto CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext)                                | Crea un contesto di riconoscimento che contiene le stesse impostazioni dell'originale. Il nuovo contesto di riconoscimento non include l'input penna o i risultati del riconoscimento dell'originale.<br/>                                                                        |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)             | Indica che non verranno aggiunti altri input penna al contesto.<br/>                                                                                                                                                                                         |
| [**GetAlternateList**](/previous-versions/windows/desktop/legacy/ms698163(v=vs.85))                        | Restituisce un elenco di alternative per la stringa di risultato migliore.<br/>                                                                                                                                                                                         |
| [**GetBestAlternate**](/previous-versions/windows/desktop/legacy/ms699575(v=vs.85))                        | Restituisce un [puntatore handle HRECOALT](hrecoalt-handle.md) per il miglior risultato alternativo.<br/>                                                                                                                                                         |
| [**GetBestResultString**](/windows/desktop/api/recapis/nf-recapis-getbestresultstring)                  | Restituisce la stringa di risultato migliore.<br/>                                                                                                                                                                                                                  |
| [**GetContextPropertyList**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)            | Restituisce un elenco di proprietà supportate dal riconoscimento.<br/>                                                                                                                                                                                            |
| [**GetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)          | Restituisce un valore della proprietà specificato dal contesto del riconoscitore.<br/>                                                                                                                                                                                  |
| [**GetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)          | Restituisce un elenco di intervalli di punti Unicode abilitati nel contesto.<br/>                                                                                                                                                                                   |
| [**GetGuide**](/windows/desktop/api/recapis/nf-recapis-getguide)                                        | Restituisce la guida utilizzata per l'input boxed o lined.<br/>                                                                                                                                                                                                 |
| [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)                              | Restituisce un puntatore al reticolo per i risultati correnti.<br/>                                                                                                                                                                                        |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) | Restituisce un valore che indica se una parola, una data, un'ora, un numero o un altro testo passato è contenuto nel dizionario.<br/>                                                                                                               |
| [**Processo**](/windows/desktop/api/recapis/nf-recapis-process)                                          | Esegue il riconoscimento input penna in modo sincrono.<br/>                                                                                                                                                                                                          |
| [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext)                                | Elimina l'input penna corrente e i risultati del riconoscimento dal contesto.<br/>                                                                                                                                                                                |
| [**SetCACMode**](/windows/desktop/api/recapis/nf-recapis-setcacmode)                                    | Specifica la modalità di completamento automatico dei caratteri per il riconoscimento di caratteri o parole.<br/>                                                                                                                                                                         |
| [**SetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)          | Aggiunge una proprietà al contesto del riconoscitore. Se esiste già una proprietà, il relativo valore viene modificato.<br/>                                                                                                                                                  |
| [**SetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)          | Abilita uno o più intervalli di punti Unicode nel contesto.<br/>                                                                                                                                                                                         |
| [**SetFactoid**](/windows/desktop/api/recapis/nf-recapis-setfactoid)                                    | Imposta il factoid utilizzato da un sistema di riconoscimento per vincolare la ricerca del risultato.<br/>                                                                                                                                                                       |
| [**SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)                                        | Imposta il modo in cui il riconoscimento interpreta l'input penna e determina la stringa di risultato.<br/>                                                                                                                                                                     |
| [**SetGuide**](/windows/desktop/api/recapis/nf-recapis-setguide)                                        | Imposta la guida da utilizzare per l'input boxed o lined.<br/>                                                                                                                                                                                                  |
| [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext)                            | Fornisce le stringhe di testo che vengono prima e dopo il testo contenuto nel contesto del riconoscitore. Per i riconoscitori di caratteri dell'Asia orientale, la [**funzione SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext) fornisce caratteri anziché stringhe di testo.<br/> |
| [**SetWordList**](/windows/desktop/api/recapis/nf-recapis-setwordlist)                                  | Imposta l'elenco di parole per il contesto del riconoscimento corrente da riconoscere.<br/>                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Recapis.h</dt> </dl> |



 

