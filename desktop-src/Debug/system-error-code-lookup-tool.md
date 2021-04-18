---
description: Viene descritto come utilizzare lo strumento ricerca errori Microsoft per trovare le spiegazioni del testo dei codici errore esadecimali in Windows.
title: Strumento ricerca errori Microsoft
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304659"
---
# <a name="the-microsoft-error-lookup-tool"></a><span data-ttu-id="b9c53-103">Strumento ricerca errori Microsoft</span><span class="sxs-lookup"><span data-stu-id="b9c53-103">The Microsoft Error Lookup Tool</span></span>

<span data-ttu-id="b9c53-104">Lo strumento ricerca errori Microsoft Visualizza il testo del messaggio associato a un codice di stato esadecimale (o altro codice).</span><span class="sxs-lookup"><span data-stu-id="b9c53-104">The Microsoft Error Lookup Tool displays the message text that is associated with a hexadecimal status code (or other code).</span></span> <span data-ttu-id="b9c53-105">Questo testo è definito in diversi file di intestazione del codice sorgente Microsoft, ad esempio Winerror. h, Setupapi. h e così via.</span><span class="sxs-lookup"><span data-stu-id="b9c53-105">This text is defined in various Microsoft source-code header files, such as Winerror.h, Setupapi.h, and so on.</span></span>

<span data-ttu-id="b9c53-106">Lo strumento è firmato digitalmente da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b9c53-106">The tool is digitally signed by Microsoft.</span></span> <span data-ttu-id="b9c53-107">Di seguito sono riportate le informazioni di SHA256 per il download del file:</span><span class="sxs-lookup"><span data-stu-id="b9c53-107">The following is the SHA256 information for the file download:</span></span>  

|<span data-ttu-id="b9c53-108">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="b9c53-108">Algorithm</span></span> |<span data-ttu-id="b9c53-109">Hash</span><span class="sxs-lookup"><span data-stu-id="b9c53-109">Hash</span></span> |
| --- | --- |
|<span data-ttu-id="b9c53-110">SHA256</span><span class="sxs-lookup"><span data-stu-id="b9c53-110">SHA256</span></span> |<span data-ttu-id="b9c53-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span><span class="sxs-lookup"><span data-stu-id="b9c53-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span></span> |

> [!NOTE]
> <span data-ttu-id="b9c53-112">Gli ambienti aziendali possono limitare i file che possono essere eseguiti e da dove.</span><span class="sxs-lookup"><span data-stu-id="b9c53-112">Business environments may restrict which files can run and from where.</span></span> <span data-ttu-id="b9c53-113">Prima di scaricare ed eseguire lo strumento, verificare i seguenti dettagli:</span><span class="sxs-lookup"><span data-stu-id="b9c53-113">Before you download and run this tool, check the following details:</span></span>
> - <span data-ttu-id="b9c53-114">È necessario disporre dell'autorizzazione o di un'eccezione di sicurezza per scaricare o eseguire lo strumento?</span><span class="sxs-lookup"><span data-stu-id="b9c53-114">Do you have to have permission or a security exception in order to download or run the tool?</span></span>
> - <span data-ttu-id="b9c53-115">È possibile archiviare ed eseguire lo strumento nel computer (ad esempio, nella cartella documenti)?</span><span class="sxs-lookup"><span data-stu-id="b9c53-115">Can you store and run this tool on your computer (for example, in your Documents folder)?</span></span> <span data-ttu-id="b9c53-116">In alternativa, è necessario archiviare ed eseguire lo strumento in un computer specializzato, ad esempio un file server centrale?</span><span class="sxs-lookup"><span data-stu-id="b9c53-116">Or do you have to store and run the tool on a specialized computer, such as a central file server?</span></span>

## <a name="usage"></a><span data-ttu-id="b9c53-117">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b9c53-117">Usage</span></span>

1. <span data-ttu-id="b9c53-118">Scaricare lo strumento selezionando [questo collegamento](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span><span class="sxs-lookup"><span data-stu-id="b9c53-118">Download the tool by selecting [this link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span></span>
1. <span data-ttu-id="b9c53-119">Se non è stato specificato un percorso nel passaggio 1, passare alla cartella di download e copiare o spostare il file scaricato (Err_6.4.5.exe) nella cartella in cui verrà archiviato lo strumento.</span><span class="sxs-lookup"><span data-stu-id="b9c53-119">If you didn't specify a location in step 1, go to your download folder, and copy or move the downloaded file (Err_6.4.5.exe) to folder in which you will store the tool.</span></span> <span data-ttu-id="b9c53-120">Non è necessario espandere o installare il file.</span><span class="sxs-lookup"><span data-stu-id="b9c53-120">You do not have to expand or install the file.</span></span>
   > [!NOTE]
   > <span data-ttu-id="b9c53-121">Se si copia o si sposta il file in una cartella elencata nella variabile di ambiente **path** del sistema operativo, il file funzionerà in qualsiasi prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="b9c53-121">If you copy or move the file to a folder that is listed in your operating system's **Path** environment variable, it will work at any command prompt.</span></span>

1. <span data-ttu-id="b9c53-122">Aprire una finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="b9c53-122">Open a Command Prompt window.</span></span> <span data-ttu-id="b9c53-123">Se necessario, impostare la directory sul percorso dello strumento di ricerca degli errori.</span><span class="sxs-lookup"><span data-stu-id="b9c53-123">If necessary, change the directory to the location of the Error Lookup Tool.</span></span>
1. <span data-ttu-id="b9c53-124">Eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="b9c53-124">Run the following command:</span></span>
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > <span data-ttu-id="b9c53-125">In questo comando \<*error code*> rappresenta il codice esadecimale che si desidera cercare.</span><span class="sxs-lookup"><span data-stu-id="b9c53-125">In this command, \<*error code*> represents the hexadecimal code that you want to look up.</span></span>

## <a name="examples"></a><span data-ttu-id="b9c53-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="b9c53-126">Examples</span></span>

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a><span data-ttu-id="b9c53-127">Ulteriori informazioni</span><span class="sxs-lookup"><span data-stu-id="b9c53-127">More information</span></span>

<span data-ttu-id="b9c53-128">Tenere presente che si tratta di uno strumento "temporizzato".</span><span class="sxs-lookup"><span data-stu-id="b9c53-128">Keep in mind that this is a "point-in-time" tool.</span></span> <span data-ttu-id="b9c53-129">Lo strumento ricerca errori Microsoft decodifica la maggior parte dei codici di errore Microsoft alla data in cui lo strumento è stato compilato.</span><span class="sxs-lookup"><span data-stu-id="b9c53-129">The Microsoft Error Lookup Tool decodes most Microsoft error codes as of the date on which the tool was compiled.</span></span> <span data-ttu-id="b9c53-130">Poiché le nuove versioni di Windows aggiungono nuovi codici di errore e di evento, potrebbe essere necessario scaricare una nuova versione dello strumento di ricerca degli errori.</span><span class="sxs-lookup"><span data-stu-id="b9c53-130">As new releases of Windows add new event and error codes, you may have to download a new version of the Error Lookup Tool.</span></span> <span data-ttu-id="b9c53-131">Controllare l'area download Microsoft per una nuova versione o vedere i [codici di errore](system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b9c53-131">Check the Microsoft Download Center for a new version, or see [Error Codes](system-error-codes.md).</span></span>
