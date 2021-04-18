---
description: Windows Imaging Component (WIC) è una piattaforma estensibile per la creazione di immagini digitali nei sistemi operativi Windows Vista e Windows 7.
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: Introduzione (come scrivere un codec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776bf9f2c0cb5df8b45ce04d55f20d40d05a12a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312974"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="1362a-103">Introduzione (come scrivere un codec WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="1362a-103">Introduction (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="1362a-104">Windows Imaging Component (WIC) è una piattaforma estensibile per la creazione di immagini digitali nei sistemi operativi Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1362a-104">The Windows Imaging Component (WIC) is an extensible platform for digital imaging on the Windows Vista and Windows 7 operating systems.</span></span> <span data-ttu-id="1362a-105">WIC è disponibile anche in Windows XP e Windows Server 2003, come parte di Microsoft .NET Framework 3,0 o come componente separato che può essere ridistribuito.</span><span class="sxs-lookup"><span data-stu-id="1362a-105">WIC is also available on Windows XP and Windows Server 2003, either as part of Microsoft .NET Framework 3.0 or as a separate component that you can redistribute.</span></span> <span data-ttu-id="1362a-106">Qualsiasi applicazione che utilizza WIC può accedere, visualizzare, elaborare e stampare immagini in qualsiasi formato di immagine che fornisce un codec abilitato per WIC, utilizzando un unico set di interfacce coerenti che eliminano la necessità di una conoscenza approfondita di formati specifici.</span><span class="sxs-lookup"><span data-stu-id="1362a-106">Any application using the WIC can access, display, process, and print images in any image format that provides a WIC-enabled codec, using a single set of consistent interfaces that eliminate the need for specialized knowledge of specific formats.</span></span>

<span data-ttu-id="1362a-107">Esplora risorse di Windows Vista, raccolta foto di Windows Vista, raccolta foto in diretta e Visualizzatore foto di Windows 7 sono basati su WIC.</span><span class="sxs-lookup"><span data-stu-id="1362a-107">The Windows Vista Explorer, Windows Vista Photo Gallery, Live Photo Gallery, and Windows 7 Photo Viewer are built on WIC.</span></span> <span data-ttu-id="1362a-108">Dopo l'installazione di un codec abilitato per WIC in un sistema Windows Vista o Windows 7, il sistema operativo fornisce lo stesso livello di supporto per il formato di immagine associato per i formati di immagine standard forniti con la piattaforma.</span><span class="sxs-lookup"><span data-stu-id="1362a-108">After a WIC-enabled codec is installed on a Windows Vista or Windows 7 system, the operating system provides the same level of support for the associated image format as for the standard image formats that ship with the platform.</span></span> <span data-ttu-id="1362a-109">Poiché si scrive il codec per il proprio formato di immagine, è possibile garantire una qualità coerente ovunque venga usato il formato di immagine e ottenere i vantaggi del supporto completo della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="1362a-109">Because you write the codec for your own image format, you can ensure consistent quality wherever your image format is used, and you get the benefits of full platform support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1362a-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1362a-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1362a-111">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1362a-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1362a-112">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="1362a-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="1362a-113">Funzionamento del componente Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="1362a-113">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

<span data-ttu-id="1362a-114">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="1362a-114">How to Write a WIC-Enabled CODEC</span></span>
</dt> <dt>

[<span data-ttu-id="1362a-115">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="1362a-115">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



