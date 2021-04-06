---
title: Informazioni sulle funzioni e le macro AVIFile
description: Informazioni sulle funzioni e le macro AVIFile
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- AVIFileInit (funzione)
- AVIFileExit (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045326"
---
# <a name="about-avifile-functions-and-macros"></a><span data-ttu-id="8370d-105">Informazioni sulle funzioni e le macro AVIFile</span><span class="sxs-lookup"><span data-stu-id="8370d-105">About AVIFile Functions and Macros</span></span>

<span data-ttu-id="8370d-106">Le funzioni e le macro AVIFile gestiscono le informazioni nei file basati sul tempo come uno o più *flussi di dati* anziché blocchi di dati contrassegnati, detti blocchi.</span><span class="sxs-lookup"><span data-stu-id="8370d-106">The AVIFile functions and macros handle the information in time-based files as one or more *data streams* instead of tagged blocks of data called chunks.</span></span> <span data-ttu-id="8370d-107">I flussi di dati fanno riferimento ai componenti di un file basato sul tempo.</span><span class="sxs-lookup"><span data-stu-id="8370d-107">Data streams refer to the components of a time-based file.</span></span> <span data-ttu-id="8370d-108">Un file AVI può contenere diversi tipi di dati, ad esempio una sequenza video, una colonna musicale inglese e una colonna musicale francese.</span><span class="sxs-lookup"><span data-stu-id="8370d-108">An AVI file can contain several different types of data, such as a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="8370d-109">Utilizzando AVIFile, un'applicazione può accedere separatamente a ognuno di questi componenti.</span><span class="sxs-lookup"><span data-stu-id="8370d-109">Using AVIFile, an application can access each of these components separately.</span></span>

> [!Note]  
> <span data-ttu-id="8370d-110">Sebbene le funzioni e le macro AVIFile funzionino con qualsiasi file di RIFF, questa panoramica ne illustra l'uso solo con i file AVI.</span><span class="sxs-lookup"><span data-stu-id="8370d-110">Although the AVIFile functions and macros work with any RIFF file, this overview demonstrates their use with AVI files only.</span></span> <span data-ttu-id="8370d-111">I file AVI sono in genere i file basati sul tempo usati con le macro e le funzioni di AVIFile.</span><span class="sxs-lookup"><span data-stu-id="8370d-111">AVI files are typically the time-based files used with the AVIFile macros and functions.</span></span>

 

<span data-ttu-id="8370d-112">Le funzioni e le macro AVIFile sono contenute in una libreria a collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="8370d-112">AVIFile functions and macros are contained in a dynamic-link library.</span></span> <span data-ttu-id="8370d-113">Per inizializzare la libreria, usare la funzione [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) .</span><span class="sxs-lookup"><span data-stu-id="8370d-113">To initialize the library, use the [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) function.</span></span> <span data-ttu-id="8370d-114">Dopo aver inizializzato la libreria, è possibile usare qualsiasi funzione o macro AVIFile.</span><span class="sxs-lookup"><span data-stu-id="8370d-114">After you initialize the library, you can use any of the AVIFile functions or macros.</span></span> <span data-ttu-id="8370d-115">Per rilasciare la libreria, usare la funzione [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) .</span><span class="sxs-lookup"><span data-stu-id="8370d-115">To release the library, use the [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) function.</span></span> <span data-ttu-id="8370d-116">AVIFile gestisce un conteggio dei riferimenti delle applicazioni che usano la libreria, ma non quelle che lo hanno rilasciato.</span><span class="sxs-lookup"><span data-stu-id="8370d-116">AVIFile maintains a reference count of the applications that are using the library, but not those that have released it.</span></span> <span data-ttu-id="8370d-117">Le applicazioni devono bilanciare ogni uso di **AVIFileInit** con una chiamata a **AVIFileExit** per rilasciare completamente la libreria al termine dell'uso di ogni applicazione.</span><span class="sxs-lookup"><span data-stu-id="8370d-117">Your applications should balance each use of **AVIFileInit** with a call to **AVIFileExit** to completely release the library after each application finishes using it.</span></span>

 

 




