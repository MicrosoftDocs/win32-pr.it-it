---
description: Scrittura di un oggetto intestazione ASF per un nuovo file
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Scrittura di un oggetto intestazione ASF per un nuovo file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317303"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a><span data-ttu-id="d1b12-103">Scrittura di un oggetto intestazione ASF per un nuovo file</span><span class="sxs-lookup"><span data-stu-id="d1b12-103">Writing an ASF Header Object for a New File</span></span>

<span data-ttu-id="d1b12-104">Il valore ASF oggetto consente di archiviare le informazioni sull'oggetto intestazione ASF per un file.</span><span class="sxs-lookup"><span data-stu-id="d1b12-104">The ASF ContentInfo object stores ASF Header Object information for a file.</span></span> <span data-ttu-id="d1b12-105">Quando si crea o si modifica un file ASF, è necessario generare l'oggetto intestazione.</span><span class="sxs-lookup"><span data-stu-id="d1b12-105">When an ASF file is created or modified, the Header Object must be generated.</span></span> <span data-ttu-id="d1b12-106">A tale scopo, l'applicazione deve fornire il profilo di codifica del contenuto all'oggetto ContentInfo in modo che conosca le caratteristiche del file multimediale da creare.</span><span class="sxs-lookup"><span data-stu-id="d1b12-106">To do this, the application must provide the encoding profile of the content to the ContentInfo object so that it knows the characteristics of the media file to be created.</span></span>

<span data-ttu-id="d1b12-107">Per scrivere un nuovo file, è possibile usare l'oggetto ContentInfo per:</span><span class="sxs-lookup"><span data-stu-id="d1b12-107">For writing a new file, you can use the ContentInfo object to:</span></span>

-   <span data-ttu-id="d1b12-108">Raccogliere le informazioni di intestazione dall'oggetto profilo del file da creare.</span><span class="sxs-lookup"><span data-stu-id="d1b12-108">Collect header information from the profile object of the file to be created,</span></span>
-   <span data-ttu-id="d1b12-109">Popola i vari oggetti intestazione nella libreria ASF gestita internamente da Media Foundation,</span><span class="sxs-lookup"><span data-stu-id="d1b12-109">Populate various Header Objects in the ASF library maintained internally by Media Foundation,</span></span>
-   <span data-ttu-id="d1b12-110">Inizializzare [ASF Multiplexer](asf-multiplexer.md) per la generazione di pacchetti di dati ASF e</span><span class="sxs-lookup"><span data-stu-id="d1b12-110">Initialize the [ASF Multiplexer](asf-multiplexer.md) for ASF data packet generation, and</span></span>
-   <span data-ttu-id="d1b12-111">Costruisce l'oggetto intestazione di primo livello in formato binario che può essere scritto in un file.</span><span class="sxs-lookup"><span data-stu-id="d1b12-111">Construct the top-level Header Object in binary format that can be written to a file.</span></span>

<span data-ttu-id="d1b12-112">Per informazioni sui profili, vedere [profilo ASF](asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="d1b12-112">For information about profiles, see [ASF Profile](asf-profile.md).</span></span>

<span data-ttu-id="d1b12-113">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="d1b12-113">This section contains the following topics:</span></span>



| <span data-ttu-id="d1b12-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="d1b12-114">Topic</span></span>                                                                                                              | <span data-ttu-id="d1b12-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1b12-115">Description</span></span>                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1b12-116">Inizializzazione dell'oggetto ContentInfo di un nuovo file ASF</span><span class="sxs-lookup"><span data-stu-id="d1b12-116">Initializing the ContentInfo Object of a New ASF File</span></span>](initializing-the-contentinfo-object-of-a-new-asf-file.md) | <span data-ttu-id="d1b12-117">Viene descritto il metodo [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) che Inizializza l'oggetto ContentInfo con le informazioni di intestazione archiviate in un oggetto profilo.</span><span class="sxs-lookup"><span data-stu-id="d1b12-117">Describes the [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) method that initializes the ContentInfo object with header information stored in a profile object.</span></span> |
| [<span data-ttu-id="d1b12-118">Impostazione delle proprietà nell'oggetto ContentInfo</span><span class="sxs-lookup"><span data-stu-id="d1b12-118">Setting Properties in the ContentInfo Object</span></span>](setting-properties-in-the-contentinfo-object.md)                   | <span data-ttu-id="d1b12-119">Informazioni sulle varie proprietà di configurazione che devono essere impostate nell'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="d1b12-119">Information about various configuration properties that must be set on the ContentInfo object.</span></span>                                                                                         |
| [<span data-ttu-id="d1b12-120">Generazione di un nuovo oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="d1b12-120">Generating a New ASF Header Object</span></span>](generating-a-new-asf-header-object.md)                                       | <span data-ttu-id="d1b12-121">Come generare un buffer multimediale, che contiene l'oggetto intestazione ASF effettivo del nuovo file, dall'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="d1b12-121">How to generate a media buffer, which contains the actual ASF Header Object of the new file, from the ContentInfo object.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="d1b12-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1b12-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1b12-123">Oggetto ContentInfo ASF</span><span class="sxs-lookup"><span data-stu-id="d1b12-123">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="d1b12-124">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="d1b12-124">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="d1b12-125">Struttura di file ASF</span><span class="sxs-lookup"><span data-stu-id="d1b12-125">ASF File Structure</span></span>
</dt> </dl>

 

 



