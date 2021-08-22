---
description: Le applicazioni possono recuperare e impostare la data e l'ora di creazione, ultima modifica o ultimo accesso di un file usando le funzioni GetFileTime e SetFileTime.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Impostazione e recupero del timestamp di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e98bd87ae8224ecbebc46e5f9d0ed71ad3522097fb865afc0d16e53a828812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015129"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a>Impostazione e recupero del timestamp di un file

Le applicazioni possono recuperare e impostare la data e l'ora di creazione, ultima modifica o ultimo accesso di un file usando le [**funzioni GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) [**e SetFileTime.**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) Per altre informazioni, vedere [Orari dei file.](/windows/desktop/SysInfo/file-times)

> [!Note]  
> Non tutti i file system possono registrare le ore di creazione e dell'ultimo accesso e non tutti i file system li registrano nello stesso modo. Ad esempio, in FAT file system l'ora di creazione ha una risoluzione di 10 millisecondi, l'ora di scrittura ha una risoluzione di 2 secondi e l'ora di accesso ha una risoluzione di 1 giorno (in realtà, la data di accesso). Il file system NTFS file system l'aggiornamento all'ora dell'ultimo accesso per un file fino a un'ora dopo l'ultimo accesso.

 

 

 
