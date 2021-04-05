---
description: La versione di debug del motore XAudio2 convalida i parametri e fornisce messaggi di avviso e di errore dettagliati.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Funzionalità di debug XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752410"
---
# <a name="xaudio2-debugging-facilities"></a><span data-ttu-id="5ea70-103">Funzionalità di debug XAudio2</span><span class="sxs-lookup"><span data-stu-id="5ea70-103">XAudio2 Debugging Facilities</span></span>

<span data-ttu-id="5ea70-104">La versione di debug del motore XAudio2 convalida i parametri e fornisce messaggi di avviso e di errore dettagliati.</span><span class="sxs-lookup"><span data-stu-id="5ea70-104">The debug version of the XAudio2 engine validates parameters, and provides detailed warning and error messages.</span></span>

## <a name="setting-the-debug-logging-level-at-run-time"></a><span data-ttu-id="5ea70-105">Impostazione del livello di registrazione del debug in fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="5ea70-105">Setting the Debug Logging Level at Run Time</span></span>

<span data-ttu-id="5ea70-106">È possibile impostare il livello di informazioni di debug visualizzate da XAudio2 in qualsiasi momento compilando una struttura di [**\_ \_ configurazione di debug XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) con i flag per il livello di registrazione desiderato, quindi passare la struttura al metodo [**IXAudio2:: SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="5ea70-106">You can set the level of debugging information shown by XAudio2 at any time by filling out an [**XAUDIO2\_DEBUG\_CONFIGURATION**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) structure with the flags for the desired logging level, and then pass the structure to the [**IXAudio2::SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) method.</span></span> <span data-ttu-id="5ea70-107">I valori passati al metodo **IXAudio2:: SetDebugConfiguration** eseguono sempre l'override dei valori predefiniti impostati nel registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="5ea70-107">Values passed to the **IXAudio2::SetDebugConfiguration** method always override any default values that were set in the Windows registry.</span></span>

## <a name="debug-support"></a><span data-ttu-id="5ea70-108">Supporto per il debug</span><span class="sxs-lookup"><span data-stu-id="5ea70-108">Debug Support</span></span>

<span data-ttu-id="5ea70-109">Le funzionalità di debug sono sempre disponibili per XAUDIO2 in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5ea70-109">The debugging facilities are always available for XAUDIO2 in Windows 8.</span></span>

<span data-ttu-id="5ea70-110">Per le versioni di DirectX SDK di XAUDIO2, è necessario usare il **\_ \_ motore di debug di XAUDIO2** quando si crea l'oggetto XAUDIO2 con [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) e il sistema deve disporre del runtime di DirectX SDK Developer installato per supportare il debug.</span><span class="sxs-lookup"><span data-stu-id="5ea70-110">For the DirectX SDK versions of XAUDIO2, you must use **XAUDIO2\_DEBUG\_ENGINE** when creating the XAUDIO2 object with [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) and the system must have the DirectX SDK Developer Runtime installed for debugging to be supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ea70-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ea70-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ea70-112">Funzionalità di debug</span><span class="sxs-lookup"><span data-stu-id="5ea70-112">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="5ea70-113">Guida di riferimento alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="5ea70-113">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
