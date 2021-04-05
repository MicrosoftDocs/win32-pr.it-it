---
title: Sessioni FTP
description: WinINet consente alle applicazioni di esplorare e modificare directory e file in un server FTP. Poiché i proxy CERN non supportano FTP, le applicazioni che usano un proxy CERN devono usare esclusivamente la funzione InternetOpenUrl.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047039"
---
# <a name="ftp-sessions"></a><span data-ttu-id="b92dd-104">Sessioni FTP</span><span class="sxs-lookup"><span data-stu-id="b92dd-104">FTP Sessions</span></span>

<span data-ttu-id="b92dd-105">WinINet consente alle applicazioni di esplorare e modificare directory e file in un server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-105">WinINet enables applications to navigate and manipulate directories and files on an ftp server.</span></span> <span data-ttu-id="b92dd-106">Poiché i proxy CERN non supportano FTP, le applicazioni che usano un proxy CERN devono usare esclusivamente la funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="b92dd-106">Because CERN proxies do not support FTP, applications that use a CERN proxy exclusively must use the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> <span data-ttu-id="b92dd-107">Per altre informazioni su come usare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), vedere [accesso diretto agli URL](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="b92dd-107">For more information about how to use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="b92dd-108">Per iniziare una sessione FTP, usare [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) per creare l'handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="b92dd-108">To begin an FTP session, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to create the session handle.</span></span>

<span data-ttu-id="b92dd-109">WinINet consente di eseguire le azioni seguenti su un server FTP:</span><span class="sxs-lookup"><span data-stu-id="b92dd-109">WinINet enables you to perform the following actions on an FTP server:</span></span>

-   <span data-ttu-id="b92dd-110">Spostarsi tra le directory.</span><span class="sxs-lookup"><span data-stu-id="b92dd-110">Navigate between directories.</span></span>
-   <span data-ttu-id="b92dd-111">Enumerare, creare, rimuovere e rinominare le directory.</span><span class="sxs-lookup"><span data-stu-id="b92dd-111">Enumerate, create, remove, and rename directories.</span></span>
-   <span data-ttu-id="b92dd-112">Rinominare, caricare, scaricare ed eliminare file.</span><span class="sxs-lookup"><span data-stu-id="b92dd-112">Rename, upload, download, and delete files.</span></span>

<span data-ttu-id="b92dd-113">Lo spostamento viene fornito dalle funzioni [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) e [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="b92dd-113">Navigation is provided by the [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions.</span></span> <span data-ttu-id="b92dd-114">Queste funzioni usano l'handle di sessione creato da una precedente chiamata a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) per determinare la directory in cui si trova attualmente l'applicazione o per passare a una sottodirectory diversa.</span><span class="sxs-lookup"><span data-stu-id="b92dd-114">These functions utilize the session handle created by a previous call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to determine which directory the application is currently in, or to change to a different subdirectory.</span></span>

<span data-ttu-id="b92dd-115">L'enumerazione di directory viene eseguita usando le funzioni [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) e [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="b92dd-115">Directory enumeration is performed by using the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="b92dd-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) usa l'handle di sessione creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) per trovare il primo file che corrisponde ai criteri di ricerca specificati e restituisce un handle per continuare l'enumerazione di directory.</span><span class="sxs-lookup"><span data-stu-id="b92dd-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to find the first file that matches the given search criteria and returns a handle to continue the directory enumeration.</span></span> <span data-ttu-id="b92dd-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) usa l'handle restituito da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) per restituire il file successivo corrispondente ai criteri di ricerca originali.</span><span class="sxs-lookup"><span data-stu-id="b92dd-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) uses the handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) to return the next file that matches the original search criteria.</span></span> <span data-ttu-id="b92dd-118">L'applicazione deve continuare a chiamare [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) fino a quando non sono presenti altri file rimasti nella directory.</span><span class="sxs-lookup"><span data-stu-id="b92dd-118">The application should continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until there are no more files left in the directory.</span></span>

<span data-ttu-id="b92dd-119">Usare la funzione [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) per creare nuove directory.</span><span class="sxs-lookup"><span data-stu-id="b92dd-119">Use the [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function to create new directories.</span></span> <span data-ttu-id="b92dd-120">Questa funzione usa l'handle di sessione creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e crea la directory specificata dalla stringa passata alla funzione.</span><span class="sxs-lookup"><span data-stu-id="b92dd-120">This function uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and creates the directory specified by the string passed to the function.</span></span> <span data-ttu-id="b92dd-121">La stringa può contenere un nome di directory relativo alla directory corrente o un percorso completo della directory.</span><span class="sxs-lookup"><span data-stu-id="b92dd-121">The string can contain a directory name relative to the current directory, or a fully qualified directory path.</span></span>

<span data-ttu-id="b92dd-122">Per rinominare file o directory, l'applicazione può chiamare [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span><span class="sxs-lookup"><span data-stu-id="b92dd-122">To rename either files or directories, the application can call [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span></span> <span data-ttu-id="b92dd-123">Questa funzione sostituisce il nome originale con il nuovo nome passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="b92dd-123">This function replaces the original name with the new name passed to the function.</span></span> <span data-ttu-id="b92dd-124">Il nome del file o della directory può essere relativo alla directory corrente o a un nome completo.</span><span class="sxs-lookup"><span data-stu-id="b92dd-124">The name of the file or directory can be relative to the current directory, or a fully qualified name.</span></span>

<span data-ttu-id="b92dd-125">Per caricare o inserire i file in un server FTP, l'applicazione può usare [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) o [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (insieme a [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span><span class="sxs-lookup"><span data-stu-id="b92dd-125">To upload or place files on an FTP server, the application can use either [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (along with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span></span> <span data-ttu-id="b92dd-126">È possibile utilizzare [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) se il file esiste già localmente, mentre [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) possono essere utilizzati se i dati devono essere scritti in un file nel server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-126">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) can be used if the file already exists locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) can be used if data needs to be written to a file on the FTP server.</span></span>

<span data-ttu-id="b92dd-127">Per scaricare o ottenere file, l'applicazione può usare [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) o [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (con [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span><span class="sxs-lookup"><span data-stu-id="b92dd-127">To download or get files, the application can use either [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span></span> <span data-ttu-id="b92dd-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) viene utilizzato per recuperare un file da un server FTP e archiviarlo localmente, mentre [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) possono essere utilizzati per controllare la posizione in cui le informazioni sono state scaricate. ad esempio, l'applicazione potrebbe visualizzare le informazioni in una casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="b92dd-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) is used to retrieve a file from an FTP server and store it locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can be used to control where the downloaded information is going (for example, the application could display the information in an edit box).</span></span>

<span data-ttu-id="b92dd-129">Eliminare i file in un server FTP utilizzando la funzione [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) .</span><span class="sxs-lookup"><span data-stu-id="b92dd-129">Delete files on an FTP server by using the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="b92dd-130">Questa funzione rimuove un nome file relativo alla directory corrente o a un nome di file completo dal server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-130">This function removes a file name that is relative either to the current directory or to a fully qualified file name from the FTP server.</span></span> <span data-ttu-id="b92dd-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) richiede un handle di sessione restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requires a session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>

## <a name="ftp-function-handles"></a><span data-ttu-id="b92dd-132">Handle di funzione FTP</span><span class="sxs-lookup"><span data-stu-id="b92dd-132">FTP Function Handles</span></span>

<span data-ttu-id="b92dd-133">Per il corretto funzionamento, le funzioni FTP richiedono determinati tipi di handle [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="b92dd-133">To work properly, the FTP functions require certain types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="b92dd-134">Questi handle devono essere creati in un ordine specifico, a partire dall'handle radice creato da [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="b92dd-134">These handles must be created in a specific order, starting with the root handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="b92dd-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) può quindi creare un handle di sessione FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) can then create an FTP session handle.</span></span>

<span data-ttu-id="b92dd-136">Il diagramma seguente mostra le funzioni che dipendono dall'handle della sessione FTP restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-136">The following diagram shows the functions that are dependent on the FTP session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="b92dd-137">Le caselle ombreggiate rappresentano funzioni che restituiscono handle [**HINTERNET**](appendix-a-hinternet-handles.md) , mentre le caselle semplici rappresentano funzioni che usano l'handle hInternet creato dalla funzione da cui dipendono.</span><span class="sxs-lookup"><span data-stu-id="b92dd-137">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the HINTERNET handle created by the function on which they depend.</span></span>

![funzioni FTP dipendenti dall'handle di sessione FTP restituito da InternetConnect](images/ax-wnt06.png)

<span data-ttu-id="b92dd-139">Il diagramma seguente illustra le due funzioni che restituiscono handle [HINTERNET](appendix-a-hinternet-handles.md) e le funzioni che dipendono da essi.</span><span class="sxs-lookup"><span data-stu-id="b92dd-139">The following diagram shows the two functions that return [HINTERNET](appendix-a-hinternet-handles.md) handles and the functions that are dependent on them.</span></span> <span data-ttu-id="b92dd-140">Le caselle ombreggiate rappresentano funzioni che restituiscono handle **HINTERNET** , mentre le caselle semplici rappresentano funzioni che usano l'handle **HINTERNET** creato dalla funzione da cui dipendono.</span><span class="sxs-lookup"><span data-stu-id="b92dd-140">The shaded boxes represent functions that return **HINTERNET** handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![funzioni FTP che restituiscono handle hInternet](images/ax-wnt03.png)

<span data-ttu-id="b92dd-142">Per altre informazioni, vedere [handle hInternet](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="b92dd-142">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-for-ftp-sessions"></a><span data-ttu-id="b92dd-143">Uso delle funzioni WinINet per le sessioni FTP</span><span class="sxs-lookup"><span data-stu-id="b92dd-143">Using the WinINet Functions for FTP Sessions</span></span>

<span data-ttu-id="b92dd-144">Le funzioni seguenti vengono utilizzate durante le sessioni FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-144">The following functions are used during FTP sessions.</span></span> <span data-ttu-id="b92dd-145">Queste funzioni non sono riconosciute dai proxy CERN.</span><span class="sxs-lookup"><span data-stu-id="b92dd-145">These functions are not recognized by CERN proxies.</span></span> <span data-ttu-id="b92dd-146">Le applicazioni che devono funzionare tramite proxy CERN devono usare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e accedere direttamente alle risorse.</span><span class="sxs-lookup"><span data-stu-id="b92dd-146">Applications that must function through CERN proxies should use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and access the resources directly.</span></span> <span data-ttu-id="b92dd-147">Per altre informazioni sull'accesso diretto alle risorse, vedere accesso diretto agli [URL](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="b92dd-147">For more information on direct resource access, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>



| <span data-ttu-id="b92dd-148">Funzione</span><span class="sxs-lookup"><span data-stu-id="b92dd-148">Function</span></span>                                                 | <span data-ttu-id="b92dd-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b92dd-149">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b92dd-150">**FtpCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="b92dd-150">**FtpCreateDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | <span data-ttu-id="b92dd-151">Crea una nuova directory nel server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-151">Creates a new directory on the server.</span></span> <span data-ttu-id="b92dd-152">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-152">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                  |
| [<span data-ttu-id="b92dd-153">**FtpDeleteFile**</span><span class="sxs-lookup"><span data-stu-id="b92dd-153">**FtpDeleteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | <span data-ttu-id="b92dd-154">Elimina un file dal server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-154">Deletes a file from the server.</span></span> <span data-ttu-id="b92dd-155">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-155">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                         |
| [<span data-ttu-id="b92dd-156">**FtpFindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="b92dd-156">**FtpFindFirstFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | <span data-ttu-id="b92dd-157">Avvia l'enumerazione dei file o la ricerca di file nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="b92dd-157">Starts file enumeration or file search in the current directory.</span></span> <span data-ttu-id="b92dd-158">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-158">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>        |
| [<span data-ttu-id="b92dd-159">**FtpGetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="b92dd-159">**FtpGetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | <span data-ttu-id="b92dd-160">Restituisce la directory corrente del client nel server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-160">Returns the client's current directory on the server.</span></span> <span data-ttu-id="b92dd-161">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-161">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="b92dd-162">**FtpGetFile**</span><span class="sxs-lookup"><span data-stu-id="b92dd-162">**FtpGetFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | <span data-ttu-id="b92dd-163">Recupera un file dal server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-163">Retrieves a file from the server.</span></span> <span data-ttu-id="b92dd-164">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-164">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                       |
| [<span data-ttu-id="b92dd-165">**FtpOpenFile**</span><span class="sxs-lookup"><span data-stu-id="b92dd-165">**FtpOpenFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | <span data-ttu-id="b92dd-166">Avvia l'accesso a un file nel server per la lettura o la scrittura.</span><span class="sxs-lookup"><span data-stu-id="b92dd-166">Initiates access to a file on the server for either reading or writing.</span></span> <span data-ttu-id="b92dd-167">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-167">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> |
| [<span data-ttu-id="b92dd-168">**FtpPutFile**</span><span class="sxs-lookup"><span data-stu-id="b92dd-168">**FtpPutFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | <span data-ttu-id="b92dd-169">Scrive un file nel server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-169">Writes a file to the server.</span></span> <span data-ttu-id="b92dd-170">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-170">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                            |
| [<span data-ttu-id="b92dd-171">**FtpRemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="b92dd-171">**FtpRemoveDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | <span data-ttu-id="b92dd-172">Elimina una directory nel server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-172">Deletes a directory on the server.</span></span> <span data-ttu-id="b92dd-173">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-173">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                      |
| [<span data-ttu-id="b92dd-174">**FtpRenameFile**</span><span class="sxs-lookup"><span data-stu-id="b92dd-174">**FtpRenameFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | <span data-ttu-id="b92dd-175">Rinomina un file nel server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-175">Renames a file on the server.</span></span> <span data-ttu-id="b92dd-176">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-176">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                           |
| [<span data-ttu-id="b92dd-177">**FtpSetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="b92dd-177">**FtpSetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | <span data-ttu-id="b92dd-178">Modifica la directory corrente del client nel server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-178">Changes the client's current directory on the server.</span></span> <span data-ttu-id="b92dd-179">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-179">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="b92dd-180">**InternetWriteFile**</span><span class="sxs-lookup"><span data-stu-id="b92dd-180">**InternetWriteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | <span data-ttu-id="b92dd-181">Scrive i dati in un file aperto nel server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-181">Writes data to an open file on the server.</span></span> <span data-ttu-id="b92dd-182">Questa funzione richiede un handle creato da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span><span class="sxs-lookup"><span data-stu-id="b92dd-182">This function requires a handle created by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span></span>                                      |



 

### <a name="starting-an-ftp-session"></a><span data-ttu-id="b92dd-183">Avvio di una sessione FTP</span><span class="sxs-lookup"><span data-stu-id="b92dd-183">Starting an FTP Session</span></span>

<span data-ttu-id="b92dd-184">L'applicazione stabilisce una sessione FTP chiamando [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) su un handle creato da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="b92dd-184">The application establishes an FTP session by calling [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) on a handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="b92dd-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) richiede il nome del server, il numero di porta, il nome utente, la password e il tipo di servizio (che deve essere impostato su \_ FTP servizio Internet \_ ).</span><span class="sxs-lookup"><span data-stu-id="b92dd-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) needs the server name, port number, user name, password, and service type (which must be set to INTERNET\_SERVICE\_FTP).</span></span> <span data-ttu-id="b92dd-186">Per la semantica FTP passiva, l'applicazione deve impostare anche il flag del [ \_ flag \_ passivo Internet](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="b92dd-186">For passive FTP semantics, the application must also set the [INTERNET\_FLAG\_PASSIVE](api-flags.md) flag.</span></span>

<span data-ttu-id="b92dd-187">\_ \_ \_ \_ \_ \_ Per il numero di porta è possibile utilizzare la porta FTP predefinita Internet e i valori numerici di porta Internet non validi.</span><span class="sxs-lookup"><span data-stu-id="b92dd-187">The INTERNET\_DEFAULT\_FTP\_PORT and INTERNET\_INVALID\_PORT\_NUMBER values can be used for the port number.</span></span> <span data-ttu-id="b92dd-188">\_La porta FTP predefinita Internet \_ \_ Usa la porta FTP predefinita, ma è ancora necessario impostare il tipo di servizio.</span><span class="sxs-lookup"><span data-stu-id="b92dd-188">INTERNET\_DEFAULT\_FTP\_PORT uses the default FTP port, but the service type still must be set.</span></span> <span data-ttu-id="b92dd-189">\_ \_ Numero di porta non valido Internet \_ Usa il valore predefinito per il tipo di servizio indicato.</span><span class="sxs-lookup"><span data-stu-id="b92dd-189">INTERNET\_INVALID\_PORT\_NUMBER uses the default value for the indicated service type.</span></span>

<span data-ttu-id="b92dd-190">I valori per nome utente e password possono essere impostati su **null**.</span><span class="sxs-lookup"><span data-stu-id="b92dd-190">The values for the user name and password can be set to **NULL**.</span></span> <span data-ttu-id="b92dd-191">Se entrambi i valori sono impostati su **null**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) USA "Anonymous" per il nome utente e l'indirizzo di posta elettronica dell'utente per la password.</span><span class="sxs-lookup"><span data-stu-id="b92dd-191">If both values are set to **NULL**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses "anonymous" for the user name, and the user's email address for the password.</span></span> <span data-ttu-id="b92dd-192">Se solo la password è impostata su **null**, il nome utente passato a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) viene usato per il nome utente e per la password viene usata una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="b92dd-192">If only the password is set to **NULL**, the user name passed to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) is used for the user name, and an empty string is used for the password.</span></span> <span data-ttu-id="b92dd-193">Se nessuno dei due valori è **null**, vengono usati il nome utente e la password assegnati a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .</span><span class="sxs-lookup"><span data-stu-id="b92dd-193">If neither value is **NULL**, the user name and password given to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) are used.</span></span>

### <a name="enumerating-directories"></a><span data-ttu-id="b92dd-194">Enumerazione delle directory</span><span class="sxs-lookup"><span data-stu-id="b92dd-194">Enumerating Directories</span></span>

<span data-ttu-id="b92dd-195">L'enumerazione di una directory in un server FTP richiede la creazione di un handle da parte di [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="b92dd-195">Enumeration of a directory on an FTP server requires the creation of a handle by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="b92dd-196">Questo handle è un ramo dell'handle di sessione creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-196">This handle is a branch of the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="b92dd-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) individua il primo file o directory sul server e lo restituisce in una struttura di [**\_ \_ dati Find Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) .</span><span class="sxs-lookup"><span data-stu-id="b92dd-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) locates the first file or directory on the server and returns it in a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="b92dd-198">Utilizzare [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) fino a quando non viene restituito [**un errore di \_ \_ altri \_ file**](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b92dd-198">Use [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until it returns [**ERROR\_NO\_MORE\_FILES**](wininet-errors.md).</span></span> <span data-ttu-id="b92dd-199">Questo metodo trova tutti i file e le directory successivi nel server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-199">This method finds all subsequent files and directories on the server.</span></span> <span data-ttu-id="b92dd-200">Per ulteriori informazioni su [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), vedere [la pagina relativa alla ricerca del file successivo](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b92dd-200">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="b92dd-201">Per determinare se il file recuperato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) o [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) è una directory, controllare il membro **dwFileAttributes** della struttura [**di \_ \_ dati Find Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) per verificare se è uguale alla directory degli \_ attributi di file \_ .</span><span class="sxs-lookup"><span data-stu-id="b92dd-201">To determine if the file retrieved by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) or [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) is a directory, check the **dwFileAttributes** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure to see if it is equal to FILE\_ATTRIBUTE\_DIRECTORY.</span></span>

<span data-ttu-id="b92dd-202">Se l'applicazione apporta modifiche al server FTP o se il server FTP viene modificato di frequente, [il \_ flag Internet nessun flag di \_ \_ \_ scrittura della cache](api-flags.md) e di [ \_ \_ ricaricamento del flag Internet](api-flags.md) deve essere impostato in [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="b92dd-202">If the application makes changes on the FTP server or if the FTP server changes frequently, the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) and [INTERNET\_FLAG\_RELOAD](api-flags.md) flags should be set in [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="b92dd-203">Questi flag assicurano che le informazioni di directory recuperate dal server FTP siano aggiornate.</span><span class="sxs-lookup"><span data-stu-id="b92dd-203">These flags ensure that the directory information being retrieved from the FTP server is current.</span></span>

<span data-ttu-id="b92dd-204">Al termine dell'enumerazione di directory da parte dell'applicazione, l'applicazione deve effettuare una chiamata a [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) sull'handle creato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="b92dd-204">After the application completes the directory enumeration, the application must make a call to [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle created by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="b92dd-205">Fino a quando l'handle non viene chiuso, l'applicazione non può chiamare nuovamente [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) sull'handle di sessione creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-205">Until that handle is closed, the application cannot call [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) again on the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="b92dd-206">Se viene eseguita una chiamata a [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) nello stesso handle di sessione prima della chiusura della precedente chiamata alla stessa funzione, la funzione ha esito negativo, restituendo l' [errore \_ \_ trasferimento FTP \_ in \_ corso](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b92dd-206">If a call to [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) is made on the same session handle before the previous call to the same function is closed, the function fails, returning [ERROR\_FTP\_TRANSFER\_IN\_PROGRESS](wininet-errors.md).</span></span>

<span data-ttu-id="b92dd-207">Nell'esempio seguente viene enumerato il contenuto di una directory FTP in un controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b92dd-207">The following example enumerates the contents of an FTP directory into a list box control.</span></span> <span data-ttu-id="b92dd-208">Il parametro *hConnection* è un handle restituito dalla funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo che è stata stabilita una sessione FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-208">The *hConnection* parameter is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span> <span data-ttu-id="b92dd-209">Il codice sorgente di esempio per la funzione InternetErrorOut a cui si fa riferimento in questo esempio è reperibile nell'argomento [gestione degli errori](appendix-c-handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b92dd-209">Sample source code for the InternetErrorOut function referenced in this example can be found in the [Handling Errors](appendix-c-handling-errors.md)topic.</span></span>


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a><span data-ttu-id="b92dd-210">Esplorazione delle directory</span><span class="sxs-lookup"><span data-stu-id="b92dd-210">Navigating Directories</span></span>

<span data-ttu-id="b92dd-211">Le funzioni [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) e [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) gestiscono la navigazione nella directory.</span><span class="sxs-lookup"><span data-stu-id="b92dd-211">The [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions handle directory navigation.</span></span>

<span data-ttu-id="b92dd-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) restituisce la directory corrente dell'applicazione nel server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) returns the application's current directory on the FTP server.</span></span> <span data-ttu-id="b92dd-213">Il percorso della directory della directory radice sul server FTP è incluso.</span><span class="sxs-lookup"><span data-stu-id="b92dd-213">The directory path from the root directory on the FTP server is included.</span></span>

<span data-ttu-id="b92dd-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) modifica la directory di lavoro nel server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the working directory on the server.</span></span> <span data-ttu-id="b92dd-215">Le informazioni della directory passate a [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) possono essere un nome di percorso parzialmente o completo rispetto alla directory corrente.</span><span class="sxs-lookup"><span data-stu-id="b92dd-215">The directory information passed to [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) can be either a partially or fully qualified path name relative to the current directory.</span></span> <span data-ttu-id="b92dd-216">Ad esempio, se l'applicazione è attualmente nella directory "public/info" e il percorso è "FTP/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) modifica la directory corrente in "public/info/FTP/example".</span><span class="sxs-lookup"><span data-stu-id="b92dd-216">For example, if the application is currently in the directory "public/info" and the path is "ftp/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the current directory to "public/info/ftp/example".</span></span>

<span data-ttu-id="b92dd-217">Nell'esempio seguente viene utilizzato l'handle di sessione FTP hConnection, restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="b92dd-217">The following example uses the FTP session handle hConnection, which is returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="b92dd-218">Il nome della nuova directory viene tratto dalla casella di modifica della finestra di dialogo padre il cui IDC viene passato nel parametro *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="b92dd-218">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="b92dd-219">Prima che venga apportata la modifica alla directory, la funzione recupera la directory corrente e la archivia nella stessa casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="b92dd-219">Before the directory change is made, the function retrieves the current directory and stores it in the same edit box.</span></span> <span data-ttu-id="b92dd-220">Il codice origine per la funzione DisplayFtpDir chiamata alla fine è elencato sopra.</span><span class="sxs-lookup"><span data-stu-id="b92dd-220">The souce code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a><span data-ttu-id="b92dd-221">Manipolazione di directory in un server FTP</span><span class="sxs-lookup"><span data-stu-id="b92dd-221">Manipulating Directories on an FTP Server</span></span>

<span data-ttu-id="b92dd-222">WinINet fornisce la possibilità di creare e rimuovere directory in un server FTP a cui l'applicazione dispone dei privilegi necessari.</span><span class="sxs-lookup"><span data-stu-id="b92dd-222">WinINet provides the capability to create and remove directories on an FTP server to which the application has the necessary privileges.</span></span> <span data-ttu-id="b92dd-223">Se l'applicazione deve accedere a un server con un nome utente e una password specifici, i valori possono essere utilizzati in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) durante la creazione dell'handle della sessione FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-223">If the application must log on to a server with a specific user name and password, the values can be used in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) when creating the FTP session handle.</span></span>

<span data-ttu-id="b92dd-224">La funzione [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) accetta un handle di sessione FTP valido e una stringa con terminazione **null** che contiene un percorso completo o un nome relativo alla directory corrente e crea una directory nel server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-224">The [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function takes a valid FTP session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and creates a directory on the FTP server.</span></span>

<span data-ttu-id="b92dd-225">Nell'esempio seguente vengono illustrate due chiamate separate a [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span><span class="sxs-lookup"><span data-stu-id="b92dd-225">The following example shows two separate calls to [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span></span> <span data-ttu-id="b92dd-226">In entrambi gli esempi, hFtpSession è l'handle di sessione creato dalla funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e la directory radice è la directory corrente.</span><span class="sxs-lookup"><span data-stu-id="b92dd-226">In both examples, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span>

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

<span data-ttu-id="b92dd-227">La funzione [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) accetta un handle di sessione e una stringa con terminazione **null** che contiene un percorso completo o un nome relativo alla directory corrente e rimuove tale directory dal server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-227">The [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) function takes a session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and removes that directory from the FTP server.</span></span>

<span data-ttu-id="b92dd-228">Nell'esempio seguente vengono illustrate due chiamate di esempio a [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span><span class="sxs-lookup"><span data-stu-id="b92dd-228">The following example shows two sample calls to [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span></span> <span data-ttu-id="b92dd-229">In entrambe le chiamate, hFtpSession è l'handle di sessione creato dalla funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e la directory radice è la directory corrente.</span><span class="sxs-lookup"><span data-stu-id="b92dd-229">In both calls, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span> <span data-ttu-id="b92dd-230">Nella directory radice è presente una directory denominata "test" e una directory denominata "example" nella directory "test".</span><span class="sxs-lookup"><span data-stu-id="b92dd-230">There is a directory called "test" in the root directory and a directory called "example" in the "test" directory.</span></span>

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



<span data-ttu-id="b92dd-231">Nell'esempio seguente viene creata una nuova directory sul server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-231">The following example creates a new directory on the FTP server.</span></span> <span data-ttu-id="b92dd-232">Il nome della nuova directory viene tratto dalla casella di modifica della finestra di dialogo padre il cui IDC viene passato nel parametro *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="b92dd-232">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="b92dd-233">L'handle *hConnection* è stato creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-233">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="b92dd-234">Il codice sorgente per la funzione DisplayFtpDir chiamata alla fine è elencato sopra.</span><span class="sxs-lookup"><span data-stu-id="b92dd-234">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



<span data-ttu-id="b92dd-235">Nell'esempio seguente viene eliminata una directory dal server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-235">The following example deletes a directory from the FTP server.</span></span> <span data-ttu-id="b92dd-236">Il nome della directory da eliminare viene ricavato dalla casella di modifica nella finestra di dialogo padre il cui IDC viene passato nel parametro *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="b92dd-236">The name of the directory to be deleted is taken from the edit box in the parent dialog whose IDC is passed into the *nDirNameId* parameter.</span></span> <span data-ttu-id="b92dd-237">L'handle *hConnection* è stato creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-237">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="b92dd-238">Il codice sorgente per la funzione DisplayFtpDir chiamata alla fine è elencato sopra.</span><span class="sxs-lookup"><span data-stu-id="b92dd-238">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a><span data-ttu-id="b92dd-239">Recupero di file in un server FTP</span><span class="sxs-lookup"><span data-stu-id="b92dd-239">Getting Files on an FTP Server</span></span>

<span data-ttu-id="b92dd-240">Sono disponibili tre metodi per il recupero di file da un server FTP:</span><span class="sxs-lookup"><span data-stu-id="b92dd-240">There are three methods for retrieving files from an FTP server:</span></span>

-   <span data-ttu-id="b92dd-241">Utilizzare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="b92dd-241">Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="b92dd-242">Utilizzare [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="b92dd-242">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="b92dd-243">Usare [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span><span class="sxs-lookup"><span data-stu-id="b92dd-243">Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span></span>

<span data-ttu-id="b92dd-244">Per ulteriori informazioni sull'utilizzo della funzione [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) , vedere la pagina relativa alla [lettura di file](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b92dd-244">For more information about using the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function, see [Reading Files](common-functions.md).</span></span>

<span data-ttu-id="b92dd-245">Se l'URL del file è disponibile, l'applicazione può chiamare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) per connettersi a tale URL, quindi usare [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) per controllare il download del file.</span><span class="sxs-lookup"><span data-stu-id="b92dd-245">If the URL of the file is available, the application can call [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to connect to that URL, then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to control the download of the file.</span></span> <span data-ttu-id="b92dd-246">In questo modo, l'applicazione può controllare più rigorosamente il download ed è ideale per le situazioni in cui non è necessario effettuare altre operazioni sul server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-246">This allows the application tighter control over the download and is ideal for situations where no other operations need to be made on the FTP server.</span></span> <span data-ttu-id="b92dd-247">Per altre informazioni su come accedere direttamente alle risorse, vedere [accesso diretto agli URL](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="b92dd-247">For more information about how to directly access resources, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="b92dd-248">Se l'applicazione ha stabilito un handle di sessione FTP per il server con [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), l'applicazione può chiamare [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) con il nome file esistente e con un nuovo nome per il file archiviato localmente.</span><span class="sxs-lookup"><span data-stu-id="b92dd-248">If the application has established an FTP session handle to the server with [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), the application can call [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with the existing file name and with a new name for the locally stored file.</span></span> <span data-ttu-id="b92dd-249">L'applicazione può quindi usare [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) per scaricare il file.</span><span class="sxs-lookup"><span data-stu-id="b92dd-249">The application can then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to download the file.</span></span> <span data-ttu-id="b92dd-250">Questo consente all'applicazione di controllare più rigorosamente il download e di mantenere la connessione al server FTP, in modo da poter eseguire più comandi.</span><span class="sxs-lookup"><span data-stu-id="b92dd-250">This allows the application tighter control over the download and keeps the connection to the FTP server, so more commands can be executed.</span></span>

<span data-ttu-id="b92dd-251">Se l'applicazione non necessita di un controllo rigoroso sul download, l'applicazione può utilizzare [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) con l'handle della sessione FTP, il nome del file remoto e il nome del file locale per recuperare il file.</span><span class="sxs-lookup"><span data-stu-id="b92dd-251">If the application does not need tight control over the download, the application can use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) with the FTP session handle, remote file name, and local file name to retrieve the file.</span></span> <span data-ttu-id="b92dd-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) esegue tutte le operazioni di contabilità e sovraccarico associate alla lettura di un file da un server FTP e all'archiviazione locale.</span><span class="sxs-lookup"><span data-stu-id="b92dd-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) performs all the bookkeeping and overhead associated with reading a file from an FTP server and storing it locally.</span></span>

<span data-ttu-id="b92dd-253">Nell'esempio seguente viene recuperato un file da un server FTP e salvato localmente.</span><span class="sxs-lookup"><span data-stu-id="b92dd-253">The following example retrieves a file from an FTP server and saves it locally.</span></span> <span data-ttu-id="b92dd-254">Il nome del file nel server FTP viene ricavato dalla casella di modifica nella finestra di dialogo padre il cui IDC viene passato nel parametro *nFtpFileNameId* e il nome locale con cui il file viene salvato viene ricavato dalla casella di modifica il cui IDC viene passato nel parametro *nLocalFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="b92dd-254">The name of the file on the FTP server is taken from the edit box in the parent dialog whose IDC is passed in the *nFtpFileNameId* parameter, and the local name under which the file is saved is taken from the edit box whose IDC is passed in the *nLocalFileNameId* parameter.</span></span> <span data-ttu-id="b92dd-255">L'handle *hConnection* è stato creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-255">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a><span data-ttu-id="b92dd-256">Inserimento di file in un server FTP</span><span class="sxs-lookup"><span data-stu-id="b92dd-256">Placing Files on an FTP Server</span></span>

<span data-ttu-id="b92dd-257">Esistono due metodi per inserire un file in un server FTP:</span><span class="sxs-lookup"><span data-stu-id="b92dd-257">There are two methods for placing a file on an FTP server:</span></span>

-   <span data-ttu-id="b92dd-258">Usare [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) con [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span><span class="sxs-lookup"><span data-stu-id="b92dd-258">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span></span>
-   <span data-ttu-id="b92dd-259">Usare [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="b92dd-259">Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>

<span data-ttu-id="b92dd-260">Un'applicazione che deve inviare dati a un server FTP, ma non dispone di un file locale che contiene tutti i dati, deve usare [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) per creare e aprire un file nel server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-260">An application that must send data to an FTP server, but does not have a local file that contains all the data, should use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) to create and open a file on the ftp server.</span></span> <span data-ttu-id="b92dd-261">L'applicazione può quindi usare [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) per caricare le informazioni nel file.</span><span class="sxs-lookup"><span data-stu-id="b92dd-261">The application then can use [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) to upload the information to the file.</span></span>

<span data-ttu-id="b92dd-262">Se il file esiste già localmente, l'applicazione può usare [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) per caricare il file nel server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-262">If the file already exists locally, the application can use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) to upload the file to the FTP server.</span></span> <span data-ttu-id="b92dd-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) esegue tutto il sovraccarico associato al caricamento di un file locale in un server FTP remoto.</span><span class="sxs-lookup"><span data-stu-id="b92dd-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) performs all the overhead that goes with uploading a local file to a remote FTP server.</span></span>

<span data-ttu-id="b92dd-264">Nell'esempio seguente viene copiato un file locale nel server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-264">The following example copies a local file onto the FTP server.</span></span> <span data-ttu-id="b92dd-265">Il nome locale del file viene ricavato dalla casella di modifica nella finestra di dialogo padre il cui IDC viene passato nel parametro *nLocalFileNameId* e il nome con cui il file viene salvato nel server FTP viene ricavato dalla casella di modifica il cui IDC viene passato nel parametro *nFtpFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="b92dd-265">The local name of the file is taken from the edit box in the parent dialog whose IDC is passed in the *nLocalFileNameId* parameter, and the name under which the file is saved on the FTP server is taken from the edit box whose IDC is passed in the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="b92dd-266">L'handle *hConnection* è stato creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-266">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a><span data-ttu-id="b92dd-267">Eliminazione di file da un server FTP</span><span class="sxs-lookup"><span data-stu-id="b92dd-267">Deleting Files from an FTP Server</span></span>

<span data-ttu-id="b92dd-268">Per eliminare un file da un server FTP, utilizzare la funzione [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) .</span><span class="sxs-lookup"><span data-stu-id="b92dd-268">To delete a file from an FTP server, use the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="b92dd-269">L'applicazione chiamante deve disporre dei privilegi necessari per eliminare un file dal server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-269">The calling application must have the necessary privileges to delete a file from the FTP server.</span></span>

<span data-ttu-id="b92dd-270">Nell'esempio seguente viene eliminato un file dal server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-270">The following example deletes a file from the FTP server.</span></span> <span data-ttu-id="b92dd-271">Il nome del file da eliminare viene ricavato dalla casella di modifica nella finestra di dialogo padre a cui IDC viene passato int il parametro *nFtpFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="b92dd-271">The name of the file to be deleted is taken from the edit box in the parent dialog whose IDC is passed int the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="b92dd-272">L'handle *hConnection* è stato creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-272">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="b92dd-273">Poiché questa funzione non aggiorna gli elenchi di file o la visualizzazione della directory, il processo chiamante deve eseguire questa operazione al completamento dell'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="b92dd-273">Since this function does not refresh file listings or directory display, the calling process should do so upon successful deletion.</span></span>


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a><span data-ttu-id="b92dd-274">Ridenominazione di file e directory in un server FTP</span><span class="sxs-lookup"><span data-stu-id="b92dd-274">Renaming Files and Directories on an FTP Server</span></span>

<span data-ttu-id="b92dd-275">I file e le directory in un server FTP possono essere rinominati tramite la funzione [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) .</span><span class="sxs-lookup"><span data-stu-id="b92dd-275">Files and directories on an FTP server can be renamed using the [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) function.</span></span> <span data-ttu-id="b92dd-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accetta due stringhe con terminazione **null** che contengono nomi parzialmente o completi rispetto alla directory corrente.</span><span class="sxs-lookup"><span data-stu-id="b92dd-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accepts two **null**-terminated strings that contain either partially or fully qualified names relative to the current directory.</span></span> <span data-ttu-id="b92dd-277">La funzione modifica il nome del file designato dalla prima stringa nel nome definito dalla seconda stringa.</span><span class="sxs-lookup"><span data-stu-id="b92dd-277">The function changes the name of the file designated by the first string to the name designated by the second string.</span></span>

<span data-ttu-id="b92dd-278">Nell'esempio seguente viene rinominato un file o una directory nel server FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-278">The following example renames a file or directory on the FTP server.</span></span> <span data-ttu-id="b92dd-279">Il nome corrente del file o della directory viene ricavato dalla casella di modifica nella finestra di dialogo padre il cui IDC viene passato nel parametro *nOldFileNameId* e il nuovo nome viene ricavato dalla casella di modifica il cui IDC viene passato nel parametro *nNewFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="b92dd-279">The current name of the file or directory is taken from the edit box in the parent dialog whose IDC is passed in the *nOldFileNameId* parameter, and the new name is taken from the edit box whose IDC is passed in the *nNewFileNameId* parameter.</span></span> <span data-ttu-id="b92dd-280">L'handle *hConnection* è stato creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo aver stabilito una sessione FTP.</span><span class="sxs-lookup"><span data-stu-id="b92dd-280">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="b92dd-281">Poiché questa funzione non aggiorna gli elenchi di file o la visualizzazione della directory, il processo chiamante deve eseguire questa operazione al completamento della ridenominazione.</span><span class="sxs-lookup"><span data-stu-id="b92dd-281">Since this function does not refresh file listings or directory display, the calling process should do so upon successful renaming.</span></span>


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> <span data-ttu-id="b92dd-282">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="b92dd-282">WinINet does not support server implementations.</span></span> <span data-ttu-id="b92dd-283">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="b92dd-283">In addition, it should not be used from a service.</span></span> <span data-ttu-id="b92dd-284">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="b92dd-284">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 