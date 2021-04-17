---
description: Controlli di riproduzione in TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Controlli di riproduzione in TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566412"
---
# <a name="playback-controls-in-topoedit"></a><span data-ttu-id="becea-103">Controlli di riproduzione in TopoEdit</span><span class="sxs-lookup"><span data-stu-id="becea-103">Playback Controls in TopoEdit</span></span>

<span data-ttu-id="becea-104">Dopo la risoluzione, una topologia viene accodata nella sessione multimediale per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="becea-104">After a topology is resolved, it is queued on the Media Session for playback.</span></span> <span data-ttu-id="becea-105">TopoEdit fornisce il controllo di trasporto per la modifica dello stato della topologia nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="becea-105">TopoEdit provides transport control for changing the state of topology on the Media Session.</span></span>

<span data-ttu-id="becea-106">La tabella seguente illustra il comando menu/barra degli strumenti e il metodo Media Foundation equivalente per ogni operazione.</span><span class="sxs-lookup"><span data-stu-id="becea-106">The following table shows the menu/toolbar command and the equivalent Media Foundation method for each operation.</span></span>



| <span data-ttu-id="becea-107">Comando menu/barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="becea-107">Menu/Toolbar Command</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="becea-108">Metodo Media Foundation</span><span class="sxs-lookup"><span data-stu-id="becea-108">Media Foundation Method</span></span>                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="becea-109">Scegliere **Riproduci** dal menu **controlli** . \[ nuova riga \] o \[ nuova riga \] fare clic sul pulsante **Riproduci** sulla barra degli strumenti (mostrata nella figura seguente). \[ \] ![ schermata di nuova riga del pulsante Riproduci](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span><span class="sxs-lookup"><span data-stu-id="becea-109">On the **Controls** menu, click **Play**.\[newline\] -or-\[newline\] click the **play** button on the toolbar (shown in the following image).\[newline\]![screen shot of the play button](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span></span>    | [<span data-ttu-id="becea-110">**IMFMediaSession:: Start**</span><span class="sxs-lookup"><span data-stu-id="becea-110">**IMFMediaSession::Start**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| <span data-ttu-id="becea-111">Scegliere **Interrompi** dal menu **controlli** . \[ nuova riga \] o \[ nuova riga \] fare clic sul pulsante **Arresta** sulla barra degli strumenti (mostrata nella figura seguente). \[ Screenshot di nuova riga \] ![ del pulsante Interrompi](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span><span class="sxs-lookup"><span data-stu-id="becea-111">On the **Controls** menu, click **Stop**.\[newline\] -or-\[newline\] click the **stop** button on the toolbar (shown in the following image).\[newline\]![screen shot of the stop button](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span></span>    | [<span data-ttu-id="becea-112">**IMFMediaSession:: Stop**</span><span class="sxs-lookup"><span data-stu-id="becea-112">**IMFMediaSession::Stop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| <span data-ttu-id="becea-113">Scegliere **Sospendi** dal menu **controlli** . \[ nuova riga \] o \[ nuova riga \] fare clic sul pulsante **Sospendi** sulla barra degli strumenti (mostrata nella figura seguente). \[ Screenshot di nuova riga \] ![ del pulsante Sospendi](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span><span class="sxs-lookup"><span data-stu-id="becea-113">On the **Controls** menu, click **Pause**.\[newline\] -or-\[newline\] click the **pause** button on the toolbar (shown in the following image).\[newline\]![screen shot of the pause button](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span></span> | [<span data-ttu-id="becea-114">**IMFMediaSession::P ause**</span><span class="sxs-lookup"><span data-stu-id="becea-114">**IMFMediaSession::Pause**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

<span data-ttu-id="becea-115">Per informazioni sul controllo della riproduzione a livello di programmazione tramite le API di Media Foundation, vedere [How to Control Presentation States](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="becea-115">For information about controlling the playback programmatically by using Media Foundation APIs, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="seeking"></a><span data-ttu-id="becea-116">La ricerca</span><span class="sxs-lookup"><span data-stu-id="becea-116">Seeking</span></span>

<span data-ttu-id="becea-117">Se la topologia è ricercabile, è possibile cercare usando la barra di ricerca (mostrata nella figura seguente) per specificare una posizione nella sequenza temporale della topologia per iniziare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="becea-117">If the topology is seekable, you can seek by using the seek bar (shown in the following image) to specify a place in the topology's timeline to begin playback.</span></span>

![screenshot della barra di ricerca](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> <span data-ttu-id="becea-119">Se l'origine del supporto è ricercabile, il comando Stop Cerca anche la topologia all'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="becea-119">If the media source is seekable, the Stop command also seeks the topology back to the start of the stream.</span></span>

 

## <a name="changing-the-playback-rate"></a><span data-ttu-id="becea-120">Modifica della velocità di riproduzione</span><span class="sxs-lookup"><span data-stu-id="becea-120">Changing the Playback Rate</span></span>

<span data-ttu-id="becea-121">Se l'origine multimediale sottostante per la topologia supporta più frequenze di riproduzione, è possibile usare la barra della velocità per modificare la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="becea-121">If the underlying media source for the topology supports multiple playback rates, you can use the rate bar to change the playback rate.</span></span> <span data-ttu-id="becea-122">Per eseguire rapidamente il provisioning di una topologia nella sessione multimediale, aumentare la velocità trascinando il dispositivo di scorrimento a destra, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="becea-122">To fast-forward a topology on the Media Session, increase the rate by dragging the slider to the right, as shown in the following image.</span></span>

![screenshot della barra della velocità](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> <span data-ttu-id="becea-124">In questa versione, TopoEdit supporta solo frequenze positive.</span><span class="sxs-lookup"><span data-stu-id="becea-124">In this version, TopoEdit only supports positive rates.</span></span> <span data-ttu-id="becea-125">La riproduzione inversa non è supportata.</span><span class="sxs-lookup"><span data-stu-id="becea-125">Reverse playback is not supported.</span></span>

 

<span data-ttu-id="becea-126">Per informazioni sulla modifica della velocità di riproduzione a livello di codice usando le API di Media Foundation, vedere [informazioni sul controllo della frequenza](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="becea-126">For information about changing the playback rate programmatically by using Media Foundation APIs, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="becea-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="becea-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="becea-128">Menu TopoEdit</span><span class="sxs-lookup"><span data-stu-id="becea-128">TopoEdit Menus</span></span>](topoedit-menus.md)
</dt> <dt>

[<span data-ttu-id="becea-129">Barra degli strumenti TopoEdit</span><span class="sxs-lookup"><span data-stu-id="becea-129">TopoEdit Toolbar</span></span>](topoedit-toolbar.md)
</dt> <dt>

[<span data-ttu-id="becea-130">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="becea-130">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



