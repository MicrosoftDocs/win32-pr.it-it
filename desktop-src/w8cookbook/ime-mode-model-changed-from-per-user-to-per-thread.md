---
title: Modifiche al modello in modalità IME
description: Modello in modalità IME modificato da per utente a per thread
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781c322949f17d4d3313b6a9b7b5eff9b1e83b06
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338838"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="e6d68-103">Modello in modalità IME modificato da per utente a per thread</span><span class="sxs-lookup"><span data-stu-id="e6d68-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="e6d68-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="e6d68-104">Platforms</span></span>

<dl> <span data-ttu-id="e6d68-105">Client-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e6d68-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="e6d68-106">Server-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e6d68-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="e6d68-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6d68-107">Description</span></span>

<span data-ttu-id="e6d68-108">In Windows 8, la modalità di conversione IME e la modalità frase IME sono basate sul contesto utente e la modifica della modalità di un'applicazione ha interessato tutte le altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e6d68-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="e6d68-109">Questo comportamento può essere disabilitato usando l'impostazione "Consenti impostazione di un metodo di input diverso per ogni finestra dell'app" nella sezione Impostazioni avanzate del pannello di controllo della lingua.</span><span class="sxs-lookup"><span data-stu-id="e6d68-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="e6d68-110">Per migliorare la compatibilità, in Windows 8.1 le modalità vengono archiviate in un contesto di input indipendentemente dalla modalità di impostazione del controllo "Consenti impostazione di un metodo di input diverso per ogni finestra dell'app".</span><span class="sxs-lookup"><span data-stu-id="e6d68-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="e6d68-111">In Windows 8.1 l'impostazione "Consenti impostazione di un metodo di input diverso per ogni finestra dell'app" influiscono solo sulla selezione del metodo di input.</span><span class="sxs-lookup"><span data-stu-id="e6d68-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="e6d68-112">All'avvio dell'applicazione, la modalità IME è impostata sui valori predefiniti seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6d68-112">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="e6d68-113">Pannello di input software</span><span class="sxs-lookup"><span data-stu-id="e6d68-113">Software input panel</span></span> | <span data-ttu-id="e6d68-114">Tastiera hardware</span><span class="sxs-lookup"><span data-stu-id="e6d68-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="e6d68-115">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="e6d68-115">KOR, JPN</span></span> | <span data-ttu-id="e6d68-116">Attivato</span><span class="sxs-lookup"><span data-stu-id="e6d68-116">On</span></span>                   | <span data-ttu-id="e6d68-117">Disattivato</span><span class="sxs-lookup"><span data-stu-id="e6d68-117">Off</span></span>               |
| <span data-ttu-id="e6d68-118">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="e6d68-118">CHS,CHT</span></span>  | <span data-ttu-id="e6d68-119">Attivato</span><span class="sxs-lookup"><span data-stu-id="e6d68-119">On</span></span>                   | <span data-ttu-id="e6d68-120">Attivato</span><span class="sxs-lookup"><span data-stu-id="e6d68-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="e6d68-121">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="e6d68-121">Manifestations</span></span>

<span data-ttu-id="e6d68-122">Quando un utente modifica la modalità IME in un'applicazione, la modifica non influisce sulle altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e6d68-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="e6d68-123">Risorse</span><span class="sxs-lookup"><span data-stu-id="e6d68-123">Resources</span></span>

-   [<span data-ttu-id="e6d68-124">Valori della modalità di conversione IME</span><span class="sxs-lookup"><span data-stu-id="e6d68-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="e6d68-125">Valori della modalità frase IME</span><span class="sxs-lookup"><span data-stu-id="e6d68-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 