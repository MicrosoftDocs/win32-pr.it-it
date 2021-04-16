---
title: Identificatori di proprietà riservati
description: Gli identificatori di proprietà riservate non possono essere utilizzati come identificatori di proprietà (ID). È possibile utilizzare qualsiasi identificatore di proprietà (ID) tranne 0, 1 e qualsiasi valore maggiore o uguale a, 0x80000000. Questi valori di identificatore di proprietà sono riservati per l'utilizzo da applicazioni.
ms.assetid: d313a7b1-4cac-41f8-ba38-bf9cfaeb9d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a16a8e232a31864a402b01033a829183105905c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473286"
---
# <a name="reserved-property-identifiers"></a>Identificatori di proprietà riservati

Gli identificatori di proprietà riservate non possono essere utilizzati come identificatori di proprietà (ID). È possibile utilizzare qualsiasi identificatore di proprietà (ID) tranne 0, 1 e qualsiasi valore maggiore o uguale a, 0x80000000. Questi valori di identificatore di proprietà sono riservati per l'utilizzo da applicazioni.

La tabella seguente elenca gli ID di proprietà riservati e la descrizione dell'ID di proprietà riservato.



| ID proprietà riservata | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                    | Riservato per la creazione di un [dizionario nome visualizzato del set di proprietà](property-set-display-name-dictionary.md)facoltativo. Ciò consente agli utenti del set di proprietà di aggiungere significato alle proprietà, oltre a quelle fornite dall'indicatore del tipo.                                                                                                                                                                                                                                                                                                                                                                |
| 1                    | Riservato come indicatore della tabella codici (Windows) o dello script (Macintosh) da usare per l'interpretazione delle stringhe nel set di proprietà.<br/> Tutti i valori stringa nel set di proprietà devono essere archiviati con la stessa tabella codici. Il valore del sistema operativo di origine nell'intestazione del set di proprietà (PROPERTYSETHEADER::d wOSVer) determina se l'indicatore della tabella codici corrisponde a una tabella codici di Windows o a uno script Macintosh.<br/>                                                                                                                                                        |
| 0x80000000           | Riservato come indicazione delle impostazioni locali per le quali viene scritto il set di proprietà.<br/> Le impostazioni locali predefinite per un set di proprietà sono le impostazioni locali predefinite del sistema (impostazioni locali del \_ sistema \_ ). Per ulteriori informazioni sulle impostazioni locali \_ \_ del sistema, vedere API Win32. Il valore predefinito viene utilizzato nel caso in cui l'indicatore delle impostazioni locali non esista nel set di proprietà.<br/>                                                                                                                                                                                                                        |
| 0x80000003           | Riservato come indicatore dei comportamenti del set di proprietà. Questo valore ID di proprietà è un \_ UI4 VT e inizia con un tipo di dati **DWORD** che contiene il valore VT \_ UI4 seguito da un valore **DWORD** che indica il comportamento del set di proprietà.<br/> Attualmente, l'unico bit in questo valore definito è il bit di ordine inferiore (0x1). Se questo bit è impostato, indica che i nomi dei set di proprietà, indicati dalla proprietà ID 0, devono essere considerati sensibili alla distinzione tra maiuscole e minuscole. Se questo bit non è impostato o se la proprietà Behavior (ID 0x80000003) non esiste, i nomi devono essere considerati senza distinzione tra maiuscole e minuscole.<br/> |
| 0xFFFFFFFF           | Riservato per la praticità della programmabilità. Non dovrebbe mai essere visualizzato in un set di proprietà serializzate.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Gli identificatori di proprietà con il set di bit elevato (ovvero i valori negativi) sono riservati per un uso futuro da parte di Microsoft.

Delle proprietà riservate, quelle con valori ID nell'intervallo compreso tra 0x80000000 e 0xBFFFFFFF sono considerate di sola lettura dalle implementazioni che non ne comprendono il significato. Se, ad esempio, un'implementazione non è in grado di comprendere il significato della proprietà 0x80000000, deve consentire la lettura, ma non la scrittura o l'eliminazione della proprietà. Tale implementazione deve consentire la lettura, la scrittura o l'eliminazione di una proprietà nell'intervallo compreso tra 0xC0000000 e 0xFFFFFFFE. L'ID di proprietà 0xFFFFFFFF è un valore riservato e non deve mai essere visualizzato in un set di proprietà serializzato.

## <a name="property-set-locale"></a>Impostazioni locali set di proprietà

Le applicazioni possono scegliere di supportare le impostazioni locali o utilizzare il comportamento predefinito. È consigliabile che le applicazioni consentano agli utenti di specificare le impostazioni locali di lavoro. Tali applicazioni devono scrivere l'identificatore delle impostazioni locali specificato dall'utente nella proprietà. Le applicazioni che usano le impostazioni locali predefinite dell'utente ( \_ impostazione predefinita dell'utente locale \_ ) devono scrivere l'identificatore delle impostazioni locali predefinito dell'utente nella proprietà. Per ulteriori informazioni sulle impostazioni locali \_ dell'utente \_ , vedere l'API Win32.

> [!Note]  
> Se l'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) viene utilizzata per creare un set di proprietà, le impostazioni locali predefinite dell'utente vengono scritte automaticamente come indicatore delle impostazioni locali.

 

Le applicazioni devono anche gestire il caso di un oggetto esterno, ovvero una delle impostazioni locali dell'applicazione, le impostazioni locali dell'utente o le impostazioni locali del sistema.

La proprietà dell'indicatore delle impostazioni locali è di tipo VT \_ U14 e pertanto è costituita da un **valore DWORD** che contiene VT \_ U14, seguito da un **valore DWORD** contenente l'identificatore delle impostazioni locali (LCID), come definito nell'API Win32.

## <a name="code-page-indicator"></a>Indicatore tabella codici

Quando un'applicazione che non è l'autore di un set di proprietà modifica una proprietà di tipo stringa nel set, deve esaminare l'indicatore della tabella codici ed eseguire una delle azioni seguenti:

-   Scrivere la stringa nel formato specificato dall'indicatore della tabella codici.
-   Sostituire e riscrivere per modificare la tabella codici.

Se un'applicazione non è in grado di riconoscere questo indicatore, non deve modificare la proprietà. Tutti gli autori dei set di proprietà devono scrivere un indicatore della tabella codici; Tuttavia, se l'indicatore della tabella codici non è presente, è necessario che venga utilizzata la tabella codici prevalente nel computer del lettore.

> [!Note]  
> Se l'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) viene utilizzata per creare un set di proprietà, l'indicatore della tabella codici viene scritto automaticamente.

 

I valori possibili per la tabella codici sono forniti nell'API Win32 (per altre informazioni, vedere la funzione [**GetACP**](/windows/desktop/api/winnls/nf-winnls-getacp) ) e *all'interno del volume di Macintosh VI*, pagine 14-111. Queste risorse potrebbero non essere disponibili in alcune lingue e paesi. Ad esempio, la tabella codici ANSI viene rappresentata da 0x04E4 (1252 in decimale) mentre la tabella codici per Unicode è 0x04B0 (1200 in decimale).

Si consiglia di utilizzare la tabella codici Unicode quando possibile e di utilizzare VT \_ LPWSTR anziché VT \_ LPSTR per evitare conversioni Unicode <-> Unicode durante l'archiviazione e il recupero. L'uso della stessa tabella codici per tutti i set di proprietà è l'unico modo per ottenere i set di proprietà interoperativi su base mondiale. Nella tabella codici Unicode o non Unicode, tenere presente che il conteggio all'inizio di un VT \_ LPSTR o VT \_ BSTR è un conteggio di **byte** e non un conteggio di **caratteri** . Questo numero di byte include uno o due byte zero alla fine della stringa, ovvero il carattere di terminazione **null** della stringa.

ID proprietà 1 è un \_ tipo VT I2 e inizia con un valore **DWORD** che contiene il valore VT \_ I2 seguito da un valore **short** che indica la tabella codici.

 

