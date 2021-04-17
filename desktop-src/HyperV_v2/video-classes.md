---
description: Tutte le macchine virtuali riflettono la presenza di un controller video S3 emulato e un controller video accelerato e sintetico.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Classi video
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485693"
---
# <a name="video-classes"></a><span data-ttu-id="b597d-103">Classi video</span><span class="sxs-lookup"><span data-stu-id="b597d-103">Video classes</span></span>

<span data-ttu-id="b597d-104">Tutte le macchine virtuali riflettono la presenza di un controller video S3 emulato e un controller video accelerato e sintetico.</span><span class="sxs-lookup"><span data-stu-id="b597d-104">All virtual machines reflect the presence of an emulated S3 video controller and an accelerated, synthetic video controller.</span></span>

<span data-ttu-id="b597d-105">A ogni controller di visualizzazione è associato un oggetto Head del video.</span><span class="sxs-lookup"><span data-stu-id="b597d-105">Each display controller has a video head object associated with it.</span></span> <span data-ttu-id="b597d-106">In una macchina virtuale può essere attivo un solo controller di visualizzazione in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="b597d-106">Only one display controller can be active in a virtual machine at any time.</span></span>

<span data-ttu-id="b597d-107">È presente una connessione terminal per ogni sessione remota attiva connessa a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b597d-107">A terminal connection is present for every active remote session connected to a virtual machine.</span></span>

<span data-ttu-id="b597d-108">Di seguito sono riportate le classi WMI di virtualizzazione correlate ai video.</span><span class="sxs-lookup"><span data-stu-id="b597d-108">The following are virtualization WMI classes related to video.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b597d-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b597d-109">In this section</span></span>



| <span data-ttu-id="b597d-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="b597d-110">Topic</span></span>                                                                                  | <span data-ttu-id="b597d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b597d-111">Description</span></span>                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b597d-112">**\_S3DisplayController MSVM**</span><span class="sxs-lookup"><span data-stu-id="b597d-112">**Msvm\_S3DisplayController**</span></span>](msvm-s3displaycontroller.md)<br/>               | <span data-ttu-id="b597d-113">Rappresenta lo stato del controller S3 emulato presente in ogni configurazione di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b597d-113">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span><br/>       |
| [<span data-ttu-id="b597d-114">**\_SyntheticDisplayController MSVM**</span><span class="sxs-lookup"><span data-stu-id="b597d-114">**Msvm\_SyntheticDisplayController**</span></span>](msvm-syntheticdisplaycontroller.md)<br/> | <span data-ttu-id="b597d-115">Rappresenta lo stato del controller di visualizzazione sintetico presente in ogni configurazione di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b597d-115">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span><br/> |
| [<span data-ttu-id="b597d-116">**\_SystemTerminalConnection MSVM**</span><span class="sxs-lookup"><span data-stu-id="b597d-116">**Msvm\_SystemTerminalConnection**</span></span>](msvm-systemterminalconnection.md)<br/>     | <span data-ttu-id="b597d-117">Associa una macchina virtuale a una connessione terminale.</span><span class="sxs-lookup"><span data-stu-id="b597d-117">Associates a virtual machine with a terminal connection.</span></span><br/>                                                        |
| [<span data-ttu-id="b597d-118">**\_TerminalConnection MSVM**</span><span class="sxs-lookup"><span data-stu-id="b597d-118">**Msvm\_TerminalConnection**</span></span>](msvm-terminalconnection.md)<br/>                 | <span data-ttu-id="b597d-119">Indica lo stato di una sessione remota attiva che interagisce con una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b597d-119">Indicates the state of an active remote session interacting with a virtual machine.</span></span><br/>                             |
| [<span data-ttu-id="b597d-120">**\_VideoHead MSVM**</span><span class="sxs-lookup"><span data-stu-id="b597d-120">**Msvm\_VideoHead**</span></span>](msvm-videohead.md)<br/>                                   | <span data-ttu-id="b597d-121">Descrive la superficie di disegno principale in un controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b597d-121">Describes the primary drawing surface on a display controller.</span></span><br/>                                                  |
| [<span data-ttu-id="b597d-122">**\_VideoHeadOnController MSVM**</span><span class="sxs-lookup"><span data-stu-id="b597d-122">**Msvm\_VideoHeadOnController**</span></span>](msvm-videoheadoncontroller.md)<br/>           | <span data-ttu-id="b597d-123">Associa una testa video al controller video che lo include.</span><span class="sxs-lookup"><span data-stu-id="b597d-123">Associates a video head with the video controller that includes it.</span></span><br/>                                             |



 

 

 




