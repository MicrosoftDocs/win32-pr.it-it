---
title: Strategie di gestione degli errori
description: Strategie di gestione degli errori
ms.assetid: 8d03ede8-0661-43dc-adaf-3c1f5fc1687e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c594a8b1e5baf0eab3d928b8f1b861b7f0160d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "104472211"
---
# <a name="error-handling-strategies"></a>Strategie di gestione degli errori

Poiché i metodi di interfaccia sono virtuali, non è possibile che un chiamante conosca il set completo di valori che possono essere restituiti da una sola chiamata. Un'implementazione di un metodo può restituire cinque valori; un altro può restituire otto.

La documentazione elenca i valori comuni che possono essere restituiti per ogni metodo. Questi sono i valori che devono essere verificati e gestiti nel codice in quanto hanno significati speciali. È possibile che vengano restituiti altri valori, ma poiché non sono significativi, non è necessario scrivere codice speciale per gestirli. Un controllo semplice per zero o un valore diverso da zero è adeguato.

## <a name="hresult-values"></a>Valori HRESULT

Il valore restituito di funzioni e metodi COM è un **HRESULT**. I valori di alcuni HRESULT sono stati modificati in COM per eliminare tutte le duplicazioni e la sovrapposizione con i codici di errore di sistema. I codici di errore di sistema duplicati sono stati modificati per la funzionalità \_ Win32 e quelli che si sovrappongono rimangono nella struttura \_ null. Nella tabella seguente sono elencati i valori **HRESULT** comuni e i relativi valori.



| HRESULT                    | Valore                 | Descrizione                                                                                                                                        |
|----------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Interrompi E<br/>        | 0x80004004<br/> | L'operazione è stata interrotta a causa di un errore non specificato.<br/>                                                                              |
| E \_ AccessDenied<br/> | 0x80070005<br/> | Errore generale di accesso negato.<br/>                                                                                                          |
| E \_ non riescono<br/>         | 0x80004005<br/> | Si è verificato un errore non specificato.<br/>                                                                                                    |
| \_handle E<br/>       | 0x80070006<br/> | È stato usato un handle non valido.<br/>                                                                                                             |
| E \_ INVALIDARG<br/>   | 0x80070057<br/> | Uno o più argomenti non sono validi.<br/>                                                                                                      |
| E \_ NOinterface<br/>  | 0x80004002<br/> | Il metodo [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) non ha riconosciuto l'interfaccia richiesta. L'interfaccia non è supportata.<br/> |
| E \_ NOTIMPL<br/>      | 0x80004001<br/> | Il metodo non è implementato.<br/>                                                                                                          |
| E \_ OutOfMemory<br/>  | 0x8007000E<br/> | Il metodo non è riuscito ad allocare la memoria necessaria.<br/>                                                                                         |
| E \_ in sospeso<br/>      | 0x8000000A<br/> | I dati necessari per il completamento dell'operazione non sono ancora disponibili.<br/>                                                                      |
| \_puntatore E<br/>      | 0x80004003<br/> | È stato utilizzato un puntatore non valido.<br/>                                                                                                            |
| E \_ imprevisto<br/>   | 0x8000FFFF<br/> | Si è verificato un errore irreversibile.<br/>                                                                                                    |
| S \_ false<br/>        | 0x00000001<br/> | Il metodo ha avuto esito positivo e ha restituito il valore booleano **false**.<br/>                                                                          |
| \_OK<br/>           | 0x00000000<br/> | Il metodo è riuscito. Se è previsto un valore booleano restituito, il valore restituito è **true**.<br/>                                            |



 

## <a name="network-errors"></a>Errori di rete

Se le prime quattro cifre del codice di errore sono 8007, indica un errore di sistema o di rete. È possibile utilizzare il comando **net** per decodificare questi tipi di errori. Per decodificare l'errore, convertire innanzitutto le ultime quattro cifre del codice di errore esadecimale in decimali. Quindi, al prompt dei comandi, digitare quanto segue, dove il codice decimale viene sostituito con il valore restituito che si vuole decodificare:

**NET HELPMSG <***\_ codice decimale***>**

Il comando NET restituisce una descrizione dell'errore. Se, ad esempio, COM restituisce l'errore 8007054B, convertire 054B in Decimal (1355). Digitare quindi quanto segue:

**NET HELPMSG 1355**

Il comando NET restituisce la descrizione dell'errore: "il dominio specificato non esiste".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> </dl>

 

 





