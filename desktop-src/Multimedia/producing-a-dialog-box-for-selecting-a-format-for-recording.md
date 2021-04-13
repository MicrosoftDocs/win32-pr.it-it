---
title: Creazione di una finestra di dialogo per la selezione di un formato per la registrazione
description: Creazione di una finestra di dialogo per la selezione di un formato per la registrazione
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Gestione compressione audio (ACM), creazione di finestre di dialogo
- ACM (Gestione compressione audio), creazione di finestre di dialogo
- Esempi di ACM, creazione di finestre di dialogo
- creazione di finestre di dialogo
- acmFormatChoose (funzione)
- Gestione compressione audio (ACM), selezione del formato per la ricodifica
- ACM (Gestione compressione audio), selezione del formato per la ricodifica
- Esempi di ACM, selezione del formato per la ricodifica
- selezione del formato per la ricodifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7584d5f56904a6aa5241930041bf89c10373f6b1
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/27/2020
ms.locfileid: "104398691"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a><span data-ttu-id="88051-112">Creazione di una finestra di dialogo per la selezione di un formato per la registrazione</span><span class="sxs-lookup"><span data-stu-id="88051-112">Producing a Dialog Box for Selecting a Format for Recording</span></span>

<span data-ttu-id="88051-113">Un'applicazione può consentire all'utente di selezionare un formato per il quale un dispositivo audio Waveform installato fornisce il supporto nativo.</span><span class="sxs-lookup"><span data-stu-id="88051-113">An application can allow the user to select a format for which an installed waveform-audio device provides native support.</span></span> <span data-ttu-id="88051-114">Ad esempio, potrebbe essere necessario che un editor audio Waveform registri i nuovi dati dell'audio della forma d'onda senza usare un compressore o un decompressore ACM per fornire un livello di conversione.</span><span class="sxs-lookup"><span data-stu-id="88051-114">For example, you might want a waveform-audio editor to record new waveform-audio data without using an ACM compressor or decompressor to provide a translation layer.</span></span> <span data-ttu-id="88051-115">A tale scopo, usare la funzione [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , specificando i \_ \_ flag di input ACM FORMATENUMF hardware e ACM \_ FORMATENUMF \_ nel membro **fdwEnum** della struttura [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="88051-115">To do this, use the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specifying the ACM\_FORMATENUMF\_HARDWARE and ACM\_FORMATENUMF\_INPUT flags in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

 

 




