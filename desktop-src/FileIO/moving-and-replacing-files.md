---
description: Considerazioni per lo spostamento e la sostituzione di file tramite le funzioni CopyFileEx, CreateFile, Replacefile e MoveFileEx.
ms.assetid: 4872af0d-42e8-4576-9aa9-4b8671375f2e
title: Spostamento e sostituzione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c78085865006d1dfbbe322239c4704d215d038897b81d1f139d66d06f65bbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696011"
---
# <a name="moving-and-replacing-files"></a>Spostamento e sostituzione di file

Prima di poter eseguire un'operazione di copia, il file di origine deve essere chiuso o aperto solo per la lettura. Nessun thread può avere il file di origine aperto per la scrittura. Per copiare un file esistente in uno nuovo, usare la [**funzione CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) [**o CopyFileEx.**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) Le applicazioni possono specificare se **CopyFile** e **CopyFileEx hanno** esito negativo se il file di destinazione esiste già. Se il file di destinazione esiste ed è aperto, deve essere stato aperto con le autorizzazioni di condivisione applicabili. Per altre informazioni, vedere [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

La [**funzione CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) consente inoltre a un'applicazione di specificare l'indirizzo di una funzione di callback (vedere [**CopyProgressRoutine**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)) che viene chiamata ogni volta che viene copiata un'altra parte del file. L'applicazione può usare queste informazioni per visualizzare un indicatore che mostra il numero totale di byte copiati come percentuale delle dimensioni totali del file.

La [**funzione ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) sostituisce un file con un altro file, con la possibilità di creare una copia di backup del file originale. La funzione mantiene gli attributi del file originale, ad esempio l'ora di creazione, gli ACL e l'attributo di crittografia.

Un file deve essere chiuso anche prima che un'applicazione possa spostarlo. Le [**funzioni MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile) [**e MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) copiano un file esistente in un nuovo percorso ed eliminano l'originale.

La [**funzione MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) consente inoltre a un'applicazione di specificare come spostare il file. La funzione può sostituire un file esistente, spostare un file tra volumi e ritardare lo spostamento del file fino al riavvio del sistema operativo.

 

 



