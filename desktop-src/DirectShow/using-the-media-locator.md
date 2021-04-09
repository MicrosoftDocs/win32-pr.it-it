---
description: Uso di media Locator
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Uso di media Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968851"
---
# <a name="using-the-media-locator"></a><span data-ttu-id="67040-103">Uso di media Locator</span><span class="sxs-lookup"><span data-stu-id="67040-103">Using the Media Locator</span></span>

<span data-ttu-id="67040-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="67040-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="67040-105">Il localizzatore multimediale è un oggetto helper che verifica i nomi di file e cerca i file mancanti nelle directory locali o di rete.</span><span class="sxs-lookup"><span data-stu-id="67040-105">The media locator is a helper object that verifies file names and searches for missing files on local or network directories.</span></span> <span data-ttu-id="67040-106">Il rilevatore multimediale mantiene una cache dei percorsi di directory in cui i file sono stati trovati correttamente nelle ricerche precedenti.</span><span class="sxs-lookup"><span data-stu-id="67040-106">The media detector keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="67040-107">Per individuare un file, Cerca le directory nella relativa cache.</span><span class="sxs-lookup"><span data-stu-id="67040-107">To locate a file, it searches the directories in its cache.</span></span> <span data-ttu-id="67040-108">In caso contrario, il rilevatore multimediale può visualizzare una finestra di dialogo Apri file in cui l'utente può individuare manualmente un file.</span><span class="sxs-lookup"><span data-stu-id="67040-108">Failing that, the media detector can display an Open File dialog for the user to locate a file manually.</span></span> <span data-ttu-id="67040-109">Supponendo che l'utente trovi il file, il localizzatore multimediale aggiunge la nuova directory alla cache.</span><span class="sxs-lookup"><span data-stu-id="67040-109">Assuming the user locates the file, the media locator adds the new directory to its cache.</span></span> <span data-ttu-id="67040-110">Il localizzatore multimediale espone l'interfaccia [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="67040-110">The media locator exposes the [**IMediaLocator**](imedialocator.md) interface.</span></span>

<span data-ttu-id="67040-111">In genere, l'applicazione non crea direttamente un'istanza del localizzatore multimediale.</span><span class="sxs-lookup"><span data-stu-id="67040-111">Typically, your application does not directly create an instance of the media locator.</span></span> <span data-ttu-id="67040-112">Al contrario, la sequenza temporale e il motore di rendering forniscono i metodi seguenti per la convalida dei nomi di file tramite il rilevatore multimediale.</span><span class="sxs-lookup"><span data-stu-id="67040-112">Instead, the timeline and the render engine provide the following methods for validating file names using the media detector.</span></span>

-   <span data-ttu-id="67040-113">Per convalidare i nomi di file nella sequenza temporale, chiamare [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span><span class="sxs-lookup"><span data-stu-id="67040-113">To validate file names in the timeline, call [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span></span> <span data-ttu-id="67040-114">Facoltativamente, questo metodo aggiorna anche gli oggetti di origine con i nomi di file corretti.</span><span class="sxs-lookup"><span data-stu-id="67040-114">Optionally, this method also updates the source objects with the correct file names.</span></span>
-   <span data-ttu-id="67040-115">Per convalidare i nomi di file quando viene eseguito il rendering del progetto, chiamare [**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span><span class="sxs-lookup"><span data-stu-id="67040-115">To validate file names when the project is rendered, call [**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span></span>

<span data-ttu-id="67040-116">Entrambi i metodi accettano flag che controllano il comportamento del localizzatore multimediale.</span><span class="sxs-lookup"><span data-stu-id="67040-116">Both methods take flags that control the behavior of the media locator.</span></span> <span data-ttu-id="67040-117">Ad esempio, è possibile limitare la ricerca alle directory locali.</span><span class="sxs-lookup"><span data-stu-id="67040-117">For example, you can restrict the search to local directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67040-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67040-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67040-119">Utilizzo di origini</span><span class="sxs-lookup"><span data-stu-id="67040-119">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



