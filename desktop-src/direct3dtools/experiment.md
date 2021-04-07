---
description: Rappresenta le informazioni su un esperimento (acquisizione).
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura dell'esperimento
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746442"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span data-ttu-id="9a768-103"><span id="vspixengine.experiment"></span>Struttura dell'esperimento</span><span class="sxs-lookup"><span data-stu-id="9a768-103"><span id="vspixengine.experiment"></span>Experiment structure</span></span>

<span data-ttu-id="9a768-104">Rappresenta le informazioni su un esperimento (acquisizione).</span><span class="sxs-lookup"><span data-stu-id="9a768-104">Represents information about an experiment (capture).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a768-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a768-105">Syntax</span></span>


```C++
} Experiment;
```

## <a name="members"></a><span data-ttu-id="9a768-106">Members</span><span class="sxs-lookup"><span data-stu-id="9a768-106">Members</span></span>

<span data-ttu-id="9a768-107">**processId**</span><span class="sxs-lookup"><span data-stu-id="9a768-107">**processId**</span></span>  
<span data-ttu-id="9a768-108">ID del processo associato.</span><span class="sxs-lookup"><span data-stu-id="9a768-108">The associated process ID.</span></span>

<span data-ttu-id="9a768-109">**applicationName**</span><span class="sxs-lookup"><span data-stu-id="9a768-109">**applicationName**</span></span>  
<span data-ttu-id="9a768-110">Stringa COM contenente il nome dell'applicazione in cui eseguire l'esperimento.</span><span class="sxs-lookup"><span data-stu-id="9a768-110">A COM string containing the name of the application to run the experiment on.</span></span>

<span data-ttu-id="9a768-111">**commandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="9a768-111">**commandLineArguments**</span></span>  
<span data-ttu-id="9a768-112">Stringa COM contenente gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9a768-112">A COM string containing the command line arguments.</span></span>

<span data-ttu-id="9a768-113">**workingDirectory**</span><span class="sxs-lookup"><span data-stu-id="9a768-113">**workingDirectory**</span></span>  
<span data-ttu-id="9a768-114">Stringa COM contenente il percorso della directory di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9a768-114">A COM string containing the path of the working directory.</span></span>

<span data-ttu-id="9a768-115">**tempPixRunFile**</span><span class="sxs-lookup"><span data-stu-id="9a768-115">**tempPixRunFile**</span></span>  
<span data-ttu-id="9a768-116">Stringa COM contenente il FilePath del file temporaneo usato per eseguire l'esperimento.</span><span class="sxs-lookup"><span data-stu-id="9a768-116">A COM string containing the filepath of the temporary file used to perform the experiment.</span></span>

<span data-ttu-id="9a768-117">**startOption**</span><span class="sxs-lookup"><span data-stu-id="9a768-117">**startOption**</span></span>  
<span data-ttu-id="9a768-118">Opzione di avvio associata all'esperimento.</span><span class="sxs-lookup"><span data-stu-id="9a768-118">The start option associated with the experiment.</span></span>

<span data-ttu-id="9a768-119">**experimentType**</span><span class="sxs-lookup"><span data-stu-id="9a768-119">**experimentType**</span></span>  
<span data-ttu-id="9a768-120">Tipo di esperimento (acquisizione).</span><span class="sxs-lookup"><span data-stu-id="9a768-120">The kind of experiment (capture).</span></span>

<span data-ttu-id="9a768-121">**uiLocale**</span><span class="sxs-lookup"><span data-stu-id="9a768-121">**uiLocale**</span></span>  
<span data-ttu-id="9a768-122">ID delle impostazioni locali utilizzate per gli elementi di sovrapposizione dell'interfaccia utente durante il experiement (acquisizione).</span><span class="sxs-lookup"><span data-stu-id="9a768-122">The ID of the locale used for UI overlay elements during the experiement (capture).</span></span> <span data-ttu-id="9a768-123">Viene passato dall'host (ad esempio Visual Studio Diagnostica della grafica) al motore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9a768-123">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

<span data-ttu-id="9a768-124">**registryRoot**</span><span class="sxs-lookup"><span data-stu-id="9a768-124">**registryRoot**</span></span>  
<span data-ttu-id="9a768-125">Stringa COM contenente la radice del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9a768-125">A COM string containing the registry root.</span></span> <span data-ttu-id="9a768-126">Viene passato dall'host (ad esempio Visual Studio Diagnostica della grafica) al motore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9a768-126">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a768-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a768-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9a768-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a768-128">Header</span></span></p></td><td><span data-ttu-id="9a768-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9a768-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



