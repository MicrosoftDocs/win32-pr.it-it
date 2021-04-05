---
title: Oggetto SpeechInput
description: Oggetto SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955624"
---
# <a name="the-speechinput-object"></a><span data-ttu-id="7c1de-103">Oggetto SpeechInput</span><span class="sxs-lookup"><span data-stu-id="7c1de-103">The SpeechInput Object</span></span>

<span data-ttu-id="7c1de-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c1de-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7c1de-105">L'oggetto [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) fornisce l'accesso alle proprietà di input vocale gestite dal server agente.</span><span class="sxs-lookup"><span data-stu-id="7c1de-105">The [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) object provides access to the speech input properties maintained by the Agent server.</span></span> <span data-ttu-id="7c1de-106">Le proprietà sono di sola lettura per le applicazioni client, ma l'utente può modificarle nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="7c1de-106">The properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="7c1de-107">Il server restituisce valori solo se è stato installato e abilitato un motore di riconoscimento vocale compatibile.</span><span class="sxs-lookup"><span data-stu-id="7c1de-107">The server returns values only if a compatible speech engine has been installed and is enabled.</span></span>

<span data-ttu-id="7c1de-108">Le proprietà [**Engine**](https://www.bing.com/search?q=**Engine**), [**installato**](https://www.bing.com/search?q=**Installed**)e [**Language**](https://www.bing.com/search?q=**Language**) non sono più supportate, ma, per compatibilità con le versioni precedenti, restituiscono valori null in caso di query.</span><span class="sxs-lookup"><span data-stu-id="7c1de-108">The [**Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**), and [**Language**](https://www.bing.com/search?q=**Language**) properties are no longer supported, but (for backward compatibility) return null values if queried.</span></span> <span data-ttu-id="7c1de-109">Per eseguire una query o impostare la modalità di riconoscimento vocale, utilizzare la proprietà [**SRModeID**](srmodeid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1de-109">To query or set a speech recognition's mode, use the [**SRModeID**](srmodeid-property.md) property.</span></span>

-   [<span data-ttu-id="7c1de-110">Proprietà di SpeechInput</span><span class="sxs-lookup"><span data-stu-id="7c1de-110">SpeechInput Properties</span></span>](speechinput-properties.md)

 

 




