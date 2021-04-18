---
title: Uso di strutture in WCS 1,0
description: La maggior parte delle strutture usate da WCS 1,0 è molto semplice e richiede una spiegazione minima. Sono documentati nella sezione di riferimento WCS 1,0 intitolata Structures.
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Windows Color System (WCS), strutture
- WCS (sistema di colori Windows), strutture
- Gestione colori immagine, strutture
- gestione dei colori, strutture
- colori, strutture
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320943"
---
# <a name="using-structures-in-wcs-10"></a><span data-ttu-id="20ea2-109">Uso di strutture in WCS 1,0</span><span class="sxs-lookup"><span data-stu-id="20ea2-109">Using Structures in WCS 1.0</span></span>

<span data-ttu-id="20ea2-110">La maggior parte delle strutture usate da WCS 1,0 è molto semplice e richiede una spiegazione minima.</span><span class="sxs-lookup"><span data-stu-id="20ea2-110">Most of the structures used by WCS 1.0 are very straightforward and require little explanation.</span></span> <span data-ttu-id="20ea2-111">Sono documentati nella sezione di riferimento WCS 1,0 intitolata [Structures](structures.md).</span><span class="sxs-lookup"><span data-stu-id="20ea2-111">They are documented in the WCS 1.0 Reference section entitled [Structures](structures.md).</span></span>

<span data-ttu-id="20ea2-112">Le eccezioni sono la struttura [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) utilizzata dalla funzione [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) e le strutture di Windows seguenti definite in wingdi. h:</span><span class="sxs-lookup"><span data-stu-id="20ea2-112">Exceptions are the [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) structure used by the [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) function, and the following Windows structures defined in Wingdi.h:</span></span>

-   [<span data-ttu-id="20ea2-113">BITMAPV5HEADER</span><span class="sxs-lookup"><span data-stu-id="20ea2-113">BITMAPV5HEADER</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="20ea2-114">**LOGCOLORSPACE**</span><span class="sxs-lookup"><span data-stu-id="20ea2-114">**LOGCOLORSPACE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [<span data-ttu-id="20ea2-115">**CIE XYZ**</span><span class="sxs-lookup"><span data-stu-id="20ea2-115">**CIEXYZ**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [<span data-ttu-id="20ea2-116">**CIEXYZTRIPLE**</span><span class="sxs-lookup"><span data-stu-id="20ea2-116">**CIEXYZTRIPLE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

<span data-ttu-id="20ea2-117">Gli argomenti seguenti sono trattati a una lunghezza maggiore:</span><span class="sxs-lookup"><span data-stu-id="20ea2-117">The following topics are discussed at greater length:</span></span>

-   [<span data-ttu-id="20ea2-118">Strutture di intestazione bitmap di Windows</span><span class="sxs-lookup"><span data-stu-id="20ea2-118">Windows Bitmap Header Structures</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="20ea2-119">Differenze tra le intestazioni V4 e V5</span><span class="sxs-lookup"><span data-stu-id="20ea2-119">Differences Between V4 and V5 Headers</span></span>](#differences-between-v4-and-v5-headers)
-   [<span data-ttu-id="20ea2-120">Bitmap.exe: utilità Command-Line per la conversione delle intestazioni bitmap</span><span class="sxs-lookup"><span data-stu-id="20ea2-120">Bitmap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a><span data-ttu-id="20ea2-121">Strutture di intestazione bitmap di Windows</span><span class="sxs-lookup"><span data-stu-id="20ea2-121">Windows Bitmap Header Structures</span></span>

<span data-ttu-id="20ea2-122">WCS 1,0 consente di collegare o incorporare i profili dei colori ICC in bitmap indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20ea2-122">WCS 1.0 allows ICC color profiles to be linked or embedded in device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="20ea2-123">Ciò consente di caratterizzare i colori DIB in modo più accurato rispetto a quanto fosse possibile utilizzando WCS in Windows 95.</span><span class="sxs-lookup"><span data-stu-id="20ea2-123">This allows DIB colors to be characterized more accurately than was possible using WCS in Windows 95.</span></span> <span data-ttu-id="20ea2-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , la nuova struttura dell'intestazione bitmap, è definita in wingdi. h nella versione di Windows 98.</span><span class="sxs-lookup"><span data-stu-id="20ea2-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , the new bitmap header structure, is defined in Wingdi.h in the release of Windows 98.</span></span> <span data-ttu-id="20ea2-125">Ai fini dello sviluppo, viene anche incluso nel file ICM. h con i riferimenti di questo programmatore.</span><span class="sxs-lookup"><span data-stu-id="20ea2-125">For development purposes, it is also included in the file Icm.h with this Programmer's Reference.</span></span> <span data-ttu-id="20ea2-126">La struttura **BITMAPV5HEADER** è la seguente:</span><span class="sxs-lookup"><span data-stu-id="20ea2-126">The **BITMAPV5HEADER** structure is as follows:</span></span>


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



<span data-ttu-id="20ea2-127">Il membro **bV5CSType** può avere il profilo dei valori \_ embedded o profile \_ collegato per specificare se un profilo è incorporato o collegato alla DIB.</span><span class="sxs-lookup"><span data-stu-id="20ea2-127">The member **bV5CSType** can have the values PROFILE\_EMBEDDED or PROFILE\_LINKED to specify whether a profile is embedded or linked with the DIB.</span></span> <span data-ttu-id="20ea2-128">Il membro **bV5ProfileData** è l'offset in byte dall'inizio della struttura **BITMAPV5HEADER** all'inizio dei dati del profilo.</span><span class="sxs-lookup"><span data-stu-id="20ea2-128">The member **bV5ProfileData** is the offset in bytes from the beginning of the **BITMAPV5HEADER** structure to the start of the profile data.</span></span> <span data-ttu-id="20ea2-129">Se il profilo è incorporato, i dati del profilo sono i profili effettivi e, se sono collegati, i dati del profilo sono il nome file con terminazione null del profilo.</span><span class="sxs-lookup"><span data-stu-id="20ea2-129">If the profile is embedded, profile data is the actual profile, and if it is linked, the profile data is the null-terminated file name of the profile.</span></span> <span data-ttu-id="20ea2-130">Non può essere una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="20ea2-130">This cannot be a Unicode string.</span></span> <span data-ttu-id="20ea2-131">Deve essere composto esclusivamente da caratteri del set di caratteri di Windows (tabella codici 1252).</span><span class="sxs-lookup"><span data-stu-id="20ea2-131">It must be composed exclusively of characters from the Windows character set (code page 1252).</span></span>

<span data-ttu-id="20ea2-132">Quando una DIB viene caricata in memoria, i dati del profilo (se presente) devono seguire la tabella dei colori e **bV5ProfileData** deve fornire l'offset dei dati di profilo dall'inizio della struttura **BITMAPV5HEADER** .</span><span class="sxs-lookup"><span data-stu-id="20ea2-132">When a DIB is loaded into memory, the profile data (if present) should follow the color table, and **bV5ProfileData** should give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span> <span data-ttu-id="20ea2-133">Il valore di questo membro sarà diverso ora, perché i bit bitmap non seguono la tabella dei colori in memoria.</span><span class="sxs-lookup"><span data-stu-id="20ea2-133">The value of this member will be different now, as the bitmap bits do not follow the color table in memory.</span></span> <span data-ttu-id="20ea2-134">Le applicazioni devono modificare il membro **bV5ProfileData** dopo il caricamento della DIB in memoria.</span><span class="sxs-lookup"><span data-stu-id="20ea2-134">Applications should modify the **bV5ProfileData** member after loading the DIB into memory.</span></span>

<span data-ttu-id="20ea2-135">Per quanto riguarda la precedenza compressa, i dati del profilo devono seguire i bit bitmap simili al formato del file.</span><span class="sxs-lookup"><span data-stu-id="20ea2-135">For packed DIBs, the profile data should follow the bitmap bits similar to the file format.</span></span> <span data-ttu-id="20ea2-136">Il membro **bV5ProfileData** deve comunque assegnare l'offset dei dati di profilo dall'inizio della struttura **BITMAPV5HEADER** .</span><span class="sxs-lookup"><span data-stu-id="20ea2-136">The **bV5ProfileData** member should still give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span>

<span data-ttu-id="20ea2-137">Le applicazioni devono accedere ai dati del profilo solo quando **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** è incorporato nel profilo \_ o collegato al profilo \_ .</span><span class="sxs-lookup"><span data-stu-id="20ea2-137">Applications should access the profile data only when **bV5Size** == **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** is PROFILE\_EMBEDDED or PROFILE\_LINKED.</span></span>

<span data-ttu-id="20ea2-138">Se un profilo è collegato, il percorso del profilo può essere qualsiasi nome completo (incluso un percorso di rete) che può essere aperto tramite la funzione **CreateFile** di Win32.</span><span class="sxs-lookup"><span data-stu-id="20ea2-138">If a profile is linked, the path of the profile can be any fully qualified name (including a network path) that can be opened using the Win32 **CreateFile** function.</span></span>

## <a name="differences-between-v4-and-v5-headers"></a><span data-ttu-id="20ea2-139">Differenze tra le intestazioni V4 e V5</span><span class="sxs-lookup"><span data-stu-id="20ea2-139">Differences Between V4 and V5 Headers</span></span>

<span data-ttu-id="20ea2-140">Quando si lavora con la nuova struttura bitmap, è utile riconoscere le differenze nella modalità di configurazione delle strutture **BITMAPV4HEADER** e **BITMAPV5HEADER** :</span><span class="sxs-lookup"><span data-stu-id="20ea2-140">In working with the new bitmap structure, it is useful to recognize differences in how **BITMAPV4HEADER** and **BITMAPV5HEADER** structures are set up:</span></span>



| <span data-ttu-id="20ea2-141">Intestazione V4</span><span class="sxs-lookup"><span data-stu-id="20ea2-141">V4 Header</span></span>     | <span data-ttu-id="20ea2-142">Significato</span><span class="sxs-lookup"><span data-stu-id="20ea2-142">Meaning</span></span>                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ea2-143">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="20ea2-143">**bV4CSType**</span></span> | <span data-ttu-id="20ea2-144">\_RGB calibrato di LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="20ea2-144">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="20ea2-145">Questo valore implica che i punti finali e gamma siano specificati nei campi appropriati.</span><span class="sxs-lookup"><span data-stu-id="20ea2-145">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="20ea2-146">I valori fasulli provocano problemi.</span><span class="sxs-lookup"><span data-stu-id="20ea2-146">Bogus values cause trouble.</span></span> |
| <span data-ttu-id="20ea2-147">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="20ea2-147">**bV4CSType**</span></span> | <span data-ttu-id="20ea2-148">LCS \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="20ea2-148">LCS\_sRGB.</span></span> <span data-ttu-id="20ea2-149">Questo valore implica che la bitmap si trovi nello spazio dei colori di sRGB (gamma ed endpoint ignorati).</span><span class="sxs-lookup"><span data-stu-id="20ea2-149">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                 |
| <span data-ttu-id="20ea2-150">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="20ea2-150">**bV4CSType**</span></span> | <span data-ttu-id="20ea2-151">\_ \_ spazio colore Windows LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="20ea2-151">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="20ea2-152">Questo valore implica che la bitmap si trovi nello spazio dei colori predefinito di Windows.</span><span class="sxs-lookup"><span data-stu-id="20ea2-152">This value implies that the bitmap is in Windows default color space.</span></span>                                    |



 



| <span data-ttu-id="20ea2-153">Intestazione V5</span><span class="sxs-lookup"><span data-stu-id="20ea2-153">V5 Header</span></span>     | <span data-ttu-id="20ea2-154">Significato</span><span class="sxs-lookup"><span data-stu-id="20ea2-154">Meaning</span></span>                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ea2-155">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="20ea2-155">**bV5CSType**</span></span> | <span data-ttu-id="20ea2-156">\_RGB calibrato di LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="20ea2-156">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="20ea2-157">Questo valore implica che i punti finali e gamma siano specificati nei campi appropriati.</span><span class="sxs-lookup"><span data-stu-id="20ea2-157">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="20ea2-158">I valori fasulli provocano problemi.</span><span class="sxs-lookup"><span data-stu-id="20ea2-158">Bogus values cause trouble.</span></span>                         |
| <span data-ttu-id="20ea2-159">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="20ea2-159">**bV5CSType**</span></span> | <span data-ttu-id="20ea2-160">LCS \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="20ea2-160">LCS\_sRGB.</span></span> <span data-ttu-id="20ea2-161">Questo valore implica che la bitmap si trovi nello spazio dei colori di sRGB (gamma ed endpoint ignorati).</span><span class="sxs-lookup"><span data-stu-id="20ea2-161">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                                         |
| <span data-ttu-id="20ea2-162">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="20ea2-162">**bV5CSType**</span></span> | <span data-ttu-id="20ea2-163">PROFILO \_ incorporato.</span><span class="sxs-lookup"><span data-stu-id="20ea2-163">PROFILE\_EMBEDDED.</span></span> <span data-ttu-id="20ea2-164">Questo valore implica che **bV5ProfileData** punta a un buffer di memoria che contiene il profilo da usare (i gamma e gli endpoint vengono ignorati).</span><span class="sxs-lookup"><span data-stu-id="20ea2-164">This value implies that **bV5ProfileData** points to a memory buffer that contains the profile to use (gammas and endpoints are ignored).</span></span> |
| <span data-ttu-id="20ea2-165">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="20ea2-165">**bV5CSType**</span></span> | <span data-ttu-id="20ea2-166">PROFILO \_ collegato.</span><span class="sxs-lookup"><span data-stu-id="20ea2-166">PROFILE\_LINKED.</span></span> <span data-ttu-id="20ea2-167">Questo valore implica che **bV5ProfileData** punta al nome file del profilo da usare (i gamma e gli endpoint vengono ignorati).</span><span class="sxs-lookup"><span data-stu-id="20ea2-167">This value implies that **bV5ProfileData** points to the file name of the profile to use (gammas and endpoints are ignored).</span></span>                |
| <span data-ttu-id="20ea2-168">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="20ea2-168">**bV5CSType**</span></span> | <span data-ttu-id="20ea2-169">\_ \_ spazio colore Windows LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="20ea2-169">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="20ea2-170">Questo valore implica che la bitmap si trovi nello spazio dei colori predefinito di Windows.</span><span class="sxs-lookup"><span data-stu-id="20ea2-170">This value implies that the bitmap is in Windows default color space.</span></span>                                                            |



 

<span data-ttu-id="20ea2-171">Per convertire le bitmap meno recenti da e verso la nuova struttura **BITMAPV5HEADER** , un file dell'utilità di conversione da riga di comando denominato Bitmap.exe è incluso nella Guida di riferimento per programmatori WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="20ea2-171">In order to convert older bitmaps to and from the new **BITMAPV5HEADER** structure, a command-line conversion utility file named Bitmap.exe is included in the WCS 1.0 Programmer's Reference.</span></span>

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a><span data-ttu-id="20ea2-172">BitMap.exe: utilità Command-Line per la conversione delle intestazioni bitmap</span><span class="sxs-lookup"><span data-stu-id="20ea2-172">BitMap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>

<span data-ttu-id="20ea2-173">Bitmap.exe è un'utilità da riga di comando che si trova nella \\ cartella bin nella cartella di installazione specificata.</span><span class="sxs-lookup"><span data-stu-id="20ea2-173">Bitmap.exe is a command-line utility located in the \\Bin folder under the installation folder that you specified.</span></span> <span data-ttu-id="20ea2-174">Modifica le intestazioni delle bitmap di Windows, consentendo di convertire le bitmap esistenti dalle strutture di intestazione **BITMAPINFOHEADER** e **BITMAPV4HEADER** alla struttura **BITMAPV5HEADER** più recente e viceversa.</span><span class="sxs-lookup"><span data-stu-id="20ea2-174">It modifies the headers of Windows bitmaps, allowing you to convert existing bitmaps from **BITMAPINFOHEADER** and **BITMAPV4HEADER** header structures to the newer **BITMAPV5HEADER** structure and back again.</span></span> <span data-ttu-id="20ea2-175">La sintassi della riga di comando è la seguente:</span><span class="sxs-lookup"><span data-stu-id="20ea2-175">The command-line syntax is as follows:</span></span>


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



<span data-ttu-id="20ea2-176">Le opzioni della riga di comando hanno gli effetti seguenti.</span><span class="sxs-lookup"><span data-stu-id="20ea2-176">The command-line switches have the following effects.</span></span>



| <span data-ttu-id="20ea2-177">Opzione</span><span class="sxs-lookup"><span data-stu-id="20ea2-177">Switch</span></span> | <span data-ttu-id="20ea2-178">Significato</span><span class="sxs-lookup"><span data-stu-id="20ea2-178">Meaning</span></span>                                                                  |
|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="20ea2-179">/d</span><span class="sxs-lookup"><span data-stu-id="20ea2-179">/d</span></span>     | <span data-ttu-id="20ea2-180">I valori predefiniti vengono immessi automaticamente nelle intestazioni convertite.</span><span class="sxs-lookup"><span data-stu-id="20ea2-180">Default values are automatically entered in the converted headers.</span></span>       |
| <span data-ttu-id="20ea2-181">/1</span><span class="sxs-lookup"><span data-stu-id="20ea2-181">/1</span></span>     | <span data-ttu-id="20ea2-182">Converte le bitmap specificate in **BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="20ea2-182">Convert the specified bitmaps to **BITMAPINFOHEADER**</span></span>                    |
| <span data-ttu-id="20ea2-183">/4</span><span class="sxs-lookup"><span data-stu-id="20ea2-183">/4</span></span>     | <span data-ttu-id="20ea2-184">Converte le bitmap specificate in **BITMAPV4HEADER**</span><span class="sxs-lookup"><span data-stu-id="20ea2-184">Convert the specified bitmaps to **BITMAPV4HEADER**</span></span>                      |
| <span data-ttu-id="20ea2-185">/5</span><span class="sxs-lookup"><span data-stu-id="20ea2-185">/5</span></span>     | <span data-ttu-id="20ea2-186">Converte le bitmap specificate in **BITMAPV5HEADER**</span><span class="sxs-lookup"><span data-stu-id="20ea2-186">Convert the specified bitmaps to **BITMAPV5HEADER**</span></span>                      |
| <span data-ttu-id="20ea2-187">/f</span><span class="sxs-lookup"><span data-stu-id="20ea2-187">/f</span></span>     | <span data-ttu-id="20ea2-188">Forza la conversione, anche se la bitmap ha già l'intestazione corretta</span><span class="sxs-lookup"><span data-stu-id="20ea2-188">Forces conversion, even if the bitmap already has the right header</span></span>       |
| <span data-ttu-id="20ea2-189">/s</span><span class="sxs-lookup"><span data-stu-id="20ea2-189">/s</span></span>     | <span data-ttu-id="20ea2-190">Converte le bitmap nella cartella specificata e in tutte le sottodirectory</span><span class="sxs-lookup"><span data-stu-id="20ea2-190">Converts bitmaps in the specified folder and all subdirectories under it</span></span> |



 

 

 