---
description: Comandi di OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandi di OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309067"
---
# <a name="opm-commands"></a><span data-ttu-id="939fa-103">Comandi di OPM</span><span class="sxs-lookup"><span data-stu-id="939fa-103">OPM Commands</span></span>

<span data-ttu-id="939fa-104">Questa sezione elenca i comandi disponibili per l' [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="939fa-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="939fa-105">Per inviare un comando OPM, chiamare [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="939fa-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="939fa-106">Per ogni comando vengono elencate le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="939fa-106">For each command, the following information is listed.</span></span>



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="939fa-107">GUID comando</span><span class="sxs-lookup"><span data-stu-id="939fa-107">Command GUID</span></span> | <span data-ttu-id="939fa-108">Identifica il comando.</span><span class="sxs-lookup"><span data-stu-id="939fa-108">Identifies the command.</span></span> <span data-ttu-id="939fa-109">Impostare il membro **guidSetting** della struttura di [**configurazione dei \_ \_ parametri di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) uguale a questo valore.</span><span class="sxs-lookup"><span data-stu-id="939fa-109">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="939fa-110">Dati di input</span><span class="sxs-lookup"><span data-stu-id="939fa-110">Input data</span></span>   | <span data-ttu-id="939fa-111">Specifica come interpretare la matrice **abParameters** nella struttura [**dei \_ \_ parametri di configurazione di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .</span><span class="sxs-lookup"><span data-stu-id="939fa-111">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="939fa-112">Sono definiti i seguenti comandi:</span><span class="sxs-lookup"><span data-stu-id="939fa-112">The following commands are defined:</span></span>



| <span data-ttu-id="939fa-113">Comando</span><span class="sxs-lookup"><span data-stu-id="939fa-113">Command</span></span>                                                                                                       | <span data-ttu-id="939fa-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="939fa-114">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="939fa-115">**il \_ set \_ di OPM ACP \_ e la \_ \_ segnalazione CGMSA**</span><span class="sxs-lookup"><span data-stu-id="939fa-115">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="939fa-116">Specifica le informazioni sul segnale video, oltre al livello di protezione.</span><span class="sxs-lookup"><span data-stu-id="939fa-116">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="939fa-117">**\_set OPM \_ HDCP \_ SRM**</span><span class="sxs-lookup"><span data-stu-id="939fa-117">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="939fa-118">Aggiorna il messaggio di rinnovabilità del sistema (SRM) per High-Bandwidth Digital protezione del contenuto (HDCP).</span><span class="sxs-lookup"><span data-stu-id="939fa-118">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="939fa-119">**\_livello di \_ protezione \_ set OPM**</span><span class="sxs-lookup"><span data-stu-id="939fa-119">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="939fa-120">Imposta il livello di protezione per un meccanismo di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="939fa-120">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="939fa-121">**\_impostazione del \_ \_ livello di protezione di OPM \_ \_ in base al \_ \_ DVD CSS**</span><span class="sxs-lookup"><span data-stu-id="939fa-121">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="939fa-122">Imposta il livello di protezione HDCP per la riproduzione DVD, seguendo le regole CSS (Content Scramble System) del DVD.</span><span class="sxs-lookup"><span data-stu-id="939fa-122">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="939fa-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="939fa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="939fa-124">Guida di riferimento alla programmazione di OPM</span><span class="sxs-lookup"><span data-stu-id="939fa-124">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="939fa-125">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="939fa-125">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



