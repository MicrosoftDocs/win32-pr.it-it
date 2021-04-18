---
description: Questa sezione elenca un problema che può verificarsi quando si usano le finestre del dispositivo nelle applicazioni Direct3D.
ms.assetid: 7cfd2ad6-fb85-4303-9fa4-6fe7d16d9951
title: Uso di Windows Device (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56352ef0ec66def620a0ae0995d92d8b421722e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303794"
---
# <a name="working-with-device-windows-direct3d-9"></a><span data-ttu-id="2d9e6-103">Uso di Windows Device (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2d9e6-103">Working with Device Windows (Direct3D 9)</span></span>

<span data-ttu-id="2d9e6-104">Questa sezione elenca un problema che può verificarsi quando si usano le finestre del dispositivo nelle applicazioni Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-104">This section lists an issue that you might encounter when working with device windows in Direct3D applications.</span></span>

-   <span data-ttu-id="2d9e6-105">Direct3D associa solo le finestre di stato attivo invece della finestra del dispositivo con la funzione di elaborazione dei messaggi Direct3D e elabora solo i messaggi della finestra di stato attivo.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-105">Direct3D only hooks up the focus windows instead of the device window with the Direct3D message processing function, and only processes the focus window messages.</span></span> <span data-ttu-id="2d9e6-106">Quindi, la finestra di attivazione deve essere l'elemento padre di qualsiasi finestra del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-106">So, the focus window should be the parent of any device window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d9e6-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d9e6-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d9e6-108">Suggerimenti per la programmazione</span><span class="sxs-lookup"><span data-stu-id="2d9e6-108">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



