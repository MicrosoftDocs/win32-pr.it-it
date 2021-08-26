---
title: Strategie di gestione degli errori
description: Strategie di gestione degli errori
ms.assetid: 8d03ede8-0661-43dc-adaf-3c1f5fc1687e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0527edbb8bab4b4a0b0ca9e0d135bc5cf8c2827497a36fb9cad021680868f764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029971"
---
# <a name="error-handling-strategies"></a>Strategie di gestione degli errori

Poiché i metodi di interfaccia sono virtuali, un chiamante non può conoscere il set completo di valori che possono essere restituiti da una chiamata. Un'implementazione di un metodo può restituire cinque valori. un altro può restituire otto.

La documentazione elenca i valori comuni che possono essere restituiti per ogni metodo. si tratta dei valori che è necessario verificare e gestire nel codice perché hanno significati speciali. È possibile che siano restituiti altri valori, ma poiché non sono significativi, non è necessario scrivere codice speciale per gestirli. È sufficiente un semplice controllo per zero o un valore diverso da zero.

## <a name="hresult-values"></a>Valori HRESULT

Il valore restituito di funzioni e metodi COM è **un HRESULT.** I valori di alcuni HRESULT sono stati modificati in COM per eliminare tutte le duplicazioni e le sovrapposizioni con i codici di errore di sistema. Quelli che duplicano i codici di errore di sistema sono stati modificati in FACILITY WIN32 e quelli che si sovrappongono \_ rimangono in FACILITY \_ NULL. I **valori HRESULT** comuni e i relativi valori sono elencati nella tabella seguente.



| HRESULT                    | Valore                 | Descrizione                                                                                                                                        |
|----------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| E \_ ABORT<br/>        | 0x80004004<br/> | L'operazione è stata interrotta a causa di un errore non specificato.<br/>                                                                              |
| E \_ ACCESSO NEGATO<br/> | 0x80070005<br/> | Errore generale di accesso negato.<br/>                                                                                                          |
| E \_ FAIL<br/>         | 0x80004005<br/> | Si è verificato un errore non specificato.<br/>                                                                                                    |
| E \_ HANDLE<br/>       | 0x80070006<br/> | È stato usato un handle non valido.<br/>                                                                                                             |
| E \_ INVALIDARG<br/>   | 0x80070057<br/> | Uno o più argomenti non sono validi.<br/>                                                                                                      |
| E \_ NOINTERFACE<br/>  | 0x80004002<br/> | Il [**metodo QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) non riconosce l'interfaccia richiesta. L'interfaccia non è supportata.<br/> |
| E \_ NOTIMPL<br/>      | 0x80004001<br/> | Il metodo non è implementato.<br/>                                                                                                          |
| E \_ OUTOFMEMORY<br/>  | 0x8007000E<br/> | Il metodo non è riuscito ad allocare la memoria necessaria.<br/>                                                                                         |
| E \_ IN SOSPESO<br/>      | 0x8000000A<br/> | I dati necessari per completare l'operazione non sono ancora disponibili.<br/>                                                                      |
| PUNTATORE \_ E<br/>      | 0x80004003<br/> | È stato usato un puntatore non valido.<br/>                                                                                                            |
| E \_ UNEXPECTED<br/>   | 0x8000FFFF<br/> | Si è verificato un errore irreversibile.<br/>                                                                                                    |
| S \_ FALSE<br/>        | 0x00000001<br/> | Il metodo ha avuto esito positivo e ha restituito il valore **booleano FALSE.**<br/>                                                                          |
| S \_ OK<br/>           | 0x00000000<br/> | Il metodo è riuscito. Se è previsto un valore restituito booleano, il valore restituito è **TRUE.**<br/>                                            |



 

## <a name="network-errors"></a>Errori di rete

Se le prime quattro cifre del codice di errore sono 8007, ciò indica un errore di sistema o di rete. È possibile usare il **comando net** per decodificare questi tipi di errori. Per decodificare l'errore, convertire innanzitutto le ultime quattro cifre del codice di errore esadecimale in decimali. Quindi, al prompt dei comandi digitare quanto segue, dove il codice decimale viene sostituito con il valore restituito che si vuole decodificare:

**net helpmsg <** _decimal \_ code_*_>_*

Il comando net restituisce una descrizione dell'errore. Ad esempio, se COM restituisce l'errore 8007054B, convertire 054B in decimal (1355). Digitare quindi quanto segue:

**net helpmsg 1355**

Il comando net restituisce la descrizione dell'errore: "Il dominio specificato non esiste".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> </dl>

 

 





