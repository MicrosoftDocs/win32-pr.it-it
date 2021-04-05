---
title: Dimensioni dell'indice
description: Dimensioni dell'indice
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711584"
---
# <a name="index-size"></a><span data-ttu-id="0bf5e-107">Dimensioni dell'indice</span><span class="sxs-lookup"><span data-stu-id="0bf5e-107">Index Size</span></span>

<span data-ttu-id="0bf5e-108">Ogni file AVI usa un indice di una dimensione specificata per individuare i blocchi di dati audio e video all'interno del file.</span><span class="sxs-lookup"><span data-stu-id="0bf5e-108">Each AVI file uses an index of a specified size to locate video and audio data chunks within the file.</span></span> <span data-ttu-id="0bf5e-109">Una voce nell'indice individua un fotogramma video o un buffer audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="0bf5e-109">An entry in the index locates one video frame or waveform-audio buffer.</span></span> <span data-ttu-id="0bf5e-110">Di conseguenza, il valore della dimensione dell'indice imposta indirettamente il limite superiore per il numero di frame che possono essere acquisiti in un file.</span><span class="sxs-lookup"><span data-stu-id="0bf5e-110">Consequently, the value of the index size indirectly sets the upper limit on the number of frames that can be captured in a file.</span></span>

<span data-ttu-id="0bf5e-111">È possibile recuperare le dimensioni correnti degli indici usando il messaggio di [**installazione della \_ sequenza WM Cap \_ get \_ \_**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="0bf5e-111">You can retrieve the current index size by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="0bf5e-112">La dimensione dell'indice corrente viene archiviata nel membro **dwIndexSize** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="0bf5e-112">The current index size is stored in the **dwIndexSize** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="0bf5e-113">È possibile specificare una nuova dimensione di indice come valore di **dwIndexSize** , quindi inviare la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_ di set di WM Cap**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="0bf5e-113">You can specify a new index size as the value of **dwIndexSize** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="0bf5e-114">La dimensione dell'indice predefinita è 34.952 voci (che consentono 32K frame e un numero proporzionale di buffer audio).</span><span class="sxs-lookup"><span data-stu-id="0bf5e-114">The default index size is 34,952 entries (allowing 32K frames and a proportional number of audio buffers).</span></span>

 

 




