---
description: Ogni reparse point ha un Tag Identifier che consente di distinguere in modo efficiente tra i diversi tipi di punti di analisi, senza dover esaminare i dati definiti dall'utente nel reparse point.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Tag di reparse point
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315928"
---
# <a name="reparse-point-tags"></a>Tag di reparse point

Ogni reparse point ha un Tag Identifier che consente di distinguere in modo efficiente tra i diversi tipi di punti di analisi, senza dover esaminare i dati definiti dall'utente nel reparse point. Il sistema usa un set di tag predefiniti e un intervallo di tag riservati per Microsoft. Se si usa uno dei tag riservati quando si imposta un punto di analisi, l'operazione non riesce. I tag non inclusi in questi intervalli non sono riservati e sono disponibili per l'applicazione.

Quando si imposta un reparse point, è necessario contrassegnare i dati da inserire nel punto di analisi. Una volta stabilita la reparse point, una nuova operazione set ha esito negativo se il tag per i nuovi dati non corrisponde al tag per i dati esistenti. Se i tag corrispondono, l'operazione di impostazione sovrascrive il reparse point esistente.

Per recuperare il tag reparse point, usare la funzione [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) . Se il membro **dwFileAttributes** include l' **attributo \_ file \_ reparse \_ Point** , il membro **dwReserved0** specifica il reparse point.

## <a name="tag-contents"></a>Contenuto del tag

I tag di reparse vengono archiviati come valori **DWORD** . I bit definiscono determinati attributi, come illustrato nel diagramma seguente.

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

I 16 bit bassi determinano il tipo di reparse point. I 16 bit alti hanno 12 bit riservati per un uso futuro e 4 bit che indicano attributi specifici dei tag e i dati rappresentati dal punto di analisi. Nella tabella seguente vengono descritti questi bit.



| bit | Descrizione                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| M   | Microsoft bit. Se questo bit è impostato, il tag è di proprietà di Microsoft. Tutti gli altri tag devono usare zero per questo bit. |
| R   | Riservati deve essere zero per tutti i tag non Microsoft.                                                           |
| N   | Nome surrogato bit. Se questo bit è impostato, il file o la directory rappresenta un'altra entità denominata nel sistema. |



 

Sono disponibili le macro seguenti per semplificare il test dei tag:

-   [**IsReparseTagMicrosoft**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [**IsReparseTagNameSurrogate**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

Ogni macro restituisce un valore diverso da zero se il bit associato è impostato.

Di seguito sono riportati i valori di tag di reparse predefiniti di Microsoft; sono definiti in WinNT. h:

-   **IO_REPARSE_TAG_AF_UNIX**
-   **IO_REPARSE_TAG_APPEXECLINK**
-   **IO_REPARSE_TAG_CLOUD**
-   **IO_REPARSE_TAG_CLOUD_1**
-   **IO_REPARSE_TAG_CLOUD_2**
-   **IO_REPARSE_TAG_CLOUD_3**
-   **IO_REPARSE_TAG_CLOUD_4**
-   **IO_REPARSE_TAG_CLOUD_5**
-   **IO_REPARSE_TAG_CLOUD_6**
-   **IO_REPARSE_TAG_CLOUD_7**
-   **IO_REPARSE_TAG_CLOUD_8**
-   **IO_REPARSE_TAG_CLOUD_9**
-   **IO_REPARSE_TAG_CLOUD_A**
-   **IO_REPARSE_TAG_CLOUD_B**
-   **IO_REPARSE_TAG_CLOUD_C**
-   **IO_REPARSE_TAG_CLOUD_D**
-   **IO_REPARSE_TAG_CLOUD_E**
-   **IO_REPARSE_TAG_CLOUD_F**
-   **IO_REPARSE_TAG_CLOUD_MASK**
-   **IO_REPARSE_TAG_CSV**
-   **IO_REPARSE_TAG_DEDUP**
-   **IO_REPARSE_TAG_DFS**
-   **IO_REPARSE_TAG_DFSR**
-   **IO_REPARSE_TAG_FILE_PLACEHOLDER**
-   **IO_REPARSE_TAG_GLOBAL_REPARSE**
-   **IO_REPARSE_TAG_HSM**
-   **IO_REPARSE_TAG_HSM2**
-   **IO_REPARSE_TAG_MOUNT_POINT**
-   **IO_REPARSE_TAG_NFS**
-   **IO_REPARSE_TAG_ONEDRIVE**
-   **IO_REPARSE_TAG_PROJFS**
-   **IO_REPARSE_TAG_PROJFS_TOMBSTONE**
-   **IO_REPARSE_TAG_SIS**
-   **IO_REPARSE_TAG_STORAGE_SYNC**
-   **IO_REPARSE_TAG_SYMLINK**
-   **IO_REPARSE_TAG_UNHANDLED**
-   **IO_REPARSE_TAG_WCI**
-   **IO_REPARSE_TAG_WCI_1**
-   **IO_REPARSE_TAG_WCI_LINK**
-   **IO_REPARSE_TAG_WCI_LINK_1**
-   **IO_REPARSE_TAG_WCI_TOMBSTONE**
-   **IO_REPARSE_TAG_WIM**
-   **IO_REPARSE_TAG_WOF**

Per garantire l'univocità dei tag, Microsoft fornisce un meccanismo per distribuire i nuovi tag. Per ulteriori informazioni, vedere il [Kit Installable File System (IFS)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).

 

 



