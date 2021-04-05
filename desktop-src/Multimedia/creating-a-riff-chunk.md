---
title: Creazione di un blocco di RIFF
description: Creazione di un blocco di RIFF
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- I/O file multimediale, creazione di un blocco RIFF
- I/O di file, creazione di un blocco RIFF
- input e output (I/O), creazione di un blocco RIFF
- I/O (input e output), creazione di un blocco RIFF
- creazione di un blocco RIFF
- mmioCreateChunk (funzione)
- formato file di interscambio risorse (RIFF)
- RIFF (formato file di interscambio risorse)
- I/O RIFF
- Blocco RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872422"
---
# <a name="creating-a-riff-chunk"></a><span data-ttu-id="523ad-113">Creazione di un blocco di RIFF</span><span class="sxs-lookup"><span data-stu-id="523ad-113">Creating a RIFF Chunk</span></span>

<span data-ttu-id="523ad-114">Nell'esempio seguente viene usata la funzione [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) per creare un blocco con un identificatore di blocco "riff" e un tipo di form "RDIB".</span><span class="sxs-lookup"><span data-stu-id="523ad-114">The following example uses the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function to create a chunk with a chunk identifier of "RIFF" and a form type of "RDIB".</span></span>


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



<span data-ttu-id="523ad-115">Se si sta creando un blocco "RIFF" o "LIST", è necessario specificare il tipo di modulo o il tipo di elenco nel membro **fccType** della struttura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) .</span><span class="sxs-lookup"><span data-stu-id="523ad-115">If you are creating a "RIFF" or "LIST" chunk, you must specify the form type or list type in the **fccType** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure.</span></span> <span data-ttu-id="523ad-116">Nell'esempio precedente, "RDIB" è il tipo di form.</span><span class="sxs-lookup"><span data-stu-id="523ad-116">In the previous example, "RDIB" is the form type.</span></span>

<span data-ttu-id="523ad-117">Se si conoscono le dimensioni del campo dati in un nuovo blocco, è possibile impostare il membro **cksize** della struttura **MMCKINFO** quando si crea il blocco.</span><span class="sxs-lookup"><span data-stu-id="523ad-117">If you know the size of the data field in a new chunk, you can set the **cksize** member of the **MMCKINFO** structure when you create the chunk.</span></span> <span data-ttu-id="523ad-118">Questo valore verrà scritto nel campo dimensione dati nel nuovo blocco.</span><span class="sxs-lookup"><span data-stu-id="523ad-118">This value will be written to the data size field in the new chunk.</span></span> <span data-ttu-id="523ad-119">Se questo valore non è corretto quando si chiama [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) per contrassegnare la fine del blocco, verrà riscritto automaticamente per riflettere la dimensione corretta del campo dati.</span><span class="sxs-lookup"><span data-stu-id="523ad-119">If this value is not correct when you call [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) to mark the end of the chunk, it will be automatically rewritten to reflect the correct size of the data field.</span></span>

<span data-ttu-id="523ad-120">Dopo aver creato un blocco usando la funzione [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) , la posizione del file è impostata sul campo dati del blocco (8 byte dall'inizio del blocco).</span><span class="sxs-lookup"><span data-stu-id="523ad-120">After you create a chunk by using the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function, the file position is set to the data field of the chunk (8 bytes from the beginning of the chunk).</span></span> <span data-ttu-id="523ad-121">Se il blocco è un blocco "RIFF" o "LIST", la posizione del file è impostata sulla posizione successiva al tipo di modulo o al tipo di elenco (12 byte dall'inizio del blocco).</span><span class="sxs-lookup"><span data-stu-id="523ad-121">If the chunk is a "RIFF" or "LIST" chunk, the file position is set to the location following the form type or list type (12 bytes from the beginning of the chunk).</span></span>

 

 