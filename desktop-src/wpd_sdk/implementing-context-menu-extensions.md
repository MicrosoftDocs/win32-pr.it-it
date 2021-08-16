---
description: Implementazione delle estensioni del menu di scelta rapida
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementazione delle estensioni del menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090f37b4cf77f9508e8c149ef6389297c561e1a4e574ef767f3a5e5c7e07fe05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194684"
---
# <a name="implementing-context-menu-extensions"></a>Implementazione delle estensioni del menu di scelta rapida

L'estensione dello spazio dei nomi WPD supporta menu di scelta rapida o contesto estendibile. Si tratta dei menu che vengono visualizzati quando un utente fa clic con il pulsante destro del mouse su un oggetto, ad esempio un file o una cartella. Alcune applicazioni WPD trarranno vantaggio da questi menu estendibili per supportare le operazioni sul contenuto sul lato dispositivo (o sugli oggetti che risiedono nel dispositivo).

I menu di scelta rapida estendibile sono supportati dalle interfacce descritte nella tabella seguente. Per altre informazioni su una di queste interfacce, vedere Windows SDK.



| Interfaccia           | Descrizione                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| IContextMenu        | La Windows Vista Shell chiama i metodi in questa interfaccia per creare o unire il nuovo menu di scelta rapida con l'oggetto specificato. |
| Idataobject         | Usato per passare la matrice PIDL del menu di scelta rapida al gestore del menu di scelta rapida.                                                    |
| IPropertySetStorage | Questa interfaccia viene usata per recuperare le proprietà WPD per l'oggetto specificato.                                                    |
| IPropertyStorage    | Questa interfaccia viene usata anche per recuperare le proprietà WPD per l'oggetto specificato.                                               |
| IShellExtInit       | Inizializza le estensioni Windows Vista Shell per il menu di scelta rapida.                                                       |
| Istream             | Da ottenere.                                                                                                            |



 

I menu di scelta rapida per la WPD vengono implementati come qualsiasi altro menu di scelta rapida in Windows Vista. Se è già stato implementato un gestore del menu di scelta rapida, è possibile modificare il codice esistente in modo che supporti il contenuto sul lato dispositivo. Se non è mai stato creato un gestore del menu di scelta rapida, vedere l'argomento Creazione di gestori del menu di scelta rapida in Windows SDK.

I due punti in cui un gestore del menu di scelta rapida WPD è diverso da qualsiasi altro gestore si trova nella registrazione del gestore e nel supporto del contenuto sul lato dispositivo.

 

 



