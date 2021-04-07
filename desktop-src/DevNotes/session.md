---
description: La struttura della sessione contiene informazioni sulla sessione corrente.
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: Struttura della sessione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e1f356020df681e00f43c7a47ac16048764c0ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747671"
---
# <a name="session-structure"></a><span data-ttu-id="03fdc-103">Struttura della sessione</span><span class="sxs-lookup"><span data-stu-id="03fdc-103">SESSION structure</span></span>

<span data-ttu-id="03fdc-104">\[Questa struttura contiene le informazioni necessarie solo quando si usano le funzioni **DeleteExtractedFiles** ed **Extract** , che non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="03fdc-104">\[This structure contains information required only when using the **DeleteExtractedFiles** and **Extract** functions, which are not supported.</span></span> <span data-ttu-id="03fdc-105">Questa documentazione viene fornita solo a scopo informativo.\]</span><span class="sxs-lookup"><span data-stu-id="03fdc-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="03fdc-106">La struttura della **sessione** contiene informazioni sulla sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="03fdc-106">The **SESSION** structure contains information about the current session.</span></span>

## <a name="syntax"></a><span data-ttu-id="03fdc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03fdc-107">Syntax</span></span>


```C++
typedef struct {
  ACTION    act;
  HFILELIST hflist;
  BOOL      fAllCabinets;
  BOOL      fOverwrite;
  BOOL      fNoLineFeed;
  BOOL      fSelfExtract;
  long      cbSelfExtractSize;
  long      cbSelfExtractSize;
  int       ahfSelf[cMAX_CAB_FILE_OPEN];
  int       cErrors;
  HFDI      hfdi;
  ERF       erf;
  long      cFiles;
  long      cbTotalBytes;
  PERROR    perr;
  SPILLERR  se;
  long      cbSpill;
  char      achSelf[cbFILE_NAME_MAX];
  char      achMsg[cbMAX_LINE*2];
  char      achLine;
  char      achLocation;
  char      achFile;
  char      achDest;
  char      achCabPath;
  BOOL      fContinuationCabinet;
  BOOL      fShowReserveInfo;
  BOOL      fNextCabCalled;
  CABINET   acab[2];
  char      achZap[cbFILE_NAME_MAX];
  char      achCabinetFile[cbFILE_NAME_MAX];
  int       cArgv;
  char      **pArgv;
  int       fDestructive;
  USHORT    iCurrentFolder;
} SESSION, *PSESSION;
```



## <a name="members"></a><span data-ttu-id="03fdc-108">Members</span><span class="sxs-lookup"><span data-stu-id="03fdc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="03fdc-109">**atto**</span><span class="sxs-lookup"><span data-stu-id="03fdc-109">**act**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-110">l'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="03fdc-110">The action to perform.</span></span> <span data-ttu-id="03fdc-111">Questo membro può essere uno dei valori del tipo enumerato seguente.</span><span class="sxs-lookup"><span data-stu-id="03fdc-111">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    actBAD,         // Invalid action
    actHELP,        // Show help
    actDEFAULT,     // Perform default action based on command line arguments
    actDIRECTORY,   // Force display of cabinet directory
    actEXTRACT,     // Force file extraction
    actCOPY,        // Do single file-to-file copy
} ACTION;  
```

</dd> <dt>

<span data-ttu-id="03fdc-112">**hflist**</span><span class="sxs-lookup"><span data-stu-id="03fdc-112">**hflist**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-113">Handle per un elenco di file specificati nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="03fdc-113">The handle to a list of files specified on the command line.</span></span> <span data-ttu-id="03fdc-114">Questo tipo di dati viene dichiarato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="03fdc-114">This datatype is declared as follows:</span></span>

`typedef void *HFILELIST;`

</dd> <dt>

<span data-ttu-id="03fdc-115">**fAllCabinets**</span><span class="sxs-lookup"><span data-stu-id="03fdc-115">**fAllCabinets**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-116">Flag che indica se deve essere elaborato più di un file CAB.</span><span class="sxs-lookup"><span data-stu-id="03fdc-116">A flag that indicates whether more than one cabinet file should be processed.</span></span> <span data-ttu-id="03fdc-117">Se questo valore è **true**, vengono elaborati i file CAB di continuazione.</span><span class="sxs-lookup"><span data-stu-id="03fdc-117">If this value is **TRUE**, continuation cabinets are processed.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-118">**fOverwrite**</span><span class="sxs-lookup"><span data-stu-id="03fdc-118">**fOverwrite**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-119">Flag che indica se i file esistenti devono essere sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="03fdc-119">A flag that indicates whether existing files should be overwritten.</span></span> <span data-ttu-id="03fdc-120">Se questo valore è **true**, i file esistenti vengono sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="03fdc-120">If this value is **TRUE**, existing files are overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-121">**fNoLineFeed**</span><span class="sxs-lookup"><span data-stu-id="03fdc-121">**fNoLineFeed**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-122">Flag che indica se l'ultima `printf` chiamata presenta i caratteri di nuova riga ( `\n` ).</span><span class="sxs-lookup"><span data-stu-id="03fdc-122">A flag that indicates whether the last `printf` call has the newline (`\n`) characters.</span></span> <span data-ttu-id="03fdc-123">Se questo valore è **true**, l'ultima `printf` chiamata non include i caratteri di nuova riga.</span><span class="sxs-lookup"><span data-stu-id="03fdc-123">If this value is **TRUE**, the last `printf` call did not include the newline characters.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-124">**fSelfExtract**</span><span class="sxs-lookup"><span data-stu-id="03fdc-124">**fSelfExtract**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-125">Flag che indica se un file CAB è autoestraente.</span><span class="sxs-lookup"><span data-stu-id="03fdc-125">A flag that indicates whether a cabinet is self extracting.</span></span> <span data-ttu-id="03fdc-126">Se questo valore è **true**, l'archivio è autoestraente.</span><span class="sxs-lookup"><span data-stu-id="03fdc-126">If this value is **TRUE**, the cabinet is self extracting.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-127">**cbSelfExtractSize**</span><span class="sxs-lookup"><span data-stu-id="03fdc-127">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-128">Lunghezza della parte eseguibile (con estensione exe) di un cabinet autoestraente.</span><span class="sxs-lookup"><span data-stu-id="03fdc-128">The length of the executable (.exe) portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-129">**cbSelfExtractSize**</span><span class="sxs-lookup"><span data-stu-id="03fdc-129">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-130">Lunghezza della parte CAB di un cabinet autoestraente.</span><span class="sxs-lookup"><span data-stu-id="03fdc-130">The length of the CAB portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-131">**ahfSelf**</span><span class="sxs-lookup"><span data-stu-id="03fdc-131">**ahfSelf**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-132">Il file viene gestito nel file CAB.</span><span class="sxs-lookup"><span data-stu-id="03fdc-132">The file handles to the cabinet.</span></span>

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

<span data-ttu-id="03fdc-133">**cErrors**</span><span class="sxs-lookup"><span data-stu-id="03fdc-133">**cErrors**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-134">Numero di errori rilevati durante la sessione di estrazione.</span><span class="sxs-lookup"><span data-stu-id="03fdc-134">The count of errors encountered during the extraction session.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-135">**hfdi**</span><span class="sxs-lookup"><span data-stu-id="03fdc-135">**hfdi**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-136">Handle per il contesto IDE.</span><span class="sxs-lookup"><span data-stu-id="03fdc-136">A handle to the FDI context.</span></span> <span data-ttu-id="03fdc-137">Questo tipo di dati viene dichiarato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="03fdc-137">This datatype is declared as follows:</span></span>

`typedef void FAR *HFDI; `

</dd> <dt>

<span data-ttu-id="03fdc-138">**erf**</span><span class="sxs-lookup"><span data-stu-id="03fdc-138">**erf**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-139">Struttura degli errori di IDE.</span><span class="sxs-lookup"><span data-stu-id="03fdc-139">The FDI error structure.</span></span> <span data-ttu-id="03fdc-140">Vedere [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span><span class="sxs-lookup"><span data-stu-id="03fdc-140">See [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-141">**cFiles**</span><span class="sxs-lookup"><span data-stu-id="03fdc-141">**cFiles**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-142">Numero di file elaborati.</span><span class="sxs-lookup"><span data-stu-id="03fdc-142">The count of files processed.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-143">**cbTotalBytes**</span><span class="sxs-lookup"><span data-stu-id="03fdc-143">**cbTotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-144">Numero totale di byte estratti.</span><span class="sxs-lookup"><span data-stu-id="03fdc-144">The total number of bytes extracted.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-145">**perr**</span><span class="sxs-lookup"><span data-stu-id="03fdc-145">**perr**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-146">Il pass-through IDE.</span><span class="sxs-lookup"><span data-stu-id="03fdc-146">The pass through FDI.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-147">**Se**</span><span class="sxs-lookup"><span data-stu-id="03fdc-147">**se**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-148">Errore di file.</span><span class="sxs-lookup"><span data-stu-id="03fdc-148">The spill file error.</span></span> <span data-ttu-id="03fdc-149">Questo membro può essere uno dei valori del tipo enumerato seguente.</span><span class="sxs-lookup"><span data-stu-id="03fdc-149">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

<span data-ttu-id="03fdc-150">**cbSpill**</span><span class="sxs-lookup"><span data-stu-id="03fdc-150">**cbSpill**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-151">Dimensioni del file di fuoriuscita richiesto.</span><span class="sxs-lookup"><span data-stu-id="03fdc-151">The size of the spill file requested.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-152">**achSelf**</span><span class="sxs-lookup"><span data-stu-id="03fdc-152">**achSelf**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-153">Nome del file eseguibile (exe).</span><span class="sxs-lookup"><span data-stu-id="03fdc-153">The name of the executable (.exe) file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="03fdc-154">**achMsg**</span><span class="sxs-lookup"><span data-stu-id="03fdc-154">**achMsg**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-155">Buffer di formattazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="03fdc-155">The message formatting buffer.</span></span>

`#define cbMAX_LINE          256`

</dd> <dt>

<span data-ttu-id="03fdc-156">**achLine**</span><span class="sxs-lookup"><span data-stu-id="03fdc-156">**achLine**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-157">Buffer di formattazione della linea.</span><span class="sxs-lookup"><span data-stu-id="03fdc-157">The line formatting buffer.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-158">**achLocation**</span><span class="sxs-lookup"><span data-stu-id="03fdc-158">**achLocation**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-159">La directory di output.</span><span class="sxs-lookup"><span data-stu-id="03fdc-159">The output directory.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-160">**achFile**</span><span class="sxs-lookup"><span data-stu-id="03fdc-160">**achFile**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-161">Nome file corrente da estrarre.</span><span class="sxs-lookup"><span data-stu-id="03fdc-161">The current file name being extracted.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-162">**achDest**</span><span class="sxs-lookup"><span data-stu-id="03fdc-162">**achDest**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-163">Nome del file di destinazione forzata.</span><span class="sxs-lookup"><span data-stu-id="03fdc-163">The forced destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-164">**achCabPath**</span><span class="sxs-lookup"><span data-stu-id="03fdc-164">**achCabPath**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-165">Percorso da esaminare per un file CAB.</span><span class="sxs-lookup"><span data-stu-id="03fdc-165">The path to look at for a cabinet file.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-166">**fContinuationCabinet**</span><span class="sxs-lookup"><span data-stu-id="03fdc-166">**fContinuationCabinet**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-167">Flag che indica se il file CAB corrente è il primo elaborato.</span><span class="sxs-lookup"><span data-stu-id="03fdc-167">A flag that indicates whether the current cabinet is the first one processed.</span></span> <span data-ttu-id="03fdc-168">Se impostato su **true**, non è il primo file CAB elaborato.</span><span class="sxs-lookup"><span data-stu-id="03fdc-168">If set to **TRUE**, it is not the first cabinet processed.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-169">**fShowReserveInfo**</span><span class="sxs-lookup"><span data-stu-id="03fdc-169">**fShowReserveInfo**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-170">Flag che indica se devono essere fornite informazioni riservate.</span><span class="sxs-lookup"><span data-stu-id="03fdc-170">A flag that indicates whether reserve information should be provided.</span></span> <span data-ttu-id="03fdc-171">Se impostato su **true**, le informazioni vengono rese disponibili.</span><span class="sxs-lookup"><span data-stu-id="03fdc-171">If set to **TRUE**, the information is made available.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-172">**fNextCabCalled**</span><span class="sxs-lookup"><span data-stu-id="03fdc-172">**fNextCabCalled**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-173">Questo membro fornisce un modo per determinare quali voci **Acab** usare se si elaborano tutti i file in un set di file CAB (**fAllCabinet** è impostato su **true**).</span><span class="sxs-lookup"><span data-stu-id="03fdc-173">This member provides a way to determine which of the **acab** entries to use if we are processing all files in a cabinet set (**fAllCabinet** is set to **TRUE**).</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-174">**ACAB**</span><span class="sxs-lookup"><span data-stu-id="03fdc-174">**acab**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-175">Ultime due voci nel set di file CAB.</span><span class="sxs-lookup"><span data-stu-id="03fdc-175">The last two entries in the cabinet set.</span></span> <span data-ttu-id="03fdc-176">Questa struttura viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="03fdc-176">This structure is defined as follows:</span></span>

``` syntax
typedef struct {
    char    achCabPath[cbFILE_NAME_MAX];     // Cabinet file path
    char    achCabFilename[cbFILE_NAME_MAX]; // Cabinet file name.ext
    char    achDiskName[cbFILE_NAME_MAX];    // User readable disk label
    USHORT  setID;
    USHORT  iCabinet;
} CABINET;
typedef CABINET *PCABINET;
```

</dd> <dt>

<span data-ttu-id="03fdc-177">**achZap**</span><span class="sxs-lookup"><span data-stu-id="03fdc-177">**achZap**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-178">Prefisso da rimuovere dal nome del file.</span><span class="sxs-lookup"><span data-stu-id="03fdc-178">The prefix to strip from the file name.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="03fdc-179">**achCabinetFile**</span><span class="sxs-lookup"><span data-stu-id="03fdc-179">**achCabinetFile**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-180">File CAB corrente.</span><span class="sxs-lookup"><span data-stu-id="03fdc-180">The current cabinet file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="03fdc-181">**cArgv**</span><span class="sxs-lookup"><span data-stu-id="03fdc-181">**cArgv**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-182">Argc autoestraente predefinito.</span><span class="sxs-lookup"><span data-stu-id="03fdc-182">The default self-extracting argc.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-183">**pArgv**</span><span class="sxs-lookup"><span data-stu-id="03fdc-183">**pArgv**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-184">Puntatore a un puntatore al valore predefinito argv autoestraente \[ \] .</span><span class="sxs-lookup"><span data-stu-id="03fdc-184">A pointer to a pointer to the default self-extracting argv\[\].</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-185">**fDestructive**</span><span class="sxs-lookup"><span data-stu-id="03fdc-185">**fDestructive**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-186">Flag che riduce al minimo lo spazio su disco necessario quando è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="03fdc-186">A flag that minimizes the disk space needed when set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="03fdc-187">**iCurrentFolder**</span><span class="sxs-lookup"><span data-stu-id="03fdc-187">**iCurrentFolder**</span></span>
</dt> <dd>

<span data-ttu-id="03fdc-188">Se **fDestructive** è impostato su **true**, estrarre solo la cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="03fdc-188">If **fDestructive** is set to **TRUE**, extract only the current folder.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="03fdc-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03fdc-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03fdc-190">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="03fdc-190">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="03fdc-191">**Estrarre**</span><span class="sxs-lookup"><span data-stu-id="03fdc-191">**Extract**</span></span>](extract.md)
</dt> </dl>

 

 
