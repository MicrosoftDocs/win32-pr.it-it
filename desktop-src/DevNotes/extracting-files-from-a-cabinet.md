---
description: Nella sintassi seguente viene illustrata la creazione di un file CAB.
ms.assetid: d9d0e14a-f68c-4b3d-b91d-a3fa824031ea
title: Estrazione di file da un file CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ed62779f97c083fd39af79626d5b79baa6d305
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966041"
---
# <a name="extracting-files-from-a-cabinet"></a><span data-ttu-id="d42b0-103">Estrazione di file da un file CAB</span><span class="sxs-lookup"><span data-stu-id="d42b0-103">Extracting Files from a Cabinet</span></span>

<span data-ttu-id="d42b0-104">Nella sintassi seguente viene illustrata la creazione di un file CAB.</span><span class="sxs-lookup"><span data-stu-id="d42b0-104">The following syntax illustrates the creation of a cabinet.</span></span>

> [!Note]  
> <span data-ttu-id="d42b0-105">Questo codice è solo a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="d42b0-105">This code is for illustrative purposes only.</span></span> <span data-ttu-id="d42b0-106">Per la compilazione, è necessario definire le funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="d42b0-106">To compile, the callback functions must be defined.</span></span>

 

## <a name="example"></a><span data-ttu-id="d42b0-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="d42b0-107">Example</span></span>


```C++
#include <windows.h>
#include <strsafe.h>
#include "fdisample.h"
#include "fdicallbacks.h"

#pragma comment(lib,"cabinet.lib")

//Function prototypes
BOOL ExtractCabinetFiles(
                         LPSTR pszCabinetName, 
                         LPSTR pszCabinetPath,
                         LPSTR pszDestinationDir 
                         );
LPCSTR FDIErrorToString(FDIERROR err);

int main(INT argc, CHAR *argv[])
{
    INT iExitCode = -1;
    HRESULT hr = S_OK;
    HANDLE hFile = INVALID_HANDLE_VALUE;

    LPSTR pszCabinetName = NULL;    //the cabinet name
    LPSTR pszDestinationDir = NULL; //the destination directory
    CHAR pszCabinetPath[MAX_PATH];  //the cabinet path
    
    WIN32_FIND_DATAA findFileData;

    (VOID)HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if ( argc != 3 )
    {
        printf("Usage: %s [cabinet] [destination]\n", argv[0]);
        goto CLEANUP;
    }

    //Split the cabinet name and path

    pszCabinetName = strrchr(argv[1], '\\');

    if ( pszCabinetName == NULL )
    {
        pszCabinetName = argv[1];
        pszCabinetPath[0] = '\0'; 
    }
    else
    {
        pszCabinetName++;
        hr = StringCchCopyA(pszCabinetPath, MAX_PATH, argv[1]);

        if ( SUCCEEDED(hr) )
        {
            pszCabinetPath[(INT)( pszCabinetName - argv[1] )] = '\0';
        }
        else
        {
            printf("Failed to split the cabinet name \"%s\".\n",
                   argv[1]);
            goto CLEANUP;
        }
    }

    pszDestinationDir  = argv[2]; //Destination directory

    //Determine whether the destination directory provided by the user exists

    hFile = FindFirstFileA(pszDestinationDir, &findFileData);

    if ( hFile == INVALID_HANDLE_VALUE )
    {
        printf("Destination directory \"%s\" does not exist.\n", 
               pszDestinationDir);
        goto CLEANUP;
    }
    
    if ( (findFileData.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY) == FALSE )
    {
        printf("Destination, \"%s\", is not a directory.\n", 
               pszDestinationDir);
        goto CLEANUP;
    }

    //Get the files from the cabinet

    if ( ExtractCabinetFiles(pszCabinetName, pszCabinetPath, pszDestinationDir) == TRUE )
    {
        iExitCode = 0;
    }

CLEANUP:

    if ( hFile != INVALID_HANDLE_VALUE )
    {
        FindClose(hFile);
    }

    return iExitCode;
}

BOOL ExtractCabinetFiles(
                         LPSTR pszCabinetName, 
                         LPSTR pszCabinetPath,
                         LPSTR pszDestinationDir 
                         )
{
    ERF  erf;         //FDI error structure
    HFDI hfdi = NULL; //FDI handle
    BOOL bSuccessful = FALSE;

    //Creates the FDI context

    hfdi = FDICreate(fnMemAlloc,  //function to allocate memory
                     fnMemFree,   //function to free memory
                     fnFileOpen,  //function to open a file
                     fnFileRead,  //function to read data from a file
                     fnFileWrite, //function to write data to a file
                     fnFileClose, //function to close a file
                     fnFileSeek,  //function to move the file pointer
              cpuUNKNOWN,  //only used by the 16-bit version of FDI
                     &erf);       //pointer the FDI error structure

    if ( hfdi == NULL )
    {
        printf("FDICreate failed with error code %d: %s\n",
               erf.erfOper,
               FDIErrorToString((FDIERROR)erf.erfOper));
        goto CLEANUP;
    }

    //Extract the files from the cabinet

    if ( FDICopy(hfdi,                        //FDI handle
                 pszCabinetName,              //the cabinet name
                 pszCabinetPath,              //the cabinet path
                 0,                           //not used, set to zero
                 fnNotify,                    //function for notifications
                 NULL,                        //not used, set to NULL
                 pszDestinationDir) == FALSE )//this value is application-specific 
    {
        printf("FDICopy failed with error code %d: %s\n",
               erf.erfOper,
               FDIErrorToString((FDIERROR)erf.erfOper));
        goto CLEANUP;
    }

    bSuccessful = TRUE;

CLEANUP:
    
    //Destory the FDI context

    if ( hfdi != NULL )
    {
        if ( FDIDestroy(hfdi) != TRUE )
        {
            printf("FDIDestroy failed with error code %d: %s\n",
                   erf.erfOper,
                   FDIErrorToString((FDIERROR)erf.erfOper));
        }
    }

    return bSuccessful;
}

LPCSTR FDIErrorToString(FDIERROR err)
{
    switch (err)
    {      
        case FDIERROR_NONE:
        return "No error";

        case FDIERROR_CABINET_NOT_FOUND:
            return "Cabinet not found";

        case FDIERROR_NOT_A_CABINET:
            return "Not a cabinet";

        case FDIERROR_UNKNOWN_CABINET_VERSION:
            return "Unknown cabinet version";

        case FDIERROR_CORRUPT_CABINET:
            return "Corrupt cabinet";

        case FDIERROR_ALLOC_FAIL:
            return "Memory allocation failed";

        case FDIERROR_BAD_COMPR_TYPE:
            return "Unknown compression type";

        case FDIERROR_MDI_FAIL:
            return "Failure decompressing data";

        case FDIERROR_TARGET_FILE:
            return "Failure writing to target file";

    case FDIERROR_RESERVE_MISMATCH:
        return "Cabinets in set have different RESERVE sizes";
            
    case FDIERROR_WRONG_CABINET:
        return "Cabinet returned on fdintNEXT_CABINET is incorrect";

        case FDIERROR_USER_ABORT:
            return "Application aborted";

        default:
        return "Unknown error";
    }
}
}
```



## <a name="related-topics"></a><span data-ttu-id="d42b0-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d42b0-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d42b0-109">**FDICreate**</span><span class="sxs-lookup"><span data-stu-id="d42b0-109">**FDICreate**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicreate)
</dt> <dt>

[<span data-ttu-id="d42b0-110">**FDICopy**</span><span class="sxs-lookup"><span data-stu-id="d42b0-110">**FDICopy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicopy)
</dt> <dt>

[<span data-ttu-id="d42b0-111">**FDIDestroy**</span><span class="sxs-lookup"><span data-stu-id="d42b0-111">**FDIDestroy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)
</dt> <dt>

[<span data-ttu-id="d42b0-112">Macro API cabinet</span><span class="sxs-lookup"><span data-stu-id="d42b0-112">Cabinet API Macros</span></span>](cabinet-api-macros.md)
</dt> </dl>

 

 



