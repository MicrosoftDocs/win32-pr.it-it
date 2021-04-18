---
description: Implementazione delle estensioni della finestra delle proprietà
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementazione delle estensioni della finestra delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319088"
---
# <a name="implementing-property-sheet-extensions"></a>Implementazione delle estensioni della finestra delle proprietà

L'estensione dello spazio dei nomi WPD supporta le finestre delle proprietà estendibili. Si tratta delle finestre di dialogo delle proprietà visualizzate quando un utente fa clic con il pulsante destro del mouse su un oggetto, ad esempio un file o una cartella, e seleziona **Proprietà**. Alcune applicazioni WPD sfruttano i vantaggi di queste finestre delle proprietà estendibili per visualizzare le proprietà del contenuto sul lato dispositivo o gli oggetti che risiedono nel dispositivo.

Le finestre delle proprietà estendibili sono supportate dalle interfacce descritte nella tabella seguente. Per ulteriori informazioni su una di queste interfacce, vedere la Windows SDK.



| Interfaccia           | Descrizione                                                                  |
|---------------------|------------------------------------------------------------------------------|
| IDataObject         | Utilizzato per passare la matrice PIDL del menu di scelta rapida al gestore del menu di scelta rapida.      |
| IPropertySetStorage | Questa interfaccia viene utilizzata per recuperare le proprietà WPD per l'oggetto specificato.      |
| IPropertyStorage    | Questa interfaccia viene utilizzata anche per recuperare le proprietà WPD per l'oggetto specificato. |
| IShellExtInit       | Inizializza le estensioni della shell di Windows Vista per il menu di scelta rapida.         |
| IShellPropSheetExt  | Supporta l'aggiunta di estensioni della finestra delle proprietà.                              |



 

Le finestre delle proprietà per WPD vengono implementate come qualsiasi altra finestra delle proprietà in Windows Vista. Se è già stato implementato un gestore della finestra delle proprietà, è possibile modificare il codice esistente in modo che supporti il contenuto lato dispositivo. Se non è mai stato creato un gestore di menu di scelta rapida, vedere l'argomento Creazione di gestori della finestra delle proprietà nell'Windows SDK.

I due punti in cui un gestore della finestra delle proprietà di WPD è diverso da qualsiasi altro gestore si trova nella registrazione del gestore e il supporto del contenuto sul lato dispositivo.

 

 



