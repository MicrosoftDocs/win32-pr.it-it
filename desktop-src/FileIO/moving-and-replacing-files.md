---
description: Considerazioni per lo spostamento e la sostituzione dei file tramite le funzioni CopyFileEx, CreateFile, ReplaceFile e MoveFileEx.
ms.assetid: 4872af0d-42e8-4576-9aa9-4b8671375f2e
title: Trasferimento e sostituzione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d7f08d2bd8d07645076620e839d7d12f5969502
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320832"
---
# <a name="moving-and-replacing-files"></a>Trasferimento e sostituzione di file

Prima di poter eseguire un'operazione di copia, è necessario chiudere o aprire il file di origine solo per la lettura. Nessun thread può disporre del file di origine aperto per la scrittura. Per copiare un file esistente in un nuovo file, usare la funzione [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) o [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) . Le applicazioni possono specificare se **CopyFile** e **CopyFileEx** hanno esito negativo se il file di destinazione esiste già. Se il file di destinazione esiste ed è aperto, è necessario che sia stato aperto con le autorizzazioni di condivisione applicabili. Per ulteriori informazioni, vedere [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

La funzione [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) consente anche a un'applicazione di specificare l'indirizzo di una funzione di callback (vedere [**CopyProgressRoutine**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)) che viene chiamato ogni volta che è stata copiata un'altra parte del file. L'applicazione può utilizzare queste informazioni per visualizzare un indicatore che indica il numero totale di byte copiati come percentuale delle dimensioni totali del file.

La funzione [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) sostituisce un file con un altro file, con l'opzione di creare una copia di backup del file originale. La funzione conserva gli attributi del file originale, ad esempio l'ora di creazione, gli ACL e l'attributo di crittografia.

Prima che un'applicazione possa spostarla, è necessario chiudere anche un file. Le funzioni [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile) e [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) copiano un file esistente in un nuovo percorso ed Elimina l'originale.

La funzione [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) consente anche a un'applicazione di specificare come spostare il file. La funzione può sostituire un file esistente, spostare un file tra volumi e ritardare lo spostamento del file fino al riavvio del sistema operativo.

 

 



