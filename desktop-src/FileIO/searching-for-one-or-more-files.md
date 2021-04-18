---
description: Un'applicazione può eseguire ricerche nella directory corrente per tutti i nomi di file che corrispondono a un modello specificato usando le funzioni FindFirstFile, FindFirstFileEx, FindNextFile e FindClose.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Ricerca di uno o più file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308215"
---
# <a name="searching-for-one-or-more-files"></a>Ricerca di uno o più file

Un'applicazione può eseguire ricerche nella directory corrente per tutti i nomi di file che corrispondono a un modello specificato usando le funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) . Il criterio deve essere un nome di file valido e può includere caratteri jolly.

Le funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) creano handle che **FindFirstFileEx** USA per cercare altri file con lo stesso modello. Tutte le funzioni restituiscono informazioni sul file trovato. Queste informazioni includono il nome del file, la dimensione, gli attributi e l'ora.

La funzione [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) consente anche a un'applicazione di cercare i file in base a criteri di ricerca aggiuntivi. La funzione può limitare le ricerche ai nomi dei dispositivi o dei nomi di directory.

La funzione [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) Elimina gli handle creati da [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).

Un'applicazione può cercare un singolo file in un percorso specifico usando la funzione [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) .

 

 
