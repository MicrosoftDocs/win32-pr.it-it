---
description: Ogni reparse point ha un tag identificatore in modo che sia possibile distinguere in modo efficiente tra i diversi tipi di reparse point, senza dover esaminare i dati definiti dall'utente nel reparse point.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Tag dei punti di analisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b31d4a1765266295b85c95c0955ae9c51faeb34ae07f3af48288a17a50f2166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015189"
---
# <a name="reparse-point-tags"></a>Tag dei punti di analisi

Ogni reparse point ha un tag identificatore in modo che sia possibile distinguere in modo efficiente tra i diversi tipi di reparse point, senza dover esaminare i dati definiti dall'utente nel reparse point. Il sistema usa un set di tag predefiniti e un intervallo di tag riservati a Microsoft. Se si usa uno dei tag riservati durante l'impostazione di un reparse point, l'operazione ha esito negativo. I tag non inclusi in questi intervalli non sono riservati e sono disponibili per l'applicazione.

Quando si imposta un reparse point, è necessario contrassegnare i dati da inserire nel reparse point. Dopo aver stabilito il reparse point, una nuova operazione set ha esito negativo se il tag per i nuovi dati non corrisponde al tag per i dati esistenti. Se i tag corrispondono, l'operazione set sovrascrive il reparse point esistente.

Per recuperare il tag del reparse point, usare la [**funzione FindFirstFile.**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) Se il **membro dwFileAttributes** include l'attributo **FILE ATTRIBUTE \_ \_ REPARSE \_ POINT,** il **membro dwReserved0** specifica il reparse point.

## <a name="tag-contents"></a>Contenuto dei tag

I tag di analisi vengono archiviati **come valori DWORD.** I bit definiscono determinati attributi, come illustrato nel diagramma seguente.

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

I 16 bit bassi determinano il tipo di reparse point. I 16 bit alti hanno 12 bit riservati per un uso futuro e 4 bit che indicano attributi specifici dei tag e dei dati rappresentati dal reparse point. Nella tabella seguente vengono descritti questi bit.



| bit | Descrizione                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| M   | Bit Microsoft. Se questo bit è impostato, il tag è di proprietà di Microsoft. Tutti gli altri tag devono usare zero per questo bit. |
| R   | Riservato; deve essere zero per tutti i tag non Microsoft.                                                           |
| N   | Bit surrogato del nome. Se questo bit è impostato, il file o la directory rappresenta un'altra entità denominata nel sistema. |



 

Per facilitare il test dei tag sono disponibili le macro seguenti:

-   [**IsReparseTagMicrosoft**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [**IsReparseTagNameSurrogate**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

Ogni macro restituisce un valore diverso da zero se il bit associato è impostato.

Di seguito sono riportati i valori dei tag di reparse predefiniti di Microsoft. sono definiti in WinNT.h:

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

Per garantire l'univocità dei tag, Microsoft fornisce un meccanismo per distribuire nuovi tag. Per altre informazioni, vedere [Installable File System (IFS) Kit](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).

 

 



