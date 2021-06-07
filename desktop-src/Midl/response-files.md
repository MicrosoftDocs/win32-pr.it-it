---
title: File di risposta
description: In alternativa all'inserimento di tutte le opzioni nella riga di comando, il compilatore MIDL accetta i file di risposta che contengono opzioni e argomenti.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL del compilatore MIDL , file di risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9b4d079e92dff3c25f8a38c6c73073a548ea91
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387071"
---
# <a name="response-files"></a><span data-ttu-id="fc384-104">File di risposta</span><span class="sxs-lookup"><span data-stu-id="fc384-104">Response Files</span></span>

<span data-ttu-id="fc384-105">In alternativa all'inserimento di tutte le opzioni nella riga di comando, il compilatore MIDL accetta i file di risposta che contengono opzioni e argomenti.</span><span class="sxs-lookup"><span data-stu-id="fc384-105">As an alternative to placing all the options on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="fc384-106">Un file di risposta è un file di testo contenente una o più opzioni della riga di comando del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="fc384-106">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="fc384-107">A differenza di una riga di comando, un file di risposta consente più righe di opzioni e nomi di file.</span><span class="sxs-lookup"><span data-stu-id="fc384-107">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="fc384-108">Ciò può essere utile a causa di limitazioni dell'ambiente di compilazione o per praticità del processo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="fc384-108">This may be useful due to limitations of your build environment or as a convenience for your build process.</span></span> <span data-ttu-id="fc384-109">È possibile specificare un file di risposta MIDL come:</span><span class="sxs-lookup"><span data-stu-id="fc384-109">You can specify a MIDL response file as:</span></span>

<span data-ttu-id="fc384-110">**midl** **\@ filename**</span><span class="sxs-lookup"><span data-stu-id="fc384-110">**midl** **\@filename**</span></span>

<dl> <dt>

<span data-ttu-id="fc384-111"><span id="filename"></span><span id="FILENAME"></span>*Filename*</span><span class="sxs-lookup"><span data-stu-id="fc384-111"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="fc384-112">Specifica il nome del file di risposta.</span><span class="sxs-lookup"><span data-stu-id="fc384-112">Specifies the name of the response file.</span></span> <span data-ttu-id="fc384-113">Il nome del file di risposta deve seguire immediatamente il carattere @ senza spazi vuoti tra il carattere @ e il nome del file di risposta.</span><span class="sxs-lookup"><span data-stu-id="fc384-113">The response file name must immediately follow the @ character with no white space between the @ character and the response file name.</span></span>

</dd> </dl>

<span data-ttu-id="fc384-114">Le opzioni in un file di risposta vengono interpretate come se fossero presenti in tale posizione nella riga di comando MIDL.</span><span class="sxs-lookup"><span data-stu-id="fc384-114">Options in a response file are interpreted as if they were present at that place in the MIDL command line.</span></span> <span data-ttu-id="fc384-115">Ogni argomento in un file di risposta deve iniziare e terminare sulla stessa riga.</span><span class="sxs-lookup"><span data-stu-id="fc384-115">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="fc384-116">Non è possibile usare il carattere barra rovesciata ( \\ ) per concatenare le righe.</span><span class="sxs-lookup"><span data-stu-id="fc384-116">You cannot use the backslash character (\\) to concatenate lines.</span></span>

<span data-ttu-id="fc384-117">MIDL supporta argomenti della riga di comando che includono uno o più file di risposta, combinati con altre opzioni della riga di comando:</span><span class="sxs-lookup"><span data-stu-id="fc384-117">MIDL supports command-line arguments that include one or more response files, combined with other command-line switches:</span></span>

<span data-ttu-id="fc384-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span><span class="sxs-lookup"><span data-stu-id="fc384-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span></span>

<span data-ttu-id="fc384-119">Il compilatore MIDL non supporta i file di risposta annidati.</span><span class="sxs-lookup"><span data-stu-id="fc384-119">The MIDL compiler does not support nested response files.</span></span>

 

 




