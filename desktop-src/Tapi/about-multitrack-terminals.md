---
description: Un terminale multitraccia può essere considerato come un terminale che è una raccolta di altri terminali. Ogni terminale figlio (a &\# 0034; track&\# 0034;) può essere un terminale multitraccia o un terminale a traccia singola.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: Informazioni sui terminali multitraccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311914"
---
# <a name="about-multitrack-terminals"></a><span data-ttu-id="1bf0d-104">Informazioni sui terminali multitraccia</span><span class="sxs-lookup"><span data-stu-id="1bf0d-104">About Multitrack Terminals</span></span>

<span data-ttu-id="1bf0d-105">Un terminale multitraccia può essere considerato come un terminale che è una raccolta di altri terminali.</span><span class="sxs-lookup"><span data-stu-id="1bf0d-105">A multitrack terminal can be thought of as a terminal that is a collection of other terminals.</span></span> <span data-ttu-id="1bf0d-106">Ogni terminale figlio ("Track") può essere un terminale multitraccia o un terminale a singolo rilevamento.</span><span class="sxs-lookup"><span data-stu-id="1bf0d-106">Each child terminal (a "track") can be a multitrack terminal or a single-track terminal.</span></span>

<span data-ttu-id="1bf0d-107">Tutti i terminali Multitrack espongono l'interfaccia [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , che include metodi generici per l'enumerazione, la creazione e la rimozione di terminali di rilevamento da un terminale multitraccia.</span><span class="sxs-lookup"><span data-stu-id="1bf0d-107">All multitrack terminals expose the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which includes generic methods for enumerating, creating, and removing track terminals from a multitrack terminal.</span></span> <span data-ttu-id="1bf0d-108">Tutti i terminali, a traccia singola e multitraccia, espongono l'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="1bf0d-108">All terminals, single-track and multitrack, expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

<span data-ttu-id="1bf0d-109">Un client che dispone di un puntatore a un'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) può individuare se il terminale è multitraccia o a traccia singola eseguendo una query sul terminale per l'interfaccia [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , che viene esposta solo nei terminali Multitrack.</span><span class="sxs-lookup"><span data-stu-id="1bf0d-109">A client that has a pointer to an [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface can discover whether the terminal is multitrack or single-track by querying the terminal for the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which is exposed only on multitrack terminals.</span></span>

<span data-ttu-id="1bf0d-110">Il terminale padre può usare l'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) dei terminali di tracking oppure potrebbe essere necessario tenere traccia dei terminali per esporre le interfacce private.</span><span class="sxs-lookup"><span data-stu-id="1bf0d-110">The parent terminal may use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of its track terminals, or it may require track terminals to expose private interfaces.</span></span>

<span data-ttu-id="1bf0d-111">Per altre informazioni, vedere [tenere traccia dei terminali](track-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="1bf0d-111">For more information, see [Track Terminals](track-terminals.md).</span></span>

 

 
