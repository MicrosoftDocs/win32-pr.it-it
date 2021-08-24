---
description: Implementazione delle estensioni della finestra delle proprietà
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementazione delle estensioni della finestra delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b4f74559176ecc0c411f75e7ca630db152a51109f09ecdca47a62d0113e70c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590281"
---
# <a name="implementing-property-sheet-extensions"></a>Implementazione delle estensioni della finestra delle proprietà

L'estensione dello spazio dei nomi WPD supporta le finestre delle proprietà estendibili. Si tratta delle finestre di dialogo delle proprietà visualizzate quando un utente fa clic con il pulsante destro del mouse su un oggetto, ad esempio un file o una cartella, e seleziona **Proprietà**. Alcune applicazioni WPD sfruttano queste finestre delle proprietà estendibili per visualizzare le proprietà per il contenuto sul lato dispositivo (o gli oggetti che risiedono nel dispositivo).

Le finestre delle proprietà estendibili sono supportate dalle interfacce descritte nella tabella seguente. Per altre informazioni su una di queste interfacce, vedere l'SDK Windows.



| Interfaccia           | Descrizione                                                                  |
|---------------------|------------------------------------------------------------------------------|
| Idataobject         | Usato per passare la matrice PIDL del menu di scelta rapida al gestore del menu di scelta rapida.      |
| IPropertySetStorage | Questa interfaccia viene usata per recuperare le proprietà WPD per l'oggetto specificato.      |
| IPropertyStorage    | Questa interfaccia viene usata anche per recuperare le proprietà WPD per l'oggetto specificato. |
| IShellExtInit       | Inizializza le estensioni Windows Vista shell per il menu di scelta rapida.         |
| IShellPropSheetExt  | Supporta l'aggiunta di estensioni della finestra delle proprietà.                              |



 

Le finestre delle proprietà per WPD vengono implementate come qualsiasi altra finestra delle proprietà in Windows Vista. Se è già stato implementato un gestore della finestra delle proprietà, è possibile modificare il codice esistente in modo che supporti il contenuto sul lato dispositivo. Se non è mai stato creato un gestore del menu di scelta rapida, vedere l'argomento Creazione di gestori della finestra delle proprietà in Windows SDK.

I due punti in cui un gestore della finestra delle proprietà WPD è diverso da qualsiasi altro gestore si trova nella registrazione del gestore e nel supporto del contenuto sul lato dispositivo.

 

 



