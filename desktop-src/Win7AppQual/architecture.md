---
description: Internet Explorer a regime di controllo libero (LCIE) migliora l'affidabilità del browser separando i componenti e allentando l'interdipendenza.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Architettura (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760082"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="52fbd-103">Architettura (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="52fbd-103">Architecture (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="52fbd-104">*Internet Explorer* a regime di controllo libero (LCIE) migliora l'affidabilità del browser separando i componenti e allentando l'interdipendenza.</span><span class="sxs-lookup"><span data-stu-id="52fbd-104">*Loosely-coupled Internet Explorer* (LCIE) improves the browser’s reliability by separating its components and loosening their interdependence.</span></span>

<span data-ttu-id="52fbd-105">In particolare, LCIE tenta di isolare il frame di Windows Internet Explorer e le relative schede in processi distinti.</span><span class="sxs-lookup"><span data-stu-id="52fbd-105">In particular, LCIE tries to isolate the Windows Internet Explorer frame and its tabs into separate processes.</span></span> <span data-ttu-id="52fbd-106">In Windows Internet Explorer 8, questo isolamento migliora le prestazioni e la scalabilità.</span><span class="sxs-lookup"><span data-stu-id="52fbd-106">In Windows Internet Explorer 8, this isolation improves performance and scalability.</span></span> <span data-ttu-id="52fbd-107">Questa modifica dell'architettura può influire sulla compatibilità di estensioni e componenti aggiuntivi, inclusi i controlli ActiveX, gli oggetti browser helper (considerarsi) e i componenti della barra degli strumenti dell'interfaccia utente compilati utilizzando tecniche di programmazione precedenti.</span><span class="sxs-lookup"><span data-stu-id="52fbd-107">This architectural change might affect the compatibility of extensions and add-ons, including ActiveX Controls, Browser Helper Objects (BHOs), and UI toolbar components that are built by using older programming techniques.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52fbd-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52fbd-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52fbd-109">Aggiornamenti della progettazione che incidono sulla compatibilità tra browser</span><span class="sxs-lookup"><span data-stu-id="52fbd-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



