---
description: Un handle HRECOCONTEXT viene usato per aggiungere input penna al contesto, eseguire il riconoscimento dell'input penna (in modalità sincrona o asincrona), recuperare il risultato del riconoscimento e recuperare le alternative.
ms.assetid: 509188e2-28af-4915-bc76-ee451133398f
title: Handle HRECOCONTEXT (riepilogo. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13ef2b6f629587de84f831fd32a31f42a208c024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879378"
---
# <a name="hrecocontext-handle"></a>Handle HRECOCONTEXT

Un handle **HRECOCONTEXT** viene usato per aggiungere input penna al contesto, eseguire il riconoscimento dell'input penna (in modalità sincrona o asincrona), recuperare il risultato del riconoscimento e recuperare le alternative.

Il motivo principale per cui gli handle di contesto del riconoscimento è distinguere tra input input penna. Ad esempio, è possibile creare un'applicazione con due finestre, l'utente che è in grado di eseguire l'input penna in entrambe le finestre. Non si desidera che l'input penna della prima finestra venga confuso con l'input penna della seconda finestra quando si chiede al riconoscimento di riconoscere l'input penna di una delle finestre. In questo tipo di applicazione, si creano due contesti di riconoscimento (uno per ogni finestra) e si aggiungono i tratti in arrivo nella finestra 1 nel contesto di riconoscimento 1 e i tratti dalla finestra 2 al contesto di riconoscimento 2. Per restituire i risultati del riconoscimento, chiamare il metodo Process sul contesto di riconoscimento 1 o sul contesto del riconoscitore 2 a seconda che si desiderino i risultati per la finestra 1 o 2.

L'handle del contesto del riconoscimento può essere qualsiasi elemento desiderato. Ma in genere si tratta di un indice in una matrice globale di strutture. Le strutture possono contenere tutti i tratti che sono stati immessi e tutte le variabili utilizzate dal riconoscitore per quel particolare componente di input penna, ad esempio la struttura del reticolo interna o lo stato corrente del riconoscimento. Una struttura può contenere tutte le informazioni necessarie per il riconoscimento e utilizzarle per un particolare componente di input penna.

Per ottenere un handle **HRECOCONTEXT** , chiamare la funzione [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) .


```C++
typedef HANDLE HRECOCONTEXT;
```



## <a name="remarks"></a>Commenti

Di seguito sono riportate le funzioni **HRECOCONTEXT**



| Funzione                                                            | Descrizione                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStroke**](/windows/desktop/api/recapis/nf-recapis-addstroke)                                      | Aggiunge un tratto di input penna al contesto del riconoscimento.<br/>                                                                                                                                                                                                    |
| [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange)                          | Arresta l'elaborazione dell'input penna da parte del riconoscimento perché è in corso l'aggiunta o l'eliminazione di un nuovo tratto.<br/>                                                                                                                                                         |
| [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext)                                | Crea un contesto di riconoscimento che contiene le stesse impostazioni dell'oggetto originale. Il nuovo contesto di riconoscimento non include i risultati dell'input penna o del riconoscimento dell'originale.<br/>                                                                        |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)             | Indica che al contesto non verrà aggiunto altro input penna.<br/>                                                                                                                                                                                         |
| [**Getalternance**](/previous-versions/windows/desktop/legacy/ms698163(v=vs.85))                        | Restituisce un elenco di alternative per la stringa di risultato migliore.<br/>                                                                                                                                                                                         |
| [**GetBestAlternate**](/previous-versions/windows/desktop/legacy/ms699575(v=vs.85))                        | Restituisce un puntatore all' [handle HRECOALT](hrecoalt-handle.md) per l'alternativa del risultato migliore.<br/>                                                                                                                                                         |
| [**GetBestResultString**](/windows/desktop/api/recapis/nf-recapis-getbestresultstring)                  | Restituisce la stringa di risultato migliore.<br/>                                                                                                                                                                                                                  |
| [**GetContextPropertyList**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)            | Restituisce un elenco di proprietà supportate dal riconoscimento.<br/>                                                                                                                                                                                            |
| [**GetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)          | Restituisce un valore di proprietà specificato dal contesto del riconoscimento.<br/>                                                                                                                                                                                  |
| [**GetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)          | Restituisce un elenco di intervalli di punti Unicode abilitati nel contesto.<br/>                                                                                                                                                                                   |
| [**Getguide**](/windows/desktop/api/recapis/nf-recapis-getguide)                                        | Restituisce la guida utilizzata per l'input boxed o rigato.<br/>                                                                                                                                                                                                 |
| [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)                              | Restituisce un puntatore al reticolo per i risultati correnti.<br/>                                                                                                                                                                                        |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) | Restituisce un valore che indica se una parola, una data, un'ora, un numero o un altro testo passato è contenuto nel dizionario.<br/>                                                                                                               |
| [**Processo**](/windows/desktop/api/recapis/nf-recapis-process)                                          | Esegue in modo sincrono il riconoscimento dell'input penna.<br/>                                                                                                                                                                                                          |
| [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext)                                | Elimina l'input penna corrente e i risultati del riconoscimento dal contesto.<br/>                                                                                                                                                                                |
| [**SetCACMode**](/windows/desktop/api/recapis/nf-recapis-setcacmode)                                    | Specifica la modalità di completamento automatico dei caratteri per il riconoscimento di caratteri o parole.<br/>                                                                                                                                                                         |
| [**SetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)          | Aggiunge una proprietà al contesto del riconoscimento. Se una proprietà esiste già, il relativo valore viene modificato.<br/>                                                                                                                                                  |
| [**SetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)          | Abilita uno o più intervalli di punti Unicode nel contesto.<br/>                                                                                                                                                                                         |
| [**SetFactoid**](/windows/desktop/api/recapis/nf-recapis-setfactoid)                                    | Imposta il controllo oggetto utilizzato da un riconoscimento per vincolare la ricerca del risultato.<br/>                                                                                                                                                                       |
| [**SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)                                        | Imposta il modo in cui il riconoscimento interpreta l'input penna e determina la stringa di risultato.<br/>                                                                                                                                                                     |
| [**Guida di riferimento**](/windows/desktop/api/recapis/nf-recapis-setguide)                                        | Imposta la guida da utilizzare per l'input boxed o rigato.<br/>                                                                                                                                                                                                  |
| [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext)                            | Fornisce le stringhe di testo che precedono e si trovano dopo il testo contenuto nel contesto del riconoscitore. Per i riconoscitori dei caratteri asiatici orientali, la funzione [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext) fornisce caratteri anziché stringhe di testo.<br/> |
| [**SetWordList**](/windows/desktop/api/recapis/nf-recapis-setwordlist)                                  | Imposta l'elenco di parole per il contesto di riconoscimento corrente da riconoscere.<br/>                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Riepilogo. h</dt> </dl> |



 

