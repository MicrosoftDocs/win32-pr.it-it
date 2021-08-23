---
title: Identificatori di proprietà riservate
description: Gli identificatori di proprietà riservati non possono essere usati come identificatori di proprietà (ID). Qualsiasi identificatore di proprietà (ID) può essere usato ad eccezione di 0, 1 e qualsiasi valore maggiore o uguale a 0x80000000. Questi valori degli identificatori di proprietà sono riservati per l'uso da parte delle applicazioni.
ms.assetid: d313a7b1-4cac-41f8-ba38-bf9cfaeb9d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05053fd2a31a5e8ceec63420e74884484abef12d44dcfe3e7023c81b5e67e27a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683061"
---
# <a name="reserved-property-identifiers"></a>Identificatori di proprietà riservate

Gli identificatori di proprietà riservati non possono essere usati come identificatori di proprietà (ID). Qualsiasi identificatore di proprietà (ID) può essere usato ad eccezione di 0, 1 e qualsiasi valore maggiore o uguale a 0x80000000. Questi valori degli identificatori di proprietà sono riservati per l'uso da parte delle applicazioni.

Nella tabella seguente sono elencati gli ID delle proprietà riservate e la descrizione dell'ID proprietà riservato.



| ID proprietà riservata | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                    | Riservato per la creazione di un dizionario [dei nomi visualizzati del set di proprietà facoltativo.](property-set-display-name-dictionary.md) In questo modo gli utenti dei set di proprietà possono associare il significato alle proprietà, oltre a quelle fornite dall'indicatore di tipo.                                                                                                                                                                                                                                                                                                                                                                |
| 1                    | Riservato come indicatore della tabella codici (Windows) o dello script (Macintosh) da usare per interpretare le stringhe nel set di proprietà.<br/> Tutti i valori stringa nel set di proprietà devono essere archiviati con la stessa tabella codici. Il valore del sistema operativo di origine nell'intestazione del set di proprietà (PROPERTYSETHEADER::d wOSVer) determina se l'indicatore della tabella codici corrisponde a una tabella codici Windows o a uno script Macintosh.<br/>                                                                                                                                                        |
| 0x80000000           | Riservato come indicazione delle impostazioni locali per cui viene scritto il set di proprietà.<br/> Le impostazioni locali predefinite per un set di proprietà sono le impostazioni locali predefinite del sistema (IMPOSTAZIONI \_ LOCALI SYSTEM \_ DEFAULT). Per altre informazioni su LOCALE \_ SYSTEM \_ DEFAULT, vedere le API Win32. Il valore predefinito viene usato nel caso in cui l'indicatore delle impostazioni locali non esista nel set di proprietà.<br/>                                                                                                                                                                                                                        |
| 0x80000003           | Riservato come indicatore dei comportamenti del set di proprietà. Questo valore ID proprietà è un'interfaccia utente VT4 e inizia con un tipo di dati DWORD contenente il valore \_ VT UI4 seguito da un valore  DWORD che indica il comportamento del \_ set di proprietà. <br/> Attualmente, l'unico bit in questo valore definito è il bit di ordine basso (0x1). Se questo bit è impostato, indica che i nomi dei set di proprietà, indicati dall'ID proprietà 0, devono essere considerati con distinzione tra maiuscole e minuscole. Se questo bit non è impostato o se la proprietà di comportamento (ID 0x80000003) non esiste, i nomi devono essere considerati senza distinzione tra maiuscole e minuscole.<br/> |
| 0xffffffff           | Riservato per la praticità della programmabilità. Non deve mai essere visualizzato in un set di proprietà serializzato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Gli identificatori di proprietà con il set di bit alto (ovvero i valori negativi) sono riservati per un uso futuro da parte di Microsoft.

Tra le proprietà riservate, quelle con valori ID nell'intervallo da 0x80000000 a 0xBFFFFFFF sono considerate di sola lettura dalle implementazioni che non ne comprendono il significato. Ad esempio, se un'implementazione non comprende il significato della proprietà 0x80000000, deve consentire la lettura della proprietà, ma non la scrittura o l'eliminazione. Tale implementazione deve consentire a una proprietà nell'intervallo 0xC0000000 di 0xFFFFFFFE lettura, scrittura o eliminazione. L'ID 0xFFFFFFFF è un valore riservato e non deve mai essere visualizzato in un set di proprietà serializzato.

## <a name="property-set-locale"></a>Impostazioni locali del set di proprietà

Le applicazioni possono scegliere di supportare le impostazioni locali o usare il comportamento predefinito. È consigliabile che le applicazioni consentano agli utenti di specificare le impostazioni locali di lavoro. Tali applicazioni devono scrivere l'identificatore delle impostazioni locali specificato dall'utente nella proprietà . Le applicazioni che usano le impostazioni locali predefinite dell'utente (IMPOSTAZIONI LOCALI USER DEFAULT) devono scrivere l'identificatore delle impostazioni locali \_ \_ predefinite dell'utente nella proprietà . Per altre informazioni su LOCALE \_ USER \_ DEFAULT, vedere l'API Win32.

> [!Note]  
> Se si [**usa l'interfaccia IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per creare un set di proprietà, le impostazioni locali predefinite dell'utente vengono scritte automaticamente come indicatore delle impostazioni locali.

 

Le applicazioni devono anche gestire il caso di un oggetto esterno, ovvero quello in cui le impostazioni locali non sono le impostazioni locali dell'applicazione, le impostazioni locali dell'utente o le impostazioni locali del sistema.

La proprietà dell'indicatore delle impostazioni locali è di tipo VT U14 e pertanto è costituita da un valore DWORD che contiene VT U14, seguito da un valore DWORD contenente l'identificatore delle impostazioni locali (LCID), come definito \_ nell'API  \_ Win32. 

## <a name="code-page-indicator"></a>Indicatore tabella codici

Quando un'applicazione che non è l'autore di un set di proprietà modifica una proprietà di tipo stringa nel set, deve esaminare l'indicatore della tabella codici ed eseguire una delle azioni seguenti:

-   Scrivere la stringa nel formato specificato dall'indicatore della tabella codici.
-   Sostituire e riscrivere per modificare la tabella codici.

Se un'applicazione non riconosce questo indicatore, non deve modificare la proprietà . Tutti gli autori di set di proprietà devono scrivere un indicatore della tabella codici. Tuttavia, se l'indicatore della tabella codici non è presente, è necessario utilizzare la tabella codici prevalente nel computer del lettore.

> [!Note]  
> Se si [**usa l'interfaccia IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per creare un set di proprietà, l'indicatore della tabella codici viene scritto automaticamente.

 

I valori possibili per la tabella codici sono specificati nell'API Win32 (per altre informazioni, vedere la funzione [**GetACP)**](/windows/desktop/api/winnls/nf-winnls-getacp) e *inside Macintosh Volume VI*, pagine 14-111. Queste risorse potrebbero non essere disponibili in alcune lingue e paesi. Ad esempio, la tabella codici US ANSI è rappresentata da 0x04E4 (1252 in decimale) mentre la tabella codici per Unicode è 0x04B0 (1200 in decimale).

È consigliabile usare la tabella codici Unicode quando possibile e usare \_ VT LPWSTR anziché VT LPSTR per evitare \_ conversioni Unicode <-> multibyte durante l'archiviazione e il recupero. L'uso della stessa tabella codici per tutti i set di proprietà è l'unico modo per ottenere set di proprietà interoperabili su base globale. Nella tabella codici Unicode o non Unicode tenere presente che il conteggio all'inizio di un oggetto VT LPSTR o VT BSTR è un numero di byte e non un numero \_ \_ **di** caratteri.  Questo numero di byte include uno o due byte zero alla fine della stringa (terminatore **NULL** della stringa).

L'ID proprietà 1 è un tipo VT I2 e inizia con un valore DWORD che contiene il valore VT I2 seguito da un valore SHORT che indica \_ la tabella  \_ codici. 

 

