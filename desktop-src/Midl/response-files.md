---
title: File di risposta
description: In alternativa all'inserimento di tutte le opzioni nella riga di comando, il compilatore MIDL accetta i file di risposta che contengono opzioni e argomenti.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL compilatore MIDL, file di risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd949a3704b0669fd37c5629307a59df9742010
ms.sourcegitcommit: ad8bd914e19508a67af232d8d59c0e0ee9c3948b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/07/2019
ms.locfileid: "104397030"
---
# <a name="response-files"></a><span data-ttu-id="380f7-104">File di risposta</span><span class="sxs-lookup"><span data-stu-id="380f7-104">Response Files</span></span>

<span data-ttu-id="380f7-105">In alternativa all'inserimento di tutte le opzioni nella riga di comando, il compilatore MIDL accetta i file di risposta che contengono opzioni e argomenti.</span><span class="sxs-lookup"><span data-stu-id="380f7-105">As an alternative to placing all the options on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="380f7-106">Un file di risposta è un file di testo contenente una o più opzioni della riga di comando del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="380f7-106">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="380f7-107">A differenza di una riga di comando, un file di risposta consente più righe di opzioni e nomi di file.</span><span class="sxs-lookup"><span data-stu-id="380f7-107">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="380f7-108">Questo può essere utile a causa delle limitazioni dell'ambiente di compilazione o per praticità per il processo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="380f7-108">This may be useful due to limitations of your build environment or as a convenience for your build process.</span></span> <span data-ttu-id="380f7-109">È possibile specificare un file di risposta MIDL come:</span><span class="sxs-lookup"><span data-stu-id="380f7-109">You can specify a MIDL response file as:</span></span>

<span data-ttu-id="380f7-110"> **\@ nome file** MIDL</span><span class="sxs-lookup"><span data-stu-id="380f7-110">**midl** **\@filename**</span></span>

<dl> <dt>

<span data-ttu-id="380f7-111"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="380f7-111"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="380f7-112">Specifica il nome del file di risposta.</span><span class="sxs-lookup"><span data-stu-id="380f7-112">Specifies the name of the response file.</span></span> <span data-ttu-id="380f7-113">Il nome del file di risposta deve seguire immediatamente il carattere @ senza spazi vuoti tra il carattere @ e il nome del file di risposta.</span><span class="sxs-lookup"><span data-stu-id="380f7-113">The response file name must immediately follow the @ character with no white space between the @ character and the response file name.</span></span>

</dd> </dl>

<span data-ttu-id="380f7-114">Le opzioni in un file di risposta vengono interpretate come se fossero presenti in tale posizione nella riga di comando MIDL.</span><span class="sxs-lookup"><span data-stu-id="380f7-114">Options in a response file are interpreted as if they were present at that place in the MIDL command line.</span></span> <span data-ttu-id="380f7-115">Ogni argomento in un file di risposta deve iniziare e terminare sulla stessa riga.</span><span class="sxs-lookup"><span data-stu-id="380f7-115">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="380f7-116">Non è possibile usare il carattere barra rovesciata ( \) per concatenare le linee.</span><span class="sxs-lookup"><span data-stu-id="380f7-116">You cannot use the backslash character (\) to concatenate lines.</span></span>

<span data-ttu-id="380f7-117">MIDL supporta gli argomenti della riga di comando che includono uno o più file di risposta, combinati con altre opzioni della riga di comando:</span><span class="sxs-lookup"><span data-stu-id="380f7-117">MIDL supports command-line arguments that include one or more response files, combined with other command-line switches:</span></span>

<span data-ttu-id="380f7-118">**MIDL-Oicf @midl1.rsp -envwin32 @midl2.rsp ITF. idl**</span><span class="sxs-lookup"><span data-stu-id="380f7-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span></span>

<span data-ttu-id="380f7-119">Il compilatore MIDL non supporta i file di risposta annidati.</span><span class="sxs-lookup"><span data-stu-id="380f7-119">The MIDL compiler does not support nested response files.</span></span>

 

 




