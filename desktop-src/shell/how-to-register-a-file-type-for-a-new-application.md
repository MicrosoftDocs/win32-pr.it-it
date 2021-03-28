---
description: Se si prevede di associare uno o più tipi di file a una nuova applicazione, è necessario definire un ProgID per ogni tipo di file che si desidera associare all'applicazione.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Come registrare un tipo di file per una nuova applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979527"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a><span data-ttu-id="337ca-103">Come registrare un tipo di file per una nuova applicazione</span><span class="sxs-lookup"><span data-stu-id="337ca-103">How to Register a File Type for a New Application</span></span>

<span data-ttu-id="337ca-104">Se si prevede di associare uno o più tipi di file a una nuova applicazione, è necessario definire un ProgID per ogni tipo di file che si desidera associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="337ca-104">If you plan to associate one or more file types with a new application, you must define a ProgID for each file type that you want to associate with the application.</span></span>

<span data-ttu-id="337ca-105">Per creare un ProgID per ogni tipo di file univoco gestito dall'applicazione, attenersi alla procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="337ca-105">To create a ProgID for each unique file type that your application handles, use these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="337ca-106">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="337ca-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="337ca-107">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="337ca-107">Step 1:</span></span>

<span data-ttu-id="337ca-108">Si noti che alcuni tipi di file hanno più estensioni che puntano allo stesso ProgID; Per esempio:</span><span class="sxs-lookup"><span data-stu-id="337ca-108">Note that some file types have multiple extensions that point to the same ProgID; for example:</span></span>

-   <span data-ttu-id="337ca-109">**HKEY \_ Classe \_ radice** \\ **app. jpeg** (ProgID)</span><span class="sxs-lookup"><span data-stu-id="337ca-109">**HKEY\_CLASSES\_ROOT**\\**App.jpeg** (your ProgID)</span></span>
-   <span data-ttu-id="337ca-110">**HKEY \_ Classes \_ root** \\ **. jpg** = app. jpeg (mapping dei tipi di file)</span><span class="sxs-lookup"><span data-stu-id="337ca-110">**HKEY\_CLASSES\_ROOT**\\ **.jpg** = App.jpeg (the file type mappings)</span></span>
-   <span data-ttu-id="337ca-111">**HKEY \_ Classe \_ root** \\ **. jpeg** = app. jpeg</span><span class="sxs-lookup"><span data-stu-id="337ca-111">**HKEY\_CLASSES\_ROOT**\\ **.jpeg** = App.jpeg</span></span>

### <a name="step-2"></a><span data-ttu-id="337ca-112">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="337ca-112">Step 2:</span></span>

<span data-ttu-id="337ca-113">Rimuovere i valori ProgID quando si installa e disinstalla il programma.</span><span class="sxs-lookup"><span data-stu-id="337ca-113">Remove the ProgID values when you install and uninstall your program.</span></span>

### <a name="step-3"></a><span data-ttu-id="337ca-114">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="337ca-114">Step 3:</span></span>

<span data-ttu-id="337ca-115">Lasciare invariati i mapping dei tipi di file in fase di disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="337ca-115">Leave the file type mappings unchanged at uninstall time.</span></span> <span data-ttu-id="337ca-116">Questa operazione funziona perché i mapping dei tipi di file vengono archiviati per utente nelle \_ classi HKEY \_ root \\ . ext e il sistema identifica il caso in cui il valore ProgID è mancante e lo ignora.</span><span class="sxs-lookup"><span data-stu-id="337ca-116">Doing so works because file type mappings are stored per user in HKEY\_CLASSES\_ROOT\\.ext, and the system identifies the case where the ProgID value is missing and ignores it.</span></span> <span data-ttu-id="337ca-117">Se si lasciano invariati i mapping dei tipi di file, si evita di dover disporre di codice condizionale che rimuove solo il mapping dei tipi di file se il valore fa ancora riferimento al ProgID.</span><span class="sxs-lookup"><span data-stu-id="337ca-117">Leaving file type mappings unchanged avoids the need to have conditional code that only removes the file type mapping if the value still points to your ProgID.</span></span> <span data-ttu-id="337ca-118">È importante evitare di eseguire questa operazione nei casi in cui potrebbe essere stato modificato da un'altra applicazione e pertanto non è possibile rimuovere facilmente il valore.</span><span class="sxs-lookup"><span data-stu-id="337ca-118">It is important to avoid doing so in cases where it might have been changed by another application and you thus cannot easily remove the value.</span></span>

### <a name="step-4"></a><span data-ttu-id="337ca-119">Passaggio 4:</span><span class="sxs-lookup"><span data-stu-id="337ca-119">Step 4:</span></span>

<span data-ttu-id="337ca-120">Specificare un valore univoco per la descrizione del tipo di file di ogni tipo di file ProgID eseguendo una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="337ca-120">Specify a unique value for the file type description of each file type ProgID by doing one of the following:</span></span>

-   <span data-ttu-id="337ca-121">Lasciare vuoto il valore predefinito del ProgID, nel qual caso il sistema usa il file. ext.</span><span class="sxs-lookup"><span data-stu-id="337ca-121">Leave the default value of the ProgID empty, in which case the system uses the .ext file.</span></span>
-   <span data-ttu-id="337ca-122">Fornire un valore localizzato tramite FriendlyTypeName e, per compatibilità con le applicazioni precedenti che leggono direttamente il registro di sistema, assicurarsi di specificare il valore predefinito del ProgID come descrizione del tipo di file, ovvero usare lo stesso valore a cui fa riferimento il FriendlyTypeName nella risorsa inglese.</span><span class="sxs-lookup"><span data-stu-id="337ca-122">Provide a localized value via FriendlyTypeName and, for compatibility with old applications that read the registry directly, be sure to provide the default value of the ProgID as the file type description (that is, use the same value that is referred to by the FriendlyTypeName in the English resource).</span></span>

## <a name="remarks"></a><span data-ttu-id="337ca-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="337ca-123">Remarks</span></span>

<span data-ttu-id="337ca-124">Se si prevede di associare il file a un'applicazione esistente, individuare un ProgID dell'applicazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="337ca-124">If you plan to associate the file with an existing application, locate an application ProgID in the registry.</span></span> <span data-ttu-id="337ca-125">Per ulteriori informazioni, vedere [tipi di file](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="337ca-125">For more information, see [File Types](fa-file-types.md).</span></span>

 

 



