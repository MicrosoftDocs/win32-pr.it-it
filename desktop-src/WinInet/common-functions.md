---
title: Funzioni comuni (Windows Internet)
description: I diversi protocolli Internet (ad esempio FTP e http) utilizzano diverse funzioni WinINet per gestire le informazioni su Internet.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1893b085da1b3e77228e4a9abf75acc166d84726
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300794"
---
# <a name="common-functions-windows-internet"></a><span data-ttu-id="8b16a-103">Funzioni comuni (Windows Internet)</span><span class="sxs-lookup"><span data-stu-id="8b16a-103">Common Functions (Windows Internet)</span></span>

<span data-ttu-id="8b16a-104">I diversi protocolli Internet (ad esempio FTP e http) utilizzano diverse funzioni WinINet per gestire le informazioni su Internet.</span><span class="sxs-lookup"><span data-stu-id="8b16a-104">The different Internet protocols (such as ftp and http) use several of the same WinINet functions to handle information on the Internet.</span></span> <span data-ttu-id="8b16a-105">Queste funzioni comuni gestiscono le attività in modo coerente, indipendentemente dal protocollo specifico a cui vengono applicate.</span><span class="sxs-lookup"><span data-stu-id="8b16a-105">These common functions handle their tasks in a consistent manner, regardless of the particular protocol to which they are being applied.</span></span> <span data-ttu-id="8b16a-106">Le applicazioni possono utilizzare queste funzioni per creare funzioni generiche che gestiscono le attività nei diversi protocolli, ad esempio la lettura dei file per FTP e http.</span><span class="sxs-lookup"><span data-stu-id="8b16a-106">Applications can use these functions to create general-purpose functions that handle tasks across the different protocols (such as reading files for ftp and http).</span></span>

<span data-ttu-id="8b16a-107">Le funzioni comuni gestiscono le seguenti attività:</span><span class="sxs-lookup"><span data-stu-id="8b16a-107">The common functions handle the following tasks:</span></span>

-   <span data-ttu-id="8b16a-108">Download delle risorse da Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)e [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span><span class="sxs-lookup"><span data-stu-id="8b16a-108">Downloading resources from the Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), and [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span></span>
-   <span data-ttu-id="8b16a-109">Impostazione delle operazioni asincrone ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span><span class="sxs-lookup"><span data-stu-id="8b16a-109">Setting up asynchronous operations ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span></span>
-   <span data-ttu-id="8b16a-110">Visualizzazione e modifica delle opzioni ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span><span class="sxs-lookup"><span data-stu-id="8b16a-110">Viewing and changing options ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span></span>
-   <span data-ttu-id="8b16a-111">Chiusura di tutti i tipi di handle [**HINTERNET**](appendix-a-hinternet-handles.md) ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span><span class="sxs-lookup"><span data-stu-id="8b16a-111">Closing all types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span></span>
-   <span data-ttu-id="8b16a-112">Inserimento e rimozione di blocchi sulle risorse ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) e [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span><span class="sxs-lookup"><span data-stu-id="8b16a-112">Placing and removing locks on resources ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) and [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span></span>

## <a name="using-common-functions"></a><span data-ttu-id="8b16a-113">Uso di funzioni comuni</span><span class="sxs-lookup"><span data-stu-id="8b16a-113">Using Common Functions</span></span>

<span data-ttu-id="8b16a-114">Nella tabella seguente sono elencate le funzioni comuni incluse nelle funzioni WinINet.</span><span class="sxs-lookup"><span data-stu-id="8b16a-114">The following table lists the common functions included in the WinINet functions.</span></span> <span data-ttu-id="8b16a-115">Le funzioni comuni possono essere utilizzate su diversi tipi di handle [**HINTERNET**](appendix-a-hinternet-handles.md) oppure possono essere utilizzate durante diversi tipi di sessioni.</span><span class="sxs-lookup"><span data-stu-id="8b16a-115">The common functions can be used on different types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles or can be used during different types of sessions.</span></span>



| <span data-ttu-id="8b16a-116">Funzione</span><span class="sxs-lookup"><span data-stu-id="8b16a-116">Function</span></span>                                                         | <span data-ttu-id="8b16a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b16a-117">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b16a-118">**InternetFindNextFile**</span><span class="sxs-lookup"><span data-stu-id="8b16a-118">**InternetFindNextFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | <span data-ttu-id="8b16a-119">Continua l'enumerazione o la ricerca di file.</span><span class="sxs-lookup"><span data-stu-id="8b16a-119">Continues file enumeration or search.</span></span> <span data-ttu-id="8b16a-120">Richiede un handle creato dalla funzione [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-120">Requires a handle created by the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span>                                                                            |
| [<span data-ttu-id="8b16a-121">**InternetLockRequestFile**</span><span class="sxs-lookup"><span data-stu-id="8b16a-121">**InternetLockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | <span data-ttu-id="8b16a-122">Consente all'utente di inserire un blocco sul file in uso.</span><span class="sxs-lookup"><span data-stu-id="8b16a-122">Allows the user to place a lock on the file that is being used.</span></span> <span data-ttu-id="8b16a-123">Questa funzione richiede un handle restituito dalla funzione [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-123">This function requires a handle returned by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="8b16a-124">**La InternetQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="8b16a-124">**InternetQueryDataAvailable**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | <span data-ttu-id="8b16a-125">Recupera la quantità di dati disponibili.</span><span class="sxs-lookup"><span data-stu-id="8b16a-125">Retrieves the amount of data available.</span></span> <span data-ttu-id="8b16a-126">Richiede un handle creato dalla funzione [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-126">Requires a handle created by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                                    |
| [<span data-ttu-id="8b16a-127">**InternetQueryOption**</span><span class="sxs-lookup"><span data-stu-id="8b16a-127">**InternetQueryOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | <span data-ttu-id="8b16a-128">Recupera l'impostazione di un'opzione Internet.</span><span class="sxs-lookup"><span data-stu-id="8b16a-128">Retrieves the setting of an Internet option.</span></span>                                                                                                                                                                                                            |
| [<span data-ttu-id="8b16a-129">**InternetReadFile**</span><span class="sxs-lookup"><span data-stu-id="8b16a-129">**InternetReadFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | <span data-ttu-id="8b16a-130">Legge i dati dell'URL.</span><span class="sxs-lookup"><span data-stu-id="8b16a-130">Reads URL data.</span></span> <span data-ttu-id="8b16a-131">Richiede un handle creato dalla funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-131">Requires a handle created by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                |
| [<span data-ttu-id="8b16a-132">**InternetSetFilePointer**</span><span class="sxs-lookup"><span data-stu-id="8b16a-132">**InternetSetFilePointer**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | <span data-ttu-id="8b16a-133">Imposta la posizione per la successiva lettura di un file.</span><span class="sxs-lookup"><span data-stu-id="8b16a-133">Sets the position for the next read in a file.</span></span> <span data-ttu-id="8b16a-134">Richiede un handle creato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo su un URL http) o un handle creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usando il verbo HTTP Get.</span><span class="sxs-lookup"><span data-stu-id="8b16a-134">Requires a handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (on an HTTP URL only) or a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) using the GET HTTP verb.</span></span>                 |
| [<span data-ttu-id="8b16a-135">**InternetSetOption**</span><span class="sxs-lookup"><span data-stu-id="8b16a-135">**InternetSetOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | <span data-ttu-id="8b16a-136">Imposta un'opzione Internet.</span><span class="sxs-lookup"><span data-stu-id="8b16a-136">Sets an Internet option.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="8b16a-137">**InternetSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="8b16a-137">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | <span data-ttu-id="8b16a-138">Imposta una funzione di callback che riceve informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="8b16a-138">Sets a callback function that receives status information.</span></span> <span data-ttu-id="8b16a-139">Assegna una funzione di callback all'handle [**HINTERNET**](appendix-a-hinternet-handles.md) designato e a tutti gli handle derivati da esso.</span><span class="sxs-lookup"><span data-stu-id="8b16a-139">Assigns a callback function to the designated [**HINTERNET**](appendix-a-hinternet-handles.md) handle and all handles derived from it.</span></span>                                                      |
| [<span data-ttu-id="8b16a-140">**InternetUnlockRequestFile**</span><span class="sxs-lookup"><span data-stu-id="8b16a-140">**InternetUnlockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | <span data-ttu-id="8b16a-141">Sblocca un file bloccato mediante la funzione [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-141">Unlocks a file that was locked using the [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function.</span></span>                                                                                                                                           |



 

<span data-ttu-id="8b16a-142">La lettura dei file, la ricerca del file successivo, la modifica delle opzioni e la configurazione delle operazioni asincrone sono comuni alle funzioni che supportano vari protocolli e tipi di handle [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-142">Reading files, finding the next file, manipulating options, and setting up asynchronous operations are common to the functions that support various protocols and [**HINTERNET**](appendix-a-hinternet-handles.md) handle types.</span></span>

### <a name="reading-files"></a><span data-ttu-id="8b16a-143">Lettura di file</span><span class="sxs-lookup"><span data-stu-id="8b16a-143">Reading Files</span></span>

<span data-ttu-id="8b16a-144">La funzione [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) viene usata per scaricare le risorse da un handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituito dalla funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-144">The [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function is used to download resources from an [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>

<span data-ttu-id="8b16a-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accetta una variabile puntatore void che contiene l'indirizzo di un buffer e un puntatore a una variabile che contiene la lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="8b16a-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accepts a void pointer variable that contains the address of a buffer and a pointer to a variable that contains the length of the buffer.</span></span> <span data-ttu-id="8b16a-146">La funzione restituisce i dati nel buffer e la quantità di dati scaricati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="8b16a-146">The function returns the data in the buffer and the amount of data downloaded into the buffer.</span></span>

<span data-ttu-id="8b16a-147">Le funzioni WinINet forniscono due tecniche per scaricare un'intera risorsa:</span><span class="sxs-lookup"><span data-stu-id="8b16a-147">The WinINet functions provide two techniques to download an entire resource:</span></span>

-   <span data-ttu-id="8b16a-148">Funzione [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-148">The [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) function.</span></span>
-   <span data-ttu-id="8b16a-149">Valori restituiti di [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="8b16a-149">The return values of [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>

<span data-ttu-id="8b16a-150">[**La InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) accetta l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (dopo che è stato chiamato [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) sull'handle) e restituisce il numero di byte disponibili.</span><span class="sxs-lookup"><span data-stu-id="8b16a-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) has been called on the handle) and returns the number of bytes available.</span></span> <span data-ttu-id="8b16a-151">L'applicazione deve allocare un buffer uguale al numero di byte disponibili, più 1 per il carattere **null** di terminazione e usare tale buffer con [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="8b16a-151">The application should allocate a buffer equal to the number of bytes available, plus 1 for the terminating **null** character, and use that buffer with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="8b16a-152">Questo metodo non sempre funziona perché [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) sta controllando le dimensioni del file elencate nell'intestazione e non il file effettivo.</span><span class="sxs-lookup"><span data-stu-id="8b16a-152">This method does not always work because [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) is checking the file size listed in the header and not the actual file.</span></span> <span data-ttu-id="8b16a-153">Le informazioni nel file di intestazione potrebbero essere obsolete oppure il file di intestazione potrebbe essere mancante, perché non è attualmente richiesto in tutti gli standard.</span><span class="sxs-lookup"><span data-stu-id="8b16a-153">The information in the header file could be outdated, or the header file could be missing, since it is not currently required under all standards.</span></span>

<span data-ttu-id="8b16a-154">Nell'esempio seguente viene letto il contenuto della risorsa a cui si accede tramite l'handle hResource e visualizzato nella casella di modifica indicata da intCtrlID.</span><span class="sxs-lookup"><span data-stu-id="8b16a-154">The following example reads the contents of the resource accessed by the hResource handle and displayed in the edit box indicated by intCtrlID.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    // Return.
    return TRUE;
}
```



<span data-ttu-id="8b16a-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) restituisce zero byte letti e viene completato correttamente quando tutti i dati disponibili sono stati letti.</span><span class="sxs-lookup"><span data-stu-id="8b16a-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) returns zero bytes read and completes successfully when all available data has been read.</span></span> <span data-ttu-id="8b16a-156">In questo modo un'applicazione può usare [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) in un ciclo per scaricare i dati e uscire quando restituisce zero byte letti e viene completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8b16a-156">This allows an application to use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) in a loop to download the data and exit when it returns zero bytes read and completes successfully.</span></span>

<span data-ttu-id="8b16a-157">Nell'esempio seguente viene letta la risorsa da Internet e viene visualizzata la risorsa nella casella di modifica indicata da intCtrlID.</span><span class="sxs-lookup"><span data-stu-id="8b16a-157">The following example reads the resource from the Internet and displays the resource in the edit box indicated by intCtrlID.</span></span> <span data-ttu-id="8b16a-158">L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) , HINTERNET, è stato restituito [**da InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (dopo essere stato inviato da [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span><span class="sxs-lookup"><span data-stu-id="8b16a-158">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hInternet, was returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after being sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span></span>


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a><span data-ttu-id="8b16a-159">Ricerca del file successivo</span><span class="sxs-lookup"><span data-stu-id="8b16a-159">Finding the Next File</span></span>

<span data-ttu-id="8b16a-160">La funzione [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) viene usata per trovare il file successivo in una ricerca di file, usando i parametri di ricerca e l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="8b16a-160">The [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) function is used to find the next file in a file search, using the search parameters and [**HINTERNET**](appendix-a-hinternet-handles.md) handle from [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="8b16a-161">Per completare una ricerca di file, continuare a chiamare [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) usando l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituito da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) fino a quando la funzione non riesce e il messaggio di errore esteso [non genera \_ \_ più \_ file](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="8b16a-161">To complete a file search, continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) using the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) until the function fails with the extended error message [ERROR\_NO\_MORE\_FILES](wininet-errors.md).</span></span> <span data-ttu-id="8b16a-162">Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-162">To get the extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="8b16a-163">Nell'esempio seguente viene visualizzato il contenuto di una directory FTP nella casella di riepilogo indicata da lstDirectory.</span><span class="sxs-lookup"><span data-stu-id="8b16a-163">The following example displays the contents of an FTP directory in the list box indicated by lstDirectory.</span></span> <span data-ttu-id="8b16a-164">L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) , hConnect, è un handle restituito dalla funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) dopo che è stata stabilita una sessione FTP.</span><span class="sxs-lookup"><span data-stu-id="8b16a-164">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hConnect, is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span>


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a><span data-ttu-id="8b16a-165">Modifica di opzioni</span><span class="sxs-lookup"><span data-stu-id="8b16a-165">Manipulating Options</span></span>

<span data-ttu-id="8b16a-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) vengono usati per modificare le opzioni di WinInet.</span><span class="sxs-lookup"><span data-stu-id="8b16a-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) are used to manipulate the WinINet options.</span></span>

<span data-ttu-id="8b16a-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accetta una variabile che indica l'opzione da impostare, un buffer per contenere l'impostazione dell'opzione e un puntatore che contiene l'indirizzo della variabile che contiene la lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="8b16a-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accepts a variable that indicates the option to set, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

<span data-ttu-id="8b16a-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accetta una variabile che indica l'opzione da recuperare, un buffer per contenere l'impostazione dell'opzione e un puntatore che contiene l'indirizzo della variabile che contiene la lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="8b16a-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accepts a variable that indicates the option to retrieve, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

### <a name="setting-up-asynchronous-operations"></a><span data-ttu-id="8b16a-169">Impostazione delle operazioni asincrone</span><span class="sxs-lookup"><span data-stu-id="8b16a-169">Setting Up Asynchronous Operations</span></span>

<span data-ttu-id="8b16a-170">Per impostazione predefinita, le funzioni WinINet funzionano in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="8b16a-170">By default, the WinINet functions operate synchronously.</span></span> <span data-ttu-id="8b16a-171">Un'applicazione può richiedere un'operazione asincrona impostando il flag [ \_ \_ Async del flag Internet](api-flags.md) nella chiamata alla funzione [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-171">An application can request asynchronous operation by setting the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in the call to the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function.</span></span> <span data-ttu-id="8b16a-172">Tutte le chiamate future eseguite sugli handle derivati dall'handle restituito da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) vengono eseguite in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="8b16a-172">All future calls made against handles derived from the handle returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) are made asynchronously.</span></span>

<span data-ttu-id="8b16a-173">La logica per l'operazione asincrona rispetto a quella sincrona consiste nel consentire a un'applicazione a thread singolo di massimizzare l'utilizzo della CPU senza dover attendere il completamento dell'I/O di rete.</span><span class="sxs-lookup"><span data-stu-id="8b16a-173">The rationale for asynchronous versus synchronous operation is to allow a single-threaded application to maximize its utilization of the CPU without having to wait for network I/O to complete.</span></span> <span data-ttu-id="8b16a-174">Pertanto, a seconda della richiesta, l'operazione può essere completata in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="8b16a-174">Therefore, depending on the request, the operation might complete synchronously or asynchronously.</span></span> <span data-ttu-id="8b16a-175">L'applicazione deve controllare il codice restituito.</span><span class="sxs-lookup"><span data-stu-id="8b16a-175">The application should check the return code.</span></span> <span data-ttu-id="8b16a-176">Se una funzione restituisce **false** o **null** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di i/o \_ \_ in sospeso, la richiesta è stata eseguita in modo asincrono e l'applicazione viene richiamata con la \_ richiesta di stato Internet \_ \_ completata al termine della funzione.</span><span class="sxs-lookup"><span data-stu-id="8b16a-176">If a function returns **FALSE** or **NULL**, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_IO\_PENDING, the request has been made asynchronously, and the application is called back with INTERNET\_STATUS\_REQUEST\_COMPLETE when the function has completed.</span></span>

<span data-ttu-id="8b16a-177">Per avviare l'operazione asincrona, l'applicazione deve impostare il flag [ \_ \_ Async del flag Internet](api-flags.md) nella chiamata a [**internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="8b16a-177">To begin asynchronous operation, the application must set the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in its call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="8b16a-178">L'applicazione deve quindi registrare una funzione di callback valida usando [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="8b16a-178">The application must then register a valid callback function, using [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span></span>

<span data-ttu-id="8b16a-179">Dopo che una funzione di callback è stata registrata per un handle, tutte le operazioni su tale handle possono generare indicazioni sullo stato, a condizione che il valore di contesto fornito quando è stato creato l'handle non sia zero.</span><span class="sxs-lookup"><span data-stu-id="8b16a-179">After a callback function is registered for a handle, all operations on that handle can generate status indications, provided that the context value that was supplied when the handle was created was not zero.</span></span> <span data-ttu-id="8b16a-180">Se si specifica un valore di contesto zero, il completamento di un'operazione viene forzato in modo sincrono, anche se in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)è stato specificato il [ \_ flag Internet \_ asincrono](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-180">Providing a zero context value forces an operation to complete synchronously, even though [INTERNET\_FLAG\_ASYNC](api-flags.md) was specified in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span>

<span data-ttu-id="8b16a-181">Le indicazioni sullo stato forniscono all'applicazione il feedback sullo stato di avanzamento delle operazioni di rete, ad esempio la risoluzione di un nome host, la connessione a un server e la ricezione di dati.</span><span class="sxs-lookup"><span data-stu-id="8b16a-181">Status indications give the application feedback about the progress of network operations, such as resolving a host name, connecting to a server, and receiving data.</span></span> <span data-ttu-id="8b16a-182">Per un handle è possibile effettuare tre indicazioni sullo stato per scopi specifici:</span><span class="sxs-lookup"><span data-stu-id="8b16a-182">Three special-purpose status indications can be made for a handle:</span></span>

-   <span data-ttu-id="8b16a-183">\_ \_ \_ La chiusura dell'handle di stato Internet è l'ultima indicazione di stato eseguita per un handle.</span><span class="sxs-lookup"><span data-stu-id="8b16a-183">INTERNET\_STATUS\_HANDLE\_CLOSING is the last status indication that is made for a handle.</span></span>
-   <span data-ttu-id="8b16a-184">\_ \_ L'handle di stato Internet \_ creato indica quando viene inizialmente creato l'handle.</span><span class="sxs-lookup"><span data-stu-id="8b16a-184">INTERNET\_STATUS\_HANDLE\_CREATED indicates when the handle is initially created.</span></span>
-   <span data-ttu-id="8b16a-185">\_ \_ Richiesta di stato Internet \_ completata indica che un'operazione asincrona è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8b16a-185">INTERNET\_STATUS\_REQUEST\_COMPLETE indicates an asynchronous operation has completed.</span></span>

<span data-ttu-id="8b16a-186">Per determinare se l'operazione ha avuto esito positivo o negativo dopo la ricezione di una richiesta di stato INTERNET, l'applicazione deve controllare la struttura dei [**\_ \_ risultati asincrona di Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8b16a-186">The application must check the [**INTERNET\_ASYNC\_RESULT**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) structure to determine whether the operation succeeded or failed after receiving an INTERNET\_STATUS\_REQUEST\_COMPLETE indication.</span></span>

<span data-ttu-id="8b16a-187">Nell'esempio seguente viene illustrato un esempio di una funzione di callback e una chiamata a [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) per registrare la funzione come funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="8b16a-187">The following sample shows an example of a callback function and a call to [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) to register the function as the callback function.</span></span>


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a><span data-ttu-id="8b16a-188">Chiusura di handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="8b16a-188">Closing HINTERNET Handles</span></span>

<span data-ttu-id="8b16a-189">Tutti gli handle [**HINTERNET**](appendix-a-hinternet-handles.md) possono essere chiusi usando la funzione [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) .</span><span class="sxs-lookup"><span data-stu-id="8b16a-189">All [**HINTERNET**](appendix-a-hinternet-handles.md) handles can be closed by using the [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) function.</span></span> <span data-ttu-id="8b16a-190">È necessario che le applicazioni client chiudano tutti gli handle **HINTERNET** derivati dall'handle **HINTERNET** che tentano di chiudere prima di chiamare [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) sull'handle.</span><span class="sxs-lookup"><span data-stu-id="8b16a-190">Client applications must close all **HINTERNET** handles derived from the **HINTERNET** handle they are trying to close before calling [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle.</span></span>

<span data-ttu-id="8b16a-191">Nell'esempio seguente viene illustrata la gerarchia di handle.</span><span class="sxs-lookup"><span data-stu-id="8b16a-191">The following example illustrates the handle hierarchy.</span></span>


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a><span data-ttu-id="8b16a-192">Blocco e sblocco delle risorse</span><span class="sxs-lookup"><span data-stu-id="8b16a-192">Locking and Unlocking Resources</span></span>

<span data-ttu-id="8b16a-193">La funzione [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) consente a un'applicazione di garantire che la risorsa memorizzata nella cache associata all'handle [**HINTERNET**](appendix-a-hinternet-handles.md) passato non scompaia dalla cache.</span><span class="sxs-lookup"><span data-stu-id="8b16a-193">The [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function allows an application to ensure that the cached resource associated with the [**HINTERNET**](appendix-a-hinternet-handles.md) handle passed to it does not disappear from the cache.</span></span> <span data-ttu-id="8b16a-194">Se un altro download tenta di eseguire il commit di una risorsa con lo stesso URL del file bloccato, la cache evita la rimozione del file eseguendo un'eliminazione sicura.</span><span class="sxs-lookup"><span data-stu-id="8b16a-194">If another download tries to commit a resource that has the same URL as the locked file, the cache avoids removing the file by doing a safe delete.</span></span> <span data-ttu-id="8b16a-195">Quando l'applicazione chiama la funzione [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) , alla cache viene assegnata l'autorizzazione per l'eliminazione del file.</span><span class="sxs-lookup"><span data-stu-id="8b16a-195">After the application calls the [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) function, the cache is given permission to delete the file.</span></span>

<span data-ttu-id="8b16a-196">Se è stato impostato il flag [Internet \_ \_ No \_ cache \_ Write](api-flags.md) o [Internet flag \_ \_ dont \_ cache](api-flags.md) flag, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) crea un file temporaneo con estensione tmp, a meno che l'handle non sia connesso a una risorsa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="8b16a-196">If the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) or [INTERNET\_FLAG\_DONT\_CACHE](api-flags.md) flag has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) creates a temporary file with the extension TMP, unless the handle is connected to an https resource.</span></span> <span data-ttu-id="8b16a-197">Se la funzione accede a una risorsa HTTPS e a un \_ flag Internet \_ non \_ \_ è stata impostata alcuna scrittura nella cache o non \_ \_ è stato impostato alcun flag Internet \_ , [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8b16a-197">If the function accesses an https resource and INTERNET\_FLAG\_NO\_CACHE\_WRITE (or INTERNET\_FLAG\_DONT\_CACHE) has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) fails.</span></span>

> [!Note]  
> <span data-ttu-id="8b16a-198">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="8b16a-198">WinINet does not support server implementations.</span></span> <span data-ttu-id="8b16a-199">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="8b16a-199">In addition, it should not be used from a service.</span></span> <span data-ttu-id="8b16a-200">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="8b16a-200">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
