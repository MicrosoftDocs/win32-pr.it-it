---
title: Backup e ripristino di collegamenti reali
description: Per eseguire il backup e il ripristino dei collegamenti reali, utilizzare le funzioni CreateFile, CreateHardLink, FindFirstFileNameW, FindNextFileNameW, BackupRead, GetFileInformationByHandle e BackupWrite, come illustrato negli esempi di pseudocodice seguenti.
ms.assetid: 129e9cf4-8ab1-45d2-8e1a-4bc85b9de668
keywords:
- Backup dei collegamenti reali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72155231295a1eb07b6b565c018b765693c8f46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047167"
---
# <a name="backing-up-and-restoring-hard-links"></a>Backup e ripristino di collegamenti reali

Per eseguire il backup e il ripristino dei collegamenti reali, utilizzare le funzioni [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**CreateHardLink**](/windows/desktop/api/winbase/nf-winbase-createhardlinka), [**FindFirstFileNameW**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew), [**FindNextFileNameW**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew), [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread), [**GetFileInformationByHandle**](/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle)e [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) , come illustrato negli esempi di pseudocodice seguenti.

## <a name="pseudocode-algorithm-for-backing-up-hard-links"></a>Algoritmo pseudocodice per il backup dei collegamenti reali

``` syntax
1.  Initialize and empty a list of known links. 
2.  While there are more files to back up 
3.     Read the disk and get the next file. 
4.     Call CreateFile to open the file for read. 
5.     Call GetFileInformationByHandle to get the NumberOfLinks 
          and the FileIndex.
6.     If the NumberOfLinks is greater than 1 
7.        Search the list of known links, looking for the  
             same FileIndex.
8.        If a match is found 
9.           Skip this file; its link exists already on
                your backup media.
10.       Else
11.          Add the full path of the file and the FileIndex
                to the list of links.
12.          Call BackupRead to copy all data to your backup media.
13.          Call FindFirstFileNameW and FindNextFileNameW to 
                enumerate the hard links to the file.
14.          For each hard link
15.             Mark the data as a LINK on your backup media.
16.             Store the full path from the list to your backup media.
17.          Endfor
18.       Endif
19.    Else
20.       Call BackupRead to copy all data to your backup media.
21.    Endif
22. EndWhile
```

## <a name="pseudocode-algorithm-for-restoring-hard-links"></a>Algoritmo pseudocodice per il ripristino di collegamenti reali

``` syntax
1.  While there are more files to restore 
2.     If there are hard links to the file
3.        Call CreateHardLink to recreate the links.
4.     Endif
5.     Call BackupWrite with the data stored on your backup media
6.  EndWhile
```

**Windows Server 2003 e Windows XP:** Le funzioni [**FindFirstFileNameW**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew) non sono supportate. È invece possibile utilizzare la procedura illustrata nell'esempio di pseudocodice seguente.

## <a name="alternate-pseudocode-algorithm-for-backing-up-hard-links"></a>Algoritmo pseudocodice alternativo per il backup dei collegamenti reali

``` syntax
1.  Initialize and empty a list of known links. 
2.  While there are more files to back up 
3.     Read the disk and get the next file. 
4.     Call CreateFile to open the file for read. 
5.     Call GetFileInformationByHandle to get the NumberOfLinks and 
          the FileIndex. 
6.     If the NumberOfLinks is greater than 1 
7.        Search the list of known links looking for 
             the same FileIndex. 
8.           If a match is NOT found 
9.              Add the full path of the file and the FileIndex
                   to the list. 
10.             Call BackupRead to copy all data to 
                   your backup media. 
11.          Else 
12.             Mark the data as a LINK on your backup media 
13.             Store the full path from the list 
                   to your backup media. 
14.          Endif 
15.    Else 
16.       Call BackupRead to copy all data to your 
             backup media. 
17.    Endif 
18. EndWhile
```

 

 