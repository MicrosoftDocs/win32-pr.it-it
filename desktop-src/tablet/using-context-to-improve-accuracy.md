---
description: Un motore di riconoscimento della grafia, o un riconoscimento, è un software che elabora input penna e converte tale input penna in testo.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Uso del contesto per migliorare l'accuratezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306719"
---
# <a name="using-context-to-improve-accuracy"></a><span data-ttu-id="1c688-103">Uso del contesto per migliorare l'accuratezza</span><span class="sxs-lookup"><span data-stu-id="1c688-103">Using Context to Improve Accuracy</span></span>

<span data-ttu-id="1c688-104">Un motore di riconoscimento della grafia, o un riconoscimento, è un software che elabora input penna e converte tale input penna in testo.</span><span class="sxs-lookup"><span data-stu-id="1c688-104">A handwriting recognition engine, or recognizer, is software that processes ink and converts that ink into text.</span></span> <span data-ttu-id="1c688-105">Un contesto è pertinente, le informazioni specifiche dell'applicazione fornite a un riconoscimento per migliorare l'accuratezza del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="1c688-105">A context is relevant, application-specific information that you provide to a recognizer to improve recognition accuracy.</span></span> <span data-ttu-id="1c688-106">In altre parole, context è qualsiasi informazione sull'input che aiuta il riconoscimento nell'elaborare accuratamente l'input penna in un campo.</span><span class="sxs-lookup"><span data-stu-id="1c688-106">In other words, context is any piece of information about input that aids the recognizer in accurately processing the ink in a field.</span></span>

<span data-ttu-id="1c688-107">In questa sezione vengono descritti i diversi modi in cui è possibile sfruttare il contesto nell'applicazione per Tablet PC, ponendo l'accento sulla tecnica di programmazione preferita per le applicazioni che non sono abilitate per l'input penna.</span><span class="sxs-lookup"><span data-stu-id="1c688-107">This section describes the different ways you can take advantage of context in your Tablet PC application, placing emphasis on the preferred programmatic technique for applications that are not ink enabled.</span></span>

> [!Note]  
> <span data-ttu-id="1c688-108">Sono disponibili alcune sezioni della tecnologia Tablet PC di Windows Vista Software Development Kit (SDK) in cui viene usato il termine "contesto" in relazione all'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) e alle relative proprietà [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) e [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) .</span><span class="sxs-lookup"><span data-stu-id="1c688-108">There are places in the Tablet PC Technology sections of the Windows Vista Software Development Kit (SDK) where the term "context" is used in regard to the [**RecognizerContext**](inkrecognizercontext-class.md) object and its [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) and [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) properties.</span></span> <span data-ttu-id="1c688-109">Non confondere questi altri utilizzi di "context" con la definizione in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="1c688-109">Do not confuse these other usages of "context" with the definition in this section.</span></span>

 

 

 



