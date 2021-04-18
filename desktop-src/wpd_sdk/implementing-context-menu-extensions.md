---
description: Implementazione delle estensioni del menu di scelta rapida
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementazione delle estensioni del menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312466"
---
# <a name="implementing-context-menu-extensions"></a>Implementazione delle estensioni del menu di scelta rapida

L'estensione dello spazio dei nomi WPD supporta i menu di scelta rapida (o collegamento) estensibile. Questi sono i menu che vengono visualizzati quando un utente fa clic con il pulsante destro del mouse su un oggetto, ad esempio un file o una cartella. Alcune applicazioni WPD sfruttano i vantaggi di questi menu estendibili per supportare operazioni sul contenuto sul lato dispositivo o sugli oggetti che risiedono nel dispositivo.

I menu di scelta rapida estendibili sono supportati dalle interfacce descritte nella tabella seguente. Per ulteriori informazioni su una di queste interfacce, vedere la Windows SDK.



| Interfaccia           | Descrizione                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| IContextMenu        | La shell di Windows Vista chiama i metodi in questa interfaccia per creare o unire il nuovo menu di scelta rapida con l'oggetto specificato. |
| IDataObject         | Utilizzato per passare la matrice PIDL del menu di scelta rapida al gestore del menu di scelta rapida.                                                    |
| IPropertySetStorage | Questa interfaccia viene utilizzata per recuperare le proprietà WPD per l'oggetto specificato.                                                    |
| IPropertyStorage    | Questa interfaccia viene utilizzata anche per recuperare le proprietà WPD per l'oggetto specificato.                                               |
| IShellExtInit       | Inizializza le estensioni della shell di Windows Vista per il menu di scelta rapida.                                                       |
| IStream             | Da fornire.                                                                                                            |



 

I menu di scelta rapida per WPD vengono implementati come qualsiasi altro menu di scelta rapida in Windows Vista. Se è già stato implementato un gestore di menu di scelta rapida, è possibile modificare il codice esistente in modo che supporti il contenuto lato dispositivo. Se non è mai stato creato un gestore di menu di scelta rapida, vedere l'argomento Creazione di gestori di menu di scelta rapida nella Windows SDK.

I due punti in cui il gestore del menu di scelta rapida WPD differisce da qualsiasi altro gestore si trova nella registrazione del gestore e il supporto del contenuto sul lato dispositivo.

 

 



