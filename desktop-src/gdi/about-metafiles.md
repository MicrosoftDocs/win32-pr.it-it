---
description: Internamente, un metafile è una matrice di strutture a lunghezza variabile denominate record metafile.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Informazioni sui metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753594"
---
# <a name="about-metafiles"></a><span data-ttu-id="780c1-103">Informazioni sui metafile</span><span class="sxs-lookup"><span data-stu-id="780c1-103">About Metafiles</span></span>

<span data-ttu-id="780c1-104">Internamente, un metafile è una matrice di strutture a lunghezza variabile denominate *record metafile*.</span><span class="sxs-lookup"><span data-stu-id="780c1-104">Internally, a metafile is an array of variable-length structures called *metafile records*.</span></span> <span data-ttu-id="780c1-105">I primi record del metafile specificano informazioni generali, ad esempio la risoluzione del dispositivo in cui è stata creata l'immagine, le dimensioni dell'immagine e così via.</span><span class="sxs-lookup"><span data-stu-id="780c1-105">The first records in the metafile specify general information such as the resolution of the device on which the picture was created, the dimensions of the picture, and so on.</span></span> <span data-ttu-id="780c1-106">I record rimanenti, che costituiscono la maggior parte dei metafile, corrispondono alle funzioni GDI (Graphics Device Interface) necessarie per tracciare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="780c1-106">The remaining records, which constitute the bulk of any metafile, correspond to the graphics device interface (GDI) functions required to draw the picture.</span></span> <span data-ttu-id="780c1-107">Questi record vengono archiviati nel metafile dopo la creazione di un contesto di dispositivo metafile speciale.</span><span class="sxs-lookup"><span data-stu-id="780c1-107">These records are stored in the metafile after a special metafile device context is created.</span></span> <span data-ttu-id="780c1-108">Questo contesto di dispositivo metafile viene quindi utilizzato per tutte le operazioni di disegno necessarie per la creazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="780c1-108">This metafile device context is then used for all drawing operations required to create the picture.</span></span> <span data-ttu-id="780c1-109">Quando il sistema elabora una funzione GDI associata a un controller di dominio metafile, converte la funzione nei dati appropriati e archivia questi dati in un record aggiunto al metafile.</span><span class="sxs-lookup"><span data-stu-id="780c1-109">When the system processes a GDI function associated with a metafile DC, it converts the function into the appropriate data and stores this data in a record appended to the metafile.</span></span>

<span data-ttu-id="780c1-110">Una volta completata un'immagine e l'ultimo record viene archiviato nel metafile, è possibile passare il metafile a un'altra applicazione per:</span><span class="sxs-lookup"><span data-stu-id="780c1-110">After a picture is complete and the last record is stored in the metafile, you can pass the metafile to another application by:</span></span>

-   <span data-ttu-id="780c1-111">Uso degli Appunti</span><span class="sxs-lookup"><span data-stu-id="780c1-111">Using the clipboard</span></span>
-   <span data-ttu-id="780c1-112">Incorporamento in un altro file</span><span class="sxs-lookup"><span data-stu-id="780c1-112">Embedding it within another file</span></span>
-   <span data-ttu-id="780c1-113">Archiviazione su disco</span><span class="sxs-lookup"><span data-stu-id="780c1-113">Storing it on disk</span></span>
-   <span data-ttu-id="780c1-114">Riproduzione ripetuta</span><span class="sxs-lookup"><span data-stu-id="780c1-114">Playing it repeatedly</span></span>

<span data-ttu-id="780c1-115">Un metafile viene *riprodotto* quando i relativi record vengono convertiti in comandi del dispositivo ed elaborati dal dispositivo appropriato.</span><span class="sxs-lookup"><span data-stu-id="780c1-115">A metafile is *played* when its records are converted to device commands and processed by the appropriate device.</span></span>

<span data-ttu-id="780c1-116">Esistono due tipi di metafile:</span><span class="sxs-lookup"><span data-stu-id="780c1-116">There are two types of metafiles:</span></span>

-   [<span data-ttu-id="780c1-117">File di formato avanzato</span><span class="sxs-lookup"><span data-stu-id="780c1-117">Enhanced-format metafiles</span></span>](enhanced-format-metafiles.md)
-   [<span data-ttu-id="780c1-118">Metafile in formato Windows</span><span class="sxs-lookup"><span data-stu-id="780c1-118">Windows-format metafiles</span></span>](windows-format-metafiles.md)

 

 



