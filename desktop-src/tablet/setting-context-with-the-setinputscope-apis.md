---
description: La tecnica di programmazione consigliata per l'impostazione di contesti in un'applicazione che non è abilitata per l'input penna consiste nell'utilizzare le funzioni SetInputScope per associare il contesto ai campi nell'applicazione.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Impostazione del contesto con le API SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313914"
---
# <a name="setting-context-with-the-setinputscope-apis"></a><span data-ttu-id="24381-103">Impostazione del contesto con le API SetInputScope</span><span class="sxs-lookup"><span data-stu-id="24381-103">Setting Context with the SetInputScope APIs</span></span>

<span data-ttu-id="24381-104">La tecnica di programmazione consigliata per l'impostazione di contesti in un'applicazione che non è abilitata per l'input penna consiste nell'utilizzare le funzioni [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) per associare il contesto ai campi nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24381-104">The recommended programmatic technique for setting contexts in an application that is not ink enabled is to use the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions to associate context with the fields in the application.</span></span>

<span data-ttu-id="24381-105">Microsoft Windows XP Tablet PC Edition Development Kit 1,7 è stata la prima versione di Microsoft Windows a offrire [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span><span class="sxs-lookup"><span data-stu-id="24381-105">The Microsoft Windows XP Tablet PC Edition Development Kit 1.7 was the first version of Microsoft Windows to offer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span> <span data-ttu-id="24381-106">Windows Vista fornisce anche il supporto per queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="24381-106">Windows Vista also provides support for these functions.</span></span> <span data-ttu-id="24381-107">Le definizioni **SetInputScope** sono dichiarate in InputScope. idl e InputScope. h.</span><span class="sxs-lookup"><span data-stu-id="24381-107">The **SetInputScope** definitions are declared in InputScope.idl and InputScope.h.</span></span> <span data-ttu-id="24381-108">Per altre informazioni, vedere [Framework di servizi di testo](../tsf/text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="24381-108">For more details, see [Text Services Framework](../tsf/text-services-framework.md).</span></span>

<span data-ttu-id="24381-109">Le funzioni [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) rappresentano la modalità consigliata per impostare il contesto per i controlli e le applicazioni che non sono abilitati per l'input penna.</span><span class="sxs-lookup"><span data-stu-id="24381-109">The [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions are the recommended way to set context for controls and applications that are not ink enabled.</span></span>

## <a name="common-input-scopes"></a><span data-ttu-id="24381-110">Ambiti di input comuni</span><span class="sxs-lookup"><span data-stu-id="24381-110">Common Input Scopes</span></span>

<span data-ttu-id="24381-111">Utilizzando le funzioni [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) e il set definito di ambiti di input comuni descritti nell'enumerazione [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , è possibile migliorare l'accuratezza del riconoscimento dei riconoscitori della grafia Microsoft.</span><span class="sxs-lookup"><span data-stu-id="24381-111">Using the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions and the defined set of common input scopes described in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration, you can improve the recognition accuracy of the Microsoft handwriting recognizers.</span></span>

> [!Note]  
> <span data-ttu-id="24381-112">I riconoscitori per la lingua inglese (Stati Uniti), inglese (Regno Unito), tedesco, francese, italiano, spagnolo, olandese e portoghese attualmente supportano l'utilizzo degli ambiti di input comuni con [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span><span class="sxs-lookup"><span data-stu-id="24381-112">The recognizers for English (United States), English (United Kingdom), German, French, Italian, Spanish, Dutch, and Portuguese currently support using the common input scopes with [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span>

 

 

 
