---
title: Rilevamento di Windows Media Player da un'applicazione
description: Rilevamento di Windows Media Player da un'applicazione
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player, rilevamento da applicazioni
- rilevamento Media Player Windows dalle applicazioni
- Registro di sistema, rilevamento Media Player Windows dalle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298801"
---
# <a name="detecting-windows-media-player-from-an-application"></a><span data-ttu-id="bf0de-106">Rilevamento di Windows Media Player da un'applicazione</span><span class="sxs-lookup"><span data-stu-id="bf0de-106">Detecting Windows Media Player from an Application</span></span>

<span data-ttu-id="bf0de-107">È possibile determinare la versione di Windows Media Player installata controllando la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="bf0de-107">You can determine what version of Windows Media Player is installed by checking the following registry key:</span></span>

<span data-ttu-id="bf0de-108">**\_Componenti di \_ installazione \\ di \\ Microsoft \\ Active Setup Software per \\ computer locale HKEY**</span><span class="sxs-lookup"><span data-stu-id="bf0de-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Active Setup\\Installed Components**</span></span>

<span data-ttu-id="bf0de-109">Per Windows Media Player 6,4, vedere la chiave **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.</span><span class="sxs-lookup"><span data-stu-id="bf0de-109">For Windows Media Player 6.4, look at key **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.</span></span>

<span data-ttu-id="bf0de-110">Per Windows Media Player 7 o versione successiva, vedere la chiave **{6BF52A52-394A-11D3-B153-00C04F79FAA6}**.</span><span class="sxs-lookup"><span data-stu-id="bf0de-110">For Windows Media Player 7 or later, look at key **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**.</span></span>

<span data-ttu-id="bf0de-111">In una di queste chiavi, se è stato **installato**</span><span class="sxs-lookup"><span data-stu-id="bf0de-111">Under either of these keys, if the **IsInstalled**</span></span><dl> <dt>

<span data-ttu-id="bf0de-112">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bf0de-112">Data type</span></span>
</dt> <dd><span data-ttu-id="bf0de-113">DWORD</span><span class="sxs-lookup"><span data-stu-id="bf0de-113">DWORD</span></span></dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

<span data-ttu-id="bf0de-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bf0de-114">Data type</span></span>
</dt> <dd><span data-ttu-id="bf0de-115">string</span><span class="sxs-lookup"><span data-stu-id="bf0de-115">string</span></span></dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a><span data-ttu-id="bf0de-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf0de-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf0de-117">**Ridistribuzione del software Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="bf0de-117">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




