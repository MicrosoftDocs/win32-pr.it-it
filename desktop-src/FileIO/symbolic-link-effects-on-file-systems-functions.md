---
description: Il modo in cui i collegamenti simbolici influiscono sulle funzioni file standard che usano nomi di percorso per specificare uno o più file.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Effetti dei collegamenti simbolici sulle funzioni di file System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a2fe1696bf5260a0c55ba8b6e4f107270d6da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316767"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a>Effetti dei collegamenti simbolici sulle funzioni di file System

Diverse funzioni di file standard che usano nomi di percorso per specificare uno o più file sono interessate dall'uso di collegamenti simbolici. In questo argomento vengono elencate le funzioni e descritte le modifiche nel comportamento:

-   [CopyFile e CopyFileTransacted](#copyfile-and-copyfiletransacted)
-   [CopyFileEx](#copyfileex)
-   [CreateFile e CreateFileTransacted](#createfile-and-createfiletransacted)
-   [CreateHardLink e CreateHardLinkTransacted](#createhardlink-and-createhardlinktransacted)
-   [DeleteFile e DeleteFileTransacted](#deletefile-and-deletefiletransacted)
-   [FindFirstChangeNotification](#findfirstchangenotification)
-   [FindFirstFile e FindFirstFileTransacted](#findfirstfile-and-findfirstfiletransacted)
-   [FindFirstFileEx](#findfirstfileex)
-   [FindNextFile](#findnextfile)
-   [GetBinaryType](#getbinarytype)
-   [GetCompressedFileSize e GetCompressedFileSizeTransacted](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [GetDiskFreeSpace](#getdiskfreespaceex)
-   [GetDiskFreeSpaceEx](#getdiskfreespaceex)
-   [GetFileAttributes](#getfileattributesex)
-   [GetFileAttributesEx](#getfileattributesex)
-   [GetFileSecurity](#getfilesecurity)
-   [GetTempPath](#gettemppath)
-   [GetVolumeInformation](#getvolumeinformation)
-   [SetFileAttributes](#setfileattributes)
-   [SetFileSecurity](#setfilesecurity)
-   [Argomenti correlati](#related-topics)

Nelle descrizioni riportate di seguito vengono usati i termini seguenti:

-   File di origine: il file originale da copiare.
-   File di destinazione: la copia del file appena creata.
-   Target: entità a cui punta un collegamento simbolico.

> [!Note]  
> Il comportamento delle funzioni che accettano un handle creato mediante la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , ad esempio la funzione [**GetFileTime ha provocato**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) , varia a seconda che la funzione **CreateFile** sia stata chiamata o meno usando il flag di **file \_ \_ Open \_ reparse \_ Point** . Per ulteriori informazioni, vedere [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e la sezione [CreateFile e CreateFileTransacted](#createfile-and-createfiletransacted) seguente.

 

## <a name="copyfile-and-copyfiletransacted"></a>CopyFile e CopyFileTransacted

Se il file di origine è un collegamento simbolico, il file effettivamente copiato è la destinazione del collegamento simbolico.

Se il file di destinazione esiste già ed è un collegamento simbolico, il collegamento simbolico viene sovrascritto dal file di origine.

## <a name="copyfileex"></a>CopyFileEx

Se viene specificato il **\_ \_ \_ collegamento simbolico copia file** e:

-   Se il file di origine è un collegamento simbolico, viene copiato il collegamento simbolico, non il file di destinazione.
-   Se il file di origine non è un collegamento simbolico, non viene apportata alcuna modifica al comportamento.
-   Se il file di destinazione è un collegamento simbolico esistente, il collegamento simbolico viene sovrascritto, non il file di destinazione.
-   Se viene specificato anche il **file di copia, \_ \_ \_ se \_ esiste** , e il file di destinazione è un collegamento simbolico esistente, l'operazione avrà esito negativo in tutti i casi.

Se **il \_ \_ \_ collegamento simbolico copia file** non è specificato e:

-   Se viene specificato anche il **file di copia, \_ \_ \_ se \_ esiste** , e il file di destinazione è un collegamento simbolico esistente, l'operazione ha esito negativo solo se esiste la destinazione del collegamento simbolico.
-   Se il **file di copia ha \_ \_ esito negativo se non viene specificato \_ \_ Exists** , non è presente alcuna modifica nel comportamento.

**Windows Server 2003 e Windows XP:** Il flag di copia del **\_ \_ \_ collegamento simbolico copia file** non è supportato. Se il file di origine è un collegamento simbolico, il file effettivamente copiato è la destinazione del collegamento simbolico.

## <a name="createfile-and-createfiletransacted"></a>CreateFile e CreateFileTransacted

Se la chiamata a questa funzione crea un nuovo file, non viene apportata alcuna modifica al comportamento.

Se viene specificato il **flag di file \_ \_ aperto \_ reparse \_ Point** e:

-   Se un file esistente viene aperto ed è un collegamento simbolico, l'handle restituito è un handle per il collegamento simbolico.
-   Se viene specificato **Create \_ Always**, **Truncate \_ exist** o **file \_ flag \_ Delete \_ alla \_ chiusura** , il file interessato è un collegamento simbolico.

Se **il \_ flag di file \_ aperto \_ reparse \_ Point** non è specificato e:

-   Se un file esistente viene aperto ed è un collegamento simbolico, l'handle restituito è un handle per la destinazione.
-   Se viene specificato **Create \_ Always**, **Truncate \_ exist** o **file \_ flag \_ Delete alla \_ \_ chiusura** , il file interessato è la destinazione.

## <a name="createhardlink-and-createhardlinktransacted"></a>CreateHardLink e CreateHardLinkTransacted

Se il percorso punta a un collegamento simbolico, la funzione crea un collegamento reale alla destinazione.

## <a name="deletefile-and-deletefiletransacted"></a>DeleteFile e DeleteFileTransacted

Se il percorso punta a un collegamento simbolico, il collegamento simbolico viene eliminato e non la destinazione. Per eliminare una destinazione, è necessario chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e specificare **\_ il flag \_ di file Delete \_ alla \_ chiusura**.

## <a name="findfirstchangenotification"></a>FindFirstChangeNotification

Se il percorso punta a un collegamento simbolico, viene creato l'handle di notifica per la destinazione. Se un'applicazione è stata registrata per ricevere le notifiche delle modifiche per una directory che contiene collegamenti simbolici, l'applicazione riceverà una notifica solo quando i collegamenti simbolici sono stati modificati, non i file di destinazione.

## <a name="findfirstfile-and-findfirstfiletransacted"></a>FindFirstFile e FindFirstFileTransacted

Se il percorso punta a un collegamento simbolico, il buffer [**\_ \_ dei dati di ricerca Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene informazioni sul collegamento simbolico, non sulla destinazione.

## <a name="findfirstfileex"></a>FindFirstFileEx

Se il percorso punta a un collegamento simbolico, il buffer [**\_ \_ dei dati di ricerca Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene informazioni sul collegamento simbolico, non sulla destinazione.

## <a name="findnextfile"></a>FindNextFile

Se il percorso punta a un collegamento simbolico, il buffer [**\_ \_ dei dati di ricerca Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene informazioni sul collegamento simbolico, non sulla destinazione.

## <a name="getbinarytype"></a>GetBinaryType

Se il percorso punta a un collegamento simbolico, viene usato il file di destinazione.

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a>GetCompressedFileSize e GetCompressedFileSizeTransacted

Se il percorso punta a un collegamento simbolico, la funzione restituisce le dimensioni del file della destinazione.

## <a name="getdiskfreespace"></a>GetDiskFreeSpace

Se il percorso punta a un collegamento simbolico, l'operazione viene eseguita sulla destinazione.

## <a name="getdiskfreespaceex"></a>GetDiskFreeSpaceEx

Se il percorso punta a un collegamento simbolico, l'operazione viene eseguita sulla destinazione.

## <a name="getfileattributes"></a>GetFileAttributes

Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.

## <a name="getfileattributesex"></a>GetFileAttributesEx

Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.

## <a name="getfilesecurity"></a>GetFileSecurity

Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.

## <a name="gettemppath"></a>GetTempPath

Se il percorso punta a un collegamento simbolico, il nome del percorso temporaneo gestisce tutti i collegamenti simbolici.

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

[**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[**GetBinaryType**](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
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

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
