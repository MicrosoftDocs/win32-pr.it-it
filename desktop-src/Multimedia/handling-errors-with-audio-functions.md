---
title: Gestione degli errori con funzioni audio
description: Gestione degli errori con funzioni audio
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- audio multimediale, errori audio della forma d'onda
- audio, errori audio della forma d'onda
- audio multimediale, errori audio ausiliari
- audio, errori audio ausiliari
- audio Waveform, errori
- audio ausiliario, errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337007"
---
# <a name="handling-errors-with-audio-functions"></a><span data-ttu-id="6b37e-109">Gestione degli errori con funzioni audio</span><span class="sxs-lookup"><span data-stu-id="6b37e-109">Handling Errors with Audio Functions</span></span>

<span data-ttu-id="6b37e-110">Le funzioni Waveform-Audio e ausiliario-audio restituiscono un valore diverso da zero quando si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="6b37e-110">The waveform-audio and auxiliary-audio functions return a nonzero value when an error occurs.</span></span> <span data-ttu-id="6b37e-111">Windows fornisce funzioni che convertono questi valori di errore in descrizioni testuali degli errori.</span><span class="sxs-lookup"><span data-stu-id="6b37e-111">Windows provides functions that convert these error values into textual descriptions of the errors.</span></span> <span data-ttu-id="6b37e-112">L'applicazione deve comunque esaminare i valori di errore per determinare il modo in cui procedere, ma le descrizioni testuali degli errori possono essere utilizzate nelle finestre di dialogo che descrivono gli errori agli utenti.</span><span class="sxs-lookup"><span data-stu-id="6b37e-112">The application must still examine the error values to determine how to proceed, but textual descriptions of errors can be used in dialog boxes that describe errors to users.</span></span>

<span data-ttu-id="6b37e-113">È possibile utilizzare le funzioni seguenti per recuperare le descrizioni testuali dei valori di errore audio:</span><span class="sxs-lookup"><span data-stu-id="6b37e-113">You can use the following functions to retrieve textual descriptions of audio error values:</span></span>



| <span data-ttu-id="6b37e-114">Funzione</span><span class="sxs-lookup"><span data-stu-id="6b37e-114">Function</span></span>                                           | <span data-ttu-id="6b37e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b37e-115">Description</span></span>                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="6b37e-116">**waveInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="6b37e-116">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | <span data-ttu-id="6b37e-117">Recupera una descrizione testuale di un errore di input audio e di forma d'onda specificato.</span><span class="sxs-lookup"><span data-stu-id="6b37e-117">Retrieves a textual description of a specified waveform-audio input error.</span></span>  |
| [<span data-ttu-id="6b37e-118">**waveOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="6b37e-118">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | <span data-ttu-id="6b37e-119">Recupera una descrizione testuale di un errore di output della forma d'onda-audio specificato.</span><span class="sxs-lookup"><span data-stu-id="6b37e-119">Retrieves a textual description of a specified waveform-audio output error.</span></span> |



 

<span data-ttu-id="6b37e-120">Le uniche funzioni audio che non restituiscono valori di errore sono [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)e [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span><span class="sxs-lookup"><span data-stu-id="6b37e-120">The only audio functions that do not return error values are [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs), and [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span></span> <span data-ttu-id="6b37e-121">Queste funzioni restituiscono zero se non sono presenti dispositivi in un sistema o se si verificano errori.</span><span class="sxs-lookup"><span data-stu-id="6b37e-121">These functions return zero if no devices are present in a system or if they encounter any errors.</span></span>

 

 