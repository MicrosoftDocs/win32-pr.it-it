---
title: Modifiche al modello in modalità IME
description: Il modello in modalità IME è stato modificato da per utente a per thread
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443248"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="f86e1-103">Il modello in modalità IME è stato modificato da per utente a per thread</span><span class="sxs-lookup"><span data-stu-id="f86e1-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="f86e1-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="f86e1-104">Platforms</span></span>

<dl> <span data-ttu-id="f86e1-105">Client - Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f86e1-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="f86e1-106">Servers - Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f86e1-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="f86e1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f86e1-107">Description</span></span>

<span data-ttu-id="f86e1-108">In Windows 8, la modalità di conversione IME e la modalità frase IME si basavano sul contesto utente e la modifica della modalità di un'applicazione ha interessato tutte le altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f86e1-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="f86e1-109">Questo comportamento può essere disabilitato usando l'impostazione "Consenti di impostare un metodo di input diverso per ogni finestra dell'app" nella sezione impostazioni avanzate del pannello di controllo della lingua.</span><span class="sxs-lookup"><span data-stu-id="f86e1-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="f86e1-110">Per migliorare la compatibilità, in Windows 8.1 le modalità vengono archiviate in un contesto di input indipendentemente dalla modalità di impostazione del controllo "Consenti di impostare un metodo di input diverso per ogni finestra dell'app".</span><span class="sxs-lookup"><span data-stu-id="f86e1-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="f86e1-111">In Windows 8.1 l'impostazione "Consenti di impostare un metodo di input diverso per ogni finestra dell'app" influisce solo sulla selezione del metodo di input stesso.</span><span class="sxs-lookup"><span data-stu-id="f86e1-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="f86e1-112">All'avvio dell'applicazione, la modalità IME è impostata sul valore predefinito seguente:</span><span class="sxs-lookup"><span data-stu-id="f86e1-112">At application start up, the IME mode is set to the following defaults:</span></span>



| &nbsp;   | <span data-ttu-id="f86e1-113">Pannello di input software</span><span class="sxs-lookup"><span data-stu-id="f86e1-113">Software input panel</span></span> | <span data-ttu-id="f86e1-114">Tastiera hardware</span><span class="sxs-lookup"><span data-stu-id="f86e1-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="f86e1-115">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="f86e1-115">KOR, JPN</span></span> | <span data-ttu-id="f86e1-116">Attivato</span><span class="sxs-lookup"><span data-stu-id="f86e1-116">On</span></span>                   | <span data-ttu-id="f86e1-117">Disattivato</span><span class="sxs-lookup"><span data-stu-id="f86e1-117">Off</span></span>               |
| <span data-ttu-id="f86e1-118">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="f86e1-118">CHS,CHT</span></span>  | <span data-ttu-id="f86e1-119">On</span><span class="sxs-lookup"><span data-stu-id="f86e1-119">On</span></span>                   | <span data-ttu-id="f86e1-120">On</span><span class="sxs-lookup"><span data-stu-id="f86e1-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="f86e1-121">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="f86e1-121">Manifestations</span></span>

<span data-ttu-id="f86e1-122">Quando un utente modifica la modalità IME in un'applicazione, la modifica non influisce sulle altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f86e1-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="f86e1-123">Risorse</span><span class="sxs-lookup"><span data-stu-id="f86e1-123">Resources</span></span>

-   [<span data-ttu-id="f86e1-124">Valori della modalità di conversione IME</span><span class="sxs-lookup"><span data-stu-id="f86e1-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="f86e1-125">Valori della modalità frase IME</span><span class="sxs-lookup"><span data-stu-id="f86e1-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 