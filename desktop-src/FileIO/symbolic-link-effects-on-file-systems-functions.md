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
# <a name="symbolic-link-effects-on-file-systems-functions"></a><span data-ttu-id="7222f-103">Effetti dei collegamenti simbolici sulle funzioni di file System</span><span class="sxs-lookup"><span data-stu-id="7222f-103">Symbolic Link Effects on File Systems Functions</span></span>

<span data-ttu-id="7222f-104">Diverse funzioni di file standard che usano nomi di percorso per specificare uno o più file sono interessate dall'uso di collegamenti simbolici.</span><span class="sxs-lookup"><span data-stu-id="7222f-104">Several standard file functions that use path names to specify one or more files are affected by the use of symbolic links.</span></span> <span data-ttu-id="7222f-105">In questo argomento vengono elencate le funzioni e descritte le modifiche nel comportamento:</span><span class="sxs-lookup"><span data-stu-id="7222f-105">This topic lists those functions and describes the changes in behavior:</span></span>

-   [<span data-ttu-id="7222f-106">CopyFile e CopyFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-106">CopyFile and CopyFileTransacted</span></span>](#copyfile-and-copyfiletransacted)
-   [<span data-ttu-id="7222f-107">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="7222f-107">CopyFileEx</span></span>](#copyfileex)
-   [<span data-ttu-id="7222f-108">CreateFile e CreateFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-108">CreateFile and CreateFileTransacted</span></span>](#createfile-and-createfiletransacted)
-   [<span data-ttu-id="7222f-109">CreateHardLink e CreateHardLinkTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-109">CreateHardLink and CreateHardLinkTransacted</span></span>](#createhardlink-and-createhardlinktransacted)
-   [<span data-ttu-id="7222f-110">DeleteFile e DeleteFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-110">DeleteFile and DeleteFileTransacted</span></span>](#deletefile-and-deletefiletransacted)
-   [<span data-ttu-id="7222f-111">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="7222f-111">FindFirstChangeNotification</span></span>](#findfirstchangenotification)
-   [<span data-ttu-id="7222f-112">FindFirstFile e FindFirstFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-112">FindFirstFile and FindFirstFileTransacted</span></span>](#findfirstfile-and-findfirstfiletransacted)
-   [<span data-ttu-id="7222f-113">FindFirstFileEx</span><span class="sxs-lookup"><span data-stu-id="7222f-113">FindFirstFileEx</span></span>](#findfirstfileex)
-   [<span data-ttu-id="7222f-114">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="7222f-114">FindNextFile</span></span>](#findnextfile)
-   [<span data-ttu-id="7222f-115">GetBinaryType</span><span class="sxs-lookup"><span data-stu-id="7222f-115">GetBinaryType</span></span>](#getbinarytype)
-   [<span data-ttu-id="7222f-116">GetCompressedFileSize e GetCompressedFileSizeTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-116">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [<span data-ttu-id="7222f-117">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="7222f-117">GetDiskFreeSpace</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="7222f-118">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="7222f-118">GetDiskFreeSpaceEx</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="7222f-119">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="7222f-119">GetFileAttributes</span></span>](#getfileattributesex)
-   [<span data-ttu-id="7222f-120">GetFileAttributesEx</span><span class="sxs-lookup"><span data-stu-id="7222f-120">GetFileAttributesEx</span></span>](#getfileattributesex)
-   [<span data-ttu-id="7222f-121">GetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="7222f-121">GetFileSecurity</span></span>](#getfilesecurity)
-   [<span data-ttu-id="7222f-122">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="7222f-122">GetTempPath</span></span>](#gettemppath)
-   [<span data-ttu-id="7222f-123">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="7222f-123">GetVolumeInformation</span></span>](#getvolumeinformation)
-   [<span data-ttu-id="7222f-124">SetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="7222f-124">SetFileAttributes</span></span>](#setfileattributes)
-   [<span data-ttu-id="7222f-125">SetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="7222f-125">SetFileSecurity</span></span>](#setfilesecurity)
-   [<span data-ttu-id="7222f-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7222f-126">Related topics</span></span>](#related-topics)

<span data-ttu-id="7222f-127">Nelle descrizioni riportate di seguito vengono usati i termini seguenti:</span><span class="sxs-lookup"><span data-stu-id="7222f-127">In the descriptions below, the following terms are used:</span></span>

-   <span data-ttu-id="7222f-128">File di origine: il file originale da copiare.</span><span class="sxs-lookup"><span data-stu-id="7222f-128">Source file—The original file that is to be copied.</span></span>
-   <span data-ttu-id="7222f-129">File di destinazione: la copia del file appena creata.</span><span class="sxs-lookup"><span data-stu-id="7222f-129">Destination file—The newly created copy of the file.</span></span>
-   <span data-ttu-id="7222f-130">Target: entità a cui punta un collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-130">Target—The entity that a symbolic link points to.</span></span>

> [!Note]  
> <span data-ttu-id="7222f-131">Il comportamento delle funzioni che accettano un handle creato mediante la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , ad esempio la funzione [**GetFileTime ha provocato**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) , varia a seconda che la funzione **CreateFile** sia stata chiamata o meno usando il flag di **file \_ \_ Open \_ reparse \_ Point** .</span><span class="sxs-lookup"><span data-stu-id="7222f-131">The behavior of functions that accept a handle created using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, such as the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) function, will differ based on whether or not the **CreateFile** function was called using the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span> <span data-ttu-id="7222f-132">Per ulteriori informazioni, vedere [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e la sezione [CreateFile e CreateFileTransacted](#createfile-and-createfiletransacted) seguente.</span><span class="sxs-lookup"><span data-stu-id="7222f-132">For more information, see [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and the following [CreateFile and CreateFileTransacted](#createfile-and-createfiletransacted) section.</span></span>

 

## <a name="copyfile-and-copyfiletransacted"></a><span data-ttu-id="7222f-133">CopyFile e CopyFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-133">CopyFile and CopyFileTransacted</span></span>

<span data-ttu-id="7222f-134">Se il file di origine è un collegamento simbolico, il file effettivamente copiato è la destinazione del collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-134">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

<span data-ttu-id="7222f-135">Se il file di destinazione esiste già ed è un collegamento simbolico, il collegamento simbolico viene sovrascritto dal file di origine.</span><span class="sxs-lookup"><span data-stu-id="7222f-135">If the destination file already exists and is a symbolic link, the symbolic link is overwritten by the source file.</span></span>

## <a name="copyfileex"></a><span data-ttu-id="7222f-136">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="7222f-136">CopyFileEx</span></span>

<span data-ttu-id="7222f-137">Se viene specificato il **\_ \_ \_ collegamento simbolico copia file** e:</span><span class="sxs-lookup"><span data-stu-id="7222f-137">If **COPY\_FILE\_COPY\_SYMLINK** is specified and:</span></span>

-   <span data-ttu-id="7222f-138">Se il file di origine è un collegamento simbolico, viene copiato il collegamento simbolico, non il file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-138">If the source file is a symbolic link, the symbolic link is copied, not the target file.</span></span>
-   <span data-ttu-id="7222f-139">Se il file di origine non è un collegamento simbolico, non viene apportata alcuna modifica al comportamento.</span><span class="sxs-lookup"><span data-stu-id="7222f-139">If the source file is not a symbolic link, there is no change in behavior.</span></span>
-   <span data-ttu-id="7222f-140">Se il file di destinazione è un collegamento simbolico esistente, il collegamento simbolico viene sovrascritto, non il file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-140">If the destination file is an existing symbolic link, the symbolic link is overwritten, not the target file.</span></span>
-   <span data-ttu-id="7222f-141">Se viene specificato anche il **file di copia, \_ \_ \_ se \_ esiste** , e il file di destinazione è un collegamento simbolico esistente, l'operazione avrà esito negativo in tutti i casi.</span><span class="sxs-lookup"><span data-stu-id="7222f-141">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails in all cases.</span></span>

<span data-ttu-id="7222f-142">Se **il \_ \_ \_ collegamento simbolico copia file** non è specificato e:</span><span class="sxs-lookup"><span data-stu-id="7222f-142">If **COPY\_FILE\_COPY\_SYMLINK** is not specified and:</span></span>

-   <span data-ttu-id="7222f-143">Se viene specificato anche il **file di copia, \_ \_ \_ se \_ esiste** , e il file di destinazione è un collegamento simbolico esistente, l'operazione ha esito negativo solo se esiste la destinazione del collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-143">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails only if the target of the symbolic link exists.</span></span>
-   <span data-ttu-id="7222f-144">Se il **file di copia ha \_ \_ esito negativo se non viene specificato \_ \_ Exists** , non è presente alcuna modifica nel comportamento.</span><span class="sxs-lookup"><span data-stu-id="7222f-144">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is not specified, there is no change in behavior.</span></span>

<span data-ttu-id="7222f-145">**Windows Server 2003 e Windows XP:** Il flag di copia del **\_ \_ \_ collegamento simbolico copia file** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7222f-145">**Windows Server 2003 and Windows XP:** The **COPY\_FILE\_COPY\_SYMLINK** flag is not supported.</span></span> <span data-ttu-id="7222f-146">Se il file di origine è un collegamento simbolico, il file effettivamente copiato è la destinazione del collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-146">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

## <a name="createfile-and-createfiletransacted"></a><span data-ttu-id="7222f-147">CreateFile e CreateFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-147">CreateFile and CreateFileTransacted</span></span>

<span data-ttu-id="7222f-148">Se la chiamata a questa funzione crea un nuovo file, non viene apportata alcuna modifica al comportamento.</span><span class="sxs-lookup"><span data-stu-id="7222f-148">If the call to this function creates a new file, there is no change in behavior.</span></span>

<span data-ttu-id="7222f-149">Se viene specificato il **flag di file \_ \_ aperto \_ reparse \_ Point** e:</span><span class="sxs-lookup"><span data-stu-id="7222f-149">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is specified and:</span></span>

-   <span data-ttu-id="7222f-150">Se un file esistente viene aperto ed è un collegamento simbolico, l'handle restituito è un handle per il collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-150">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the symbolic link.</span></span>
-   <span data-ttu-id="7222f-151">Se viene specificato **Create \_ Always**, **Truncate \_ exist** o **file \_ flag \_ Delete \_ alla \_ chiusura** , il file interessato è un collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-151">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is a symbolic link.</span></span>

<span data-ttu-id="7222f-152">Se **il \_ flag di file \_ aperto \_ reparse \_ Point** non è specificato e:</span><span class="sxs-lookup"><span data-stu-id="7222f-152">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is not specified and:</span></span>

-   <span data-ttu-id="7222f-153">Se un file esistente viene aperto ed è un collegamento simbolico, l'handle restituito è un handle per la destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-153">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the target.</span></span>
-   <span data-ttu-id="7222f-154">Se viene specificato **Create \_ Always**, **Truncate \_ exist** o **file \_ flag \_ Delete alla \_ \_ chiusura** , il file interessato è la destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-154">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is the target.</span></span>

## <a name="createhardlink-and-createhardlinktransacted"></a><span data-ttu-id="7222f-155">CreateHardLink e CreateHardLinkTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-155">CreateHardLink and CreateHardLinkTransacted</span></span>

<span data-ttu-id="7222f-156">Se il percorso punta a un collegamento simbolico, la funzione crea un collegamento reale alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-156">If the path points to a symbolic link, the function creates a hard link to the target.</span></span>

## <a name="deletefile-and-deletefiletransacted"></a><span data-ttu-id="7222f-157">DeleteFile e DeleteFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-157">DeleteFile and DeleteFileTransacted</span></span>

<span data-ttu-id="7222f-158">Se il percorso punta a un collegamento simbolico, il collegamento simbolico viene eliminato e non la destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-158">If the path points to a symbolic link, the symbolic link is deleted, not the target.</span></span> <span data-ttu-id="7222f-159">Per eliminare una destinazione, è necessario chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e specificare **\_ il flag \_ di file Delete \_ alla \_ chiusura**.</span><span class="sxs-lookup"><span data-stu-id="7222f-159">To delete a target, you must call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and specify **FILE\_FLAG\_DELETE\_ON\_CLOSE**.</span></span>

## <a name="findfirstchangenotification"></a><span data-ttu-id="7222f-160">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="7222f-160">FindFirstChangeNotification</span></span>

<span data-ttu-id="7222f-161">Se il percorso punta a un collegamento simbolico, viene creato l'handle di notifica per la destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-161">If the path points to a symbolic link, the notification handle is created for the target.</span></span> <span data-ttu-id="7222f-162">Se un'applicazione è stata registrata per ricevere le notifiche delle modifiche per una directory che contiene collegamenti simbolici, l'applicazione riceverà una notifica solo quando i collegamenti simbolici sono stati modificati, non i file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-162">If an application has registered to receive change notifications for a directory that contains symbolic links, the application is only notified when the symbolic links have been changed, not the target files.</span></span>

## <a name="findfirstfile-and-findfirstfiletransacted"></a><span data-ttu-id="7222f-163">FindFirstFile e FindFirstFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-163">FindFirstFile and FindFirstFileTransacted</span></span>

<span data-ttu-id="7222f-164">Se il percorso punta a un collegamento simbolico, il buffer [**\_ \_ dei dati di ricerca Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene informazioni sul collegamento simbolico, non sulla destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-164">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findfirstfileex"></a><span data-ttu-id="7222f-165">FindFirstFileEx</span><span class="sxs-lookup"><span data-stu-id="7222f-165">FindFirstFileEx</span></span>

<span data-ttu-id="7222f-166">Se il percorso punta a un collegamento simbolico, il buffer [**\_ \_ dei dati di ricerca Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene informazioni sul collegamento simbolico, non sulla destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-166">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findnextfile"></a><span data-ttu-id="7222f-167">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="7222f-167">FindNextFile</span></span>

<span data-ttu-id="7222f-168">Se il percorso punta a un collegamento simbolico, il buffer [**\_ \_ dei dati di ricerca Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene informazioni sul collegamento simbolico, non sulla destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-168">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="getbinarytype"></a><span data-ttu-id="7222f-169">GetBinaryType</span><span class="sxs-lookup"><span data-stu-id="7222f-169">GetBinaryType</span></span>

<span data-ttu-id="7222f-170">Se il percorso punta a un collegamento simbolico, viene usato il file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-170">If the path points to a symbolic link, the target file is used.</span></span>

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a><span data-ttu-id="7222f-171">GetCompressedFileSize e GetCompressedFileSizeTransacted</span><span class="sxs-lookup"><span data-stu-id="7222f-171">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>

<span data-ttu-id="7222f-172">Se il percorso punta a un collegamento simbolico, la funzione restituisce le dimensioni del file della destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-172">If the path points to a symbolic link, the function returns the file size of the target.</span></span>

## <a name="getdiskfreespace"></a><span data-ttu-id="7222f-173">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="7222f-173">GetDiskFreeSpace</span></span>

<span data-ttu-id="7222f-174">Se il percorso punta a un collegamento simbolico, l'operazione viene eseguita sulla destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-174">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getdiskfreespaceex"></a><span data-ttu-id="7222f-175">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="7222f-175">GetDiskFreeSpaceEx</span></span>

<span data-ttu-id="7222f-176">Se il percorso punta a un collegamento simbolico, l'operazione viene eseguita sulla destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-176">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getfileattributes"></a><span data-ttu-id="7222f-177">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="7222f-177">GetFileAttributes</span></span>

<span data-ttu-id="7222f-178">Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-178">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfileattributesex"></a><span data-ttu-id="7222f-179">GetFileAttributesEx</span><span class="sxs-lookup"><span data-stu-id="7222f-179">GetFileAttributesEx</span></span>

<span data-ttu-id="7222f-180">Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-180">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfilesecurity"></a><span data-ttu-id="7222f-181">GetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="7222f-181">GetFileSecurity</span></span>

<span data-ttu-id="7222f-182">Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-182">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="gettemppath"></a><span data-ttu-id="7222f-183">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="7222f-183">GetTempPath</span></span>

<span data-ttu-id="7222f-184">Se il percorso punta a un collegamento simbolico, il nome del percorso temporaneo gestisce tutti i collegamenti simbolici.</span><span class="sxs-lookup"><span data-stu-id="7222f-184">If the path points to a symbolic link, the temp path name maintains any symbolic links.</span></span>

## <a name="getvolumeinformation"></a><span data-ttu-id="7222f-185">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="7222f-185">GetVolumeInformation</span></span>

<span data-ttu-id="7222f-186">Se il percorso punta a un collegamento simbolico, la funzione restituisce informazioni sul volume per la destinazione.</span><span class="sxs-lookup"><span data-stu-id="7222f-186">If the path points to a symbolic link, the function returns volume information for the target.</span></span>

## <a name="setfileattributes"></a><span data-ttu-id="7222f-187">SetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="7222f-187">SetFileAttributes</span></span>

<span data-ttu-id="7222f-188">Se il percorso punta a un collegamento simbolico, la funzione recupera gli attributi per il collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-188">If the path points to a symbolic link, the function retrieves attributes for the symbolic link.</span></span>

## <a name="setfilesecurity"></a><span data-ttu-id="7222f-189">SetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="7222f-189">SetFileSecurity</span></span>

<span data-ttu-id="7222f-190">Se il percorso punta a un collegamento simbolico, la funzione restituisce gli attributi per il collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="7222f-190">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7222f-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7222f-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7222f-192">**CopyFile**</span><span class="sxs-lookup"><span data-stu-id="7222f-192">**CopyFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[<span data-ttu-id="7222f-193">**CopyFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="7222f-193">**CopyFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[<span data-ttu-id="7222f-194">**CopyFileEx**</span><span class="sxs-lookup"><span data-stu-id="7222f-194">**CopyFileEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[<span data-ttu-id="7222f-195">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="7222f-195">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="7222f-196">**CreateFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="7222f-196">**CreateFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[<span data-ttu-id="7222f-197">**CreateHardLink**</span><span class="sxs-lookup"><span data-stu-id="7222f-197">**CreateHardLink**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[<span data-ttu-id="7222f-198">**CreateHardLinkTransacted**</span><span class="sxs-lookup"><span data-stu-id="7222f-198">**CreateHardLinkTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[<span data-ttu-id="7222f-199">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="7222f-199">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[<span data-ttu-id="7222f-200">**DeleteFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="7222f-200">**DeleteFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[<span data-ttu-id="7222f-201">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="7222f-201">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[<span data-ttu-id="7222f-202">**FindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="7222f-202">**FindFirstFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[<span data-ttu-id="7222f-203">**FindFirstFileEx**</span><span class="sxs-lookup"><span data-stu-id="7222f-203">**FindFirstFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[<span data-ttu-id="7222f-204">**FindFirstFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="7222f-204">**FindFirstFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[<span data-ttu-id="7222f-205">**FindNextFile**</span><span class="sxs-lookup"><span data-stu-id="7222f-205">**FindNextFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[<span data-ttu-id="7222f-206">**GetBinaryType**</span><span class="sxs-lookup"><span data-stu-id="7222f-206">**GetBinaryType**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[<span data-ttu-id="7222f-207">**GetCompressedFileSize**</span><span class="sxs-lookup"><span data-stu-id="7222f-207">**GetCompressedFileSize**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[<span data-ttu-id="7222f-208">**GetCompressedFileSizeTransacted**</span><span class="sxs-lookup"><span data-stu-id="7222f-208">**GetCompressedFileSizeTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[<span data-ttu-id="7222f-209">**GetDiskFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="7222f-209">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[<span data-ttu-id="7222f-210">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="7222f-210">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[<span data-ttu-id="7222f-211">**GetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="7222f-211">**GetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[<span data-ttu-id="7222f-212">**GetFileAttributesEx**</span><span class="sxs-lookup"><span data-stu-id="7222f-212">**GetFileAttributesEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[<span data-ttu-id="7222f-213">**GetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="7222f-213">**GetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[<span data-ttu-id="7222f-214">**GetTempPath**</span><span class="sxs-lookup"><span data-stu-id="7222f-214">**GetTempPath**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[<span data-ttu-id="7222f-215">**GetVolumeInformation**</span><span class="sxs-lookup"><span data-stu-id="7222f-215">**GetVolumeInformation**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[<span data-ttu-id="7222f-216">**SetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="7222f-216">**SetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[<span data-ttu-id="7222f-217">**SetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="7222f-217">**SetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
