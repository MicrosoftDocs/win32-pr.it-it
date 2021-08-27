---
description: Effetto dei collegamenti simbolici sulle funzioni di file standard che usano nomi di percorso per specificare uno o più file.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Effetti di collegamento simbolico sulle funzioni dei file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1c5d140dc70de8ebc255b779b226b6da156aa2b8961c49d86f466ac01b26ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078457"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a>Effetti di collegamento simbolico sulle funzioni dei file system

Diverse funzioni di file standard che usano nomi di percorso per specificare uno o più file sono interessate dall'uso di collegamenti simbolici. In questo argomento vengono elencate queste funzioni e vengono descritte le modifiche apportate al comportamento:

-   [CopyFile e CopyFileTransacted](#copyfile-and-copyfiletransacted)
-   [CopyFileEx](#copyfileex)
-   [CreateFile e CreateFileTransacted](#createfile-and-createfiletransacted)
-   [CreateHardLink e CreateHardLinkTransacted](#createhardlink-and-createhardlinktransacted)
-   [DeleteFile e DeleteFileTransacted](#deletefile-and-deletefiletransacted)
-   [FindFirstChangeNotification](#findfirstchangenotification)
-   [FindFirstFile e FindFirstFileTransacted](#findfirstfile-and-findfirstfiletransacted)
-   [FindFirstFileEx](#findfirstfileex)
-   [Findnextfile](#findnextfile)
-   [GetBinaryType](#getbinarytype)
-   [GetCompressedFileSize e GetCompressedFileSizeTransacted](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [GetDiskFreeSpace](#getdiskfreespaceex)
-   [Getdiskfreespaceex](#getdiskfreespaceex)
-   [GetFileAttributes](#getfileattributesex)
-   [GetFileAttributesEx](#getfileattributesex)
-   [GetFileSecurity](#getfilesecurity)
-   [GetTempPath](#gettemppath)
-   [GetVolumeInformation](#getvolumeinformation)
-   [SetFileAttributes](#setfileattributes)
-   [SetFileSecurity](#setfilesecurity)
-   [Argomenti correlati](#related-topics)

Nelle descrizioni seguenti vengono usati i termini seguenti:

-   File di origine: file originale da copiare.
-   File di destinazione: copia del file appena creata.
-   Destinazione: entità a cui punta un collegamento simbolico.

> [!Note]  
> Il comportamento delle funzioni che accettano un handle creato usando la funzione [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ad esempio la funzione [**GetFileTime,**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) sarà diverso a seconda che la funzione **CreateFile** sia stata chiamata o meno usando il flag **FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT.** Per altre informazioni, vedere [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e la sezione [CreateFile e CreateFileTransacted](#createfile-and-createfiletransacted) seguente.

 

## <a name="copyfile-and-copyfiletransacted"></a>CopyFile e CopyFileTransacted

Se il file di origine è un collegamento simbolico, il file effettivo copiato è la destinazione del collegamento simbolico.

Se il file di destinazione esiste già ed è un collegamento simbolico, il collegamento simbolico viene sovrascritto dal file di origine.

## <a name="copyfileex"></a>CopyFileEx

Se **copy FILE COPY \_ \_ \_ SYMLINK è** specificato e:

-   Se il file di origine è un collegamento simbolico, il collegamento simbolico viene copiato, non il file di destinazione.
-   Se il file di origine non è un collegamento simbolico, il comportamento non viene modificato.
-   Se il file di destinazione è un collegamento simbolico esistente, il collegamento simbolico viene sovrascritto, non il file di destinazione.
-   Se **si specifica anche COPY FILE FAIL IF \_ \_ \_ \_ EXISTS** e il file di destinazione è un collegamento simbolico esistente, l'operazione non riesce in tutti i casi.

Se **COPY FILE COPY \_ \_ \_ SYMLINK** non è specificato e:

-   Se si specifica anche **COPY FILE FAIL IF \_ \_ \_ \_ EXISTS** e il file di destinazione è un collegamento simbolico esistente, l'operazione ha esito negativo solo se esiste la destinazione del collegamento simbolico.
-   Se **l'opzione COPY \_ FILE FAIL IF \_ \_ \_ EXISTS** non è specificata, il comportamento non viene modificato.

**Windows Server 2003 e Windows XP:** Il flag **COPY \_ FILE COPY \_ \_ SYMLINK** non è supportato. Se il file di origine è un collegamento simbolico, il file effettivo copiato è la destinazione del collegamento simbolico.

## <a name="createfile-and-createfiletransacted"></a>CreateFile e CreateFileTransacted

Se la chiamata a questa funzione crea un nuovo file, il comportamento non viene modificato.

Se **è specificato FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT** e:

-   Se un file esistente viene aperto ed è un collegamento simbolico, l'handle restituito è un handle per il collegamento simbolico.
-   Se **vengono specificati CREATE \_ ALWAYS,** **TRUNCATE \_ EXISTING** o **FILE FLAG DELETE ON \_ \_ \_ \_ CLOSE,** il file interessato è un collegamento simbolico.

Se **FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT** non è specificato e:

-   Se un file esistente viene aperto ed è un collegamento simbolico, l'handle restituito è un handle per la destinazione.
-   Se **si specificato CREATE \_ ALWAYS**, **TRUNCATE \_ EXISTING** o **FILE FLAG DELETE ON \_ \_ \_ \_ CLOSE,** il file interessato è la destinazione.

## <a name="createhardlink-and-createhardlinktransacted"></a>CreateHardLink e CreateHardLinkTransacted

Se il percorso punta a un collegamento simbolico, la funzione crea un collegamento rigido alla destinazione.

## <a name="deletefile-and-deletefiletransacted"></a>DeleteFile e DeleteFileTransacted

Se il percorso punta a un collegamento simbolico, il collegamento simbolico viene eliminato, non la destinazione. Per eliminare una destinazione, è necessario chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e specificare **FILE FLAG DELETE ON \_ \_ \_ \_ CLOSE**.

## <a name="findfirstchangenotification"></a>FindFirstChangeNotification

Se il percorso punta a un collegamento simbolico, viene creato l'handle di notifica per la destinazione. Se un'applicazione è stata registrata per ricevere notifiche di modifica per una directory che contiene collegamenti simbolici, l'applicazione riceve una notifica solo quando i collegamenti simbolici sono stati modificati, non i file di destinazione.

## <a name="findfirstfile-and-findfirstfiletransacted"></a>FindFirstFile e FindFirstFileTransacted

Se il percorso punta a un collegamento simbolico, il buffer [**\_ FIND \_ DATA WIN32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene informazioni sul collegamento simbolico, non sulla destinazione.

## <a name="findfirstfileex"></a>FindFirstFileEx

Se il percorso punta a un collegamento simbolico, il buffer [**\_ FIND \_ DATA WIN32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene informazioni sul collegamento simbolico, non sulla destinazione.

## <a name="findnextfile"></a>Findnextfile

Se il percorso punta a un collegamento simbolico, il buffer [**\_ FIND \_ DATA WIN32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene informazioni sul collegamento simbolico, non sulla destinazione.

## <a name="getbinarytype"></a>GetBinaryType

Se il percorso punta a un collegamento simbolico, viene usato il file di destinazione.

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a>GetCompressedFileSize e GetCompressedFileSizeTransacted

Se il percorso punta a un collegamento simbolico, la funzione restituisce le dimensioni del file della destinazione.

## <a name="getdiskfreespace"></a>GetDiskFreeSpace

Se il percorso punta a un collegamento simbolico, l'operazione viene eseguita sulla destinazione.

## <a name="getdiskfreespaceex"></a>Getdiskfreespaceex

Se il percorso punta a un collegamento simbolico, l'operazione viene eseguita sulla destinazione.

## <a name="getfileattributes"></a>GetFileAttributes

Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.

## <a name="getfileattributesex"></a>GetFileAttributesEx

Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.

## <a name="getfilesecurity"></a>GetFileSecurity

Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.

## <a name="gettemppath"></a>GetTempPath

Se il percorso punta a un collegamento simbolico, il nome del percorso temporaneo mantiene tutti i collegamenti simbolici.

## <a name="getvolumeinformation"></a>GetVolumeInformation

Se il percorso punta a un collegamento simbolico, la funzione restituisce informazioni sul volume per la destinazione.

## <a name="setfileattributes"></a>SetFileAttributes

Se il percorso punta a un collegamento simbolico, la funzione recupera gli attributi per il collegamento simbolico.

## <a name="setfilesecurity"></a>SetFileSecurity

Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[**Findfirstfile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[**Findnextfile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[**GetBinaryType**](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[**Getdiskfreespaceex**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[**Attributi SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
