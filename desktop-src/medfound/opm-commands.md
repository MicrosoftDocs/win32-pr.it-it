---
description: Comandi OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandi OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119146"
---
# <a name="opm-commands"></a><span data-ttu-id="1d03a-103">Comandi OPM</span><span class="sxs-lookup"><span data-stu-id="1d03a-103">OPM Commands</span></span>

<span data-ttu-id="1d03a-104">Questa sezione elenca i comandi disponibili per [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="1d03a-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="1d03a-105">Per inviare un comando OPM, chiamare [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="1d03a-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="1d03a-106">Per ogni comando sono elencate le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d03a-106">For each command, the following information is listed.</span></span>



| <span data-ttu-id="1d03a-107">Valore</span><span class="sxs-lookup"><span data-stu-id="1d03a-107">Value</span></span>             | <span data-ttu-id="1d03a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d03a-108">Description</span></span>                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d03a-109">GUID del comando</span><span class="sxs-lookup"><span data-stu-id="1d03a-109">Command GUID</span></span> | <span data-ttu-id="1d03a-110">Identifica il comando.</span><span class="sxs-lookup"><span data-stu-id="1d03a-110">Identifies the command.</span></span> <span data-ttu-id="1d03a-111">Impostare il **membro guidSetting** della struttura [**OPM \_ CONFIGURE \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) su questo valore.</span><span class="sxs-lookup"><span data-stu-id="1d03a-111">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="1d03a-112">Dati di input</span><span class="sxs-lookup"><span data-stu-id="1d03a-112">Input data</span></span>   | <span data-ttu-id="1d03a-113">Specifica come interpretare la matrice **abParameters** nella [**struttura OPM \_ CONFIGURE \_ PARAMETERS.**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)</span><span class="sxs-lookup"><span data-stu-id="1d03a-113">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="1d03a-114">Sono definiti i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d03a-114">The following commands are defined:</span></span>



| <span data-ttu-id="1d03a-115">Comando</span><span class="sxs-lookup"><span data-stu-id="1d03a-115">Command</span></span>                                                                                                       | <span data-ttu-id="1d03a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d03a-116">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d03a-117">**OPM \_ SET \_ ACP \_ AND \_ CGMSA \_ SIGNALING**</span><span class="sxs-lookup"><span data-stu-id="1d03a-117">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="1d03a-118">Specifica informazioni sul segnale video, diverse dal livello di protezione.</span><span class="sxs-lookup"><span data-stu-id="1d03a-118">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="1d03a-119">**OPM \_ SET \_ HDCP \_ SRM**</span><span class="sxs-lookup"><span data-stu-id="1d03a-119">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="1d03a-120">Aggiorna il messaggio di rinnovo del sistema (SRM) per High-Bandwidth Digital protezione del contenuto (HDCP).</span><span class="sxs-lookup"><span data-stu-id="1d03a-120">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="1d03a-121">**OPM \_ SET \_ PROTECTION \_ LEVEL**</span><span class="sxs-lookup"><span data-stu-id="1d03a-121">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="1d03a-122">Imposta il livello di protezione per un meccanismo di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="1d03a-122">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="1d03a-123">**OPM \_ IMPOSTA IL LIVELLO DI PROTEZIONE IN BASE AL DVD \_ \_ \_ \_ \_ \_ CSS**</span><span class="sxs-lookup"><span data-stu-id="1d03a-123">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="1d03a-124">Imposta il livello di protezione HDCP per la riproduzione di DVD, seguendo le regole CSS (Dvd Content Scramble System).</span><span class="sxs-lookup"><span data-stu-id="1d03a-124">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1d03a-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d03a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d03a-126">Informazioni di riferimento sulla programmazione OPM</span><span class="sxs-lookup"><span data-stu-id="1d03a-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="1d03a-127">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="1d03a-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



