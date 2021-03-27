---
description: Un tipo percepito è una categoria di tipi di file che consente di identificare il tipo di file in Windows (e le applicazioni) come immagine, audio, documento o altro tipo.
title: Tipi percepiti (shell di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995277"
---
# <a name="perceived-types-the-windows-shell"></a><span data-ttu-id="7fa19-103">Tipi percepiti (shell di Windows)</span><span class="sxs-lookup"><span data-stu-id="7fa19-103">Perceived Types (The Windows Shell)</span></span>

<span data-ttu-id="7fa19-104">Un tipo percepito è una categoria di tipi di file che consente di identificare il tipo di file in Windows (e le applicazioni) come immagine, audio, documento o altro tipo.</span><span class="sxs-lookup"><span data-stu-id="7fa19-104">A perceived type is a category of file types that lets you identify your file type to Windows (and applications) as being an image, audio, document, or other type.</span></span> <span data-ttu-id="7fa19-105">I tipi percepiti vengono usati per diversi scopi, inclusa la determinazione del tipo di cartella, che viene quindi usato per impostare le impostazioni di visualizzazione predefinite.</span><span class="sxs-lookup"><span data-stu-id="7fa19-105">Perceived types are used for several purposes, including the determination of the folder type, which is then used to set the default view settings.</span></span> <span data-ttu-id="7fa19-106">Ad esempio, viene assegnata una modalità di visualizzazione predefinita delle anteprime a una cartella piena di file di tipo immagine percepita.</span><span class="sxs-lookup"><span data-stu-id="7fa19-106">For example, a folder full of files that are of the perceived type image is assigned a default view mode of thumbnails.</span></span>

<span data-ttu-id="7fa19-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="7fa19-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7fa19-108">Informazioni sui tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="7fa19-108">About Perceived Types</span></span>](#about-perceived-types)
-   [<span data-ttu-id="7fa19-109">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="7fa19-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="7fa19-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fa19-110">Related topics</span></span>](#related-topics)

## <a name="about-perceived-types"></a><span data-ttu-id="7fa19-111">Informazioni sui tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="7fa19-111">About Perceived Types</span></span>

<span data-ttu-id="7fa19-112">I tipi percepiti, definiti come valori PerceivedType, sono simili ai tipi di file, ad eccezione del fatto che fanno riferimento a grandi categorie di tipi di formato di file anziché a tipi di file specifici.</span><span class="sxs-lookup"><span data-stu-id="7fa19-112">Perceived types, defined as PerceivedType values, are similar to file types except that they refer to broad categories of file format types rather than specific file types.</span></span> <span data-ttu-id="7fa19-113">Ad esempio, immagine, testo, audio e compresso sono tipi percepiti.</span><span class="sxs-lookup"><span data-stu-id="7fa19-113">For example, image, text, audio, and compressed are perceived types.</span></span> <span data-ttu-id="7fa19-114">Ai tipi di file (in genere i tipi di file pubblici) può essere assegnato un tipo percepito e deve essere sempre assegnato uno ogni volta che ne è presente uno appropriato.</span><span class="sxs-lookup"><span data-stu-id="7fa19-114">File types (generally public file types) can be assigned a perceived type, and should always be assigned one whenever there is one that is appropriate.</span></span> <span data-ttu-id="7fa19-115">Ad esempio, i tipi di file di immagine. bmp,. png,. jpg e. gif sono anche di tipo immagine percepita.</span><span class="sxs-lookup"><span data-stu-id="7fa19-115">For example, the image file types .bmp, .png, .jpg, and .gif are also of perceived type image.</span></span>

<span data-ttu-id="7fa19-116">I tipi percepiti predefiniti sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7fa19-116">The default perceived types are as follows:</span></span>

-   <span data-ttu-id="7fa19-117">Cartella</span><span class="sxs-lookup"><span data-stu-id="7fa19-117">Folder</span></span>
-   <span data-ttu-id="7fa19-118">Testo</span><span class="sxs-lookup"><span data-stu-id="7fa19-118">Text</span></span>
-   <span data-ttu-id="7fa19-119">Immagine</span><span class="sxs-lookup"><span data-stu-id="7fa19-119">Image</span></span>
-   <span data-ttu-id="7fa19-120">Audio</span><span class="sxs-lookup"><span data-stu-id="7fa19-120">Audio</span></span>
-   <span data-ttu-id="7fa19-121">Video</span><span class="sxs-lookup"><span data-stu-id="7fa19-121">Video</span></span>
-   <span data-ttu-id="7fa19-122">Compresso</span><span class="sxs-lookup"><span data-stu-id="7fa19-122">Compressed</span></span>
-   <span data-ttu-id="7fa19-123">Documento</span><span class="sxs-lookup"><span data-stu-id="7fa19-123">Document</span></span>
-   <span data-ttu-id="7fa19-124">Sistema</span><span class="sxs-lookup"><span data-stu-id="7fa19-124">System</span></span>
-   <span data-ttu-id="7fa19-125">Applicazione</span><span class="sxs-lookup"><span data-stu-id="7fa19-125">Application</span></span>
-   <span data-ttu-id="7fa19-126">Gamemedia</span><span class="sxs-lookup"><span data-stu-id="7fa19-126">Gamemedia</span></span>
-   <span data-ttu-id="7fa19-127">Contatti</span><span class="sxs-lookup"><span data-stu-id="7fa19-127">Contacts</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fa19-128">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="7fa19-128">Additional Resources</span></span>

-   <span data-ttu-id="7fa19-129">Per informazioni su come registrare i tipi percepiti, vedere [registrazione dell'applicazione](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="7fa19-129">For information about how to register perceived types, see [Application Registration](app-registration.md).</span></span>
-   <span data-ttu-id="7fa19-130">Per un elenco di tipi percepiti predefiniti, vedere l'enumerazione [**percepita**](/windows/win32/api/shtypes/ne-shtypes-perceived) .</span><span class="sxs-lookup"><span data-stu-id="7fa19-130">For a list of default perceived types, see the [**PERCEIVED**](/windows/win32/api/shtypes/ne-shtypes-perceived) enumeration.</span></span>
-   <span data-ttu-id="7fa19-131">Per recuperare il tipo percepito di un file in base all'estensione del nome file, vedere la funzione [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .</span><span class="sxs-lookup"><span data-stu-id="7fa19-131">To retrieves a file's perceived type based on its file name extension, see the [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fa19-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fa19-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fa19-133">Registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="7fa19-133">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="7fa19-134">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="7fa19-134">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="7fa19-135">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="7fa19-135">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="7fa19-136">Visualizzazione contenuto per tipo di file o tipo</span><span class="sxs-lookup"><span data-stu-id="7fa19-136">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="7fa19-137">Tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="7fa19-137">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="7fa19-138">Gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="7fa19-138">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="7fa19-139">Identificatori a livello di codice</span><span class="sxs-lookup"><span data-stu-id="7fa19-139">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="7fa19-140">Matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="7fa19-140">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



