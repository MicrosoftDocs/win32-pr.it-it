---
description: Le applicazioni possono recuperare e impostare la data e l'ora di creazione, dell'Ultima modifica o dell'ultimo accesso di un file tramite le funzioni GetFileTime ha provocato e SetFileTime.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Impostazione e recupero del timestamp di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34735994dd3017662f517a8c0a57be1d5c0e3096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226262"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a>Impostazione e recupero del timestamp di un file

Le applicazioni possono recuperare e impostare la data e l'ora di creazione, dell'Ultima modifica o dell'ultimo accesso di un file tramite le funzioni [**GetFileTime ha provocato**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) e [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) . Per ulteriori informazioni, vedere [file Times](/windows/desktop/SysInfo/file-times).

> [!Note]  
> Non tutti i file System possono registrare i tempi di creazione e di ultimo accesso e non tutti i file System li registrano nello stesso modo. Ad esempio, in file system FAT, l'ora di creazione ha una risoluzione di 10 millisecondi, l'ora di scrittura ha una risoluzione di 2 secondi e l'ora di accesso ha una risoluzione di 1 giorno (in realtà, la data di accesso). Il file system NTFS ritarda l'aggiornamento all'ora dell'ultimo accesso per un file fino a un'ora dopo l'ultimo accesso.

 

 

 
