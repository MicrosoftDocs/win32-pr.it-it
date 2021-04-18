---
description: La preparazione delle risorse per un'applicazione MUI supporta sia i modelli PE Win32 che quelli non Win32.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Preparazione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317144"
---
# <a name="preparing-resources"></a><span data-ttu-id="263fb-103">Preparazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="263fb-103">Preparing Resources</span></span>

<span data-ttu-id="263fb-104">La preparazione delle risorse per un'applicazione MUI supporta sia i modelli PE Win32 che quelli non Win32.</span><span class="sxs-lookup"><span data-stu-id="263fb-104">Resource preparation for a MUI application supports both Win32 PE and non-Win32 PE models.</span></span> <span data-ttu-id="263fb-105">Le risorse PE Win32 sono disponibili nei file basati su PE, ad esempio i file con estensione dll, exe o sys.</span><span class="sxs-lookup"><span data-stu-id="263fb-105">Win32 PE resources are provided in PE-based files, such as .dll, .exe, or .sys files.</span></span> <span data-ttu-id="263fb-106">Le risorse PE non Win32 sono fornite in un modulo personalizzato di propria scelta.</span><span class="sxs-lookup"><span data-stu-id="263fb-106">Non-Win32 PE resources are furnished in a customized module of your choosing.</span></span>

> [!Note]  
> <span data-ttu-id="263fb-107">Si consiglia vivamente di utilizzare le risorse PE Win32 per le applicazioni MUI Win32, in quanto queste risorse sono completamente supportate dalla tecnologia delle risorse MUI.</span><span class="sxs-lookup"><span data-stu-id="263fb-107">It is highly recommended for you to use Win32 PE resources for Win32 MUI applications, as these resources are completely supported by the MUI resource technology.</span></span> <span data-ttu-id="263fb-108">È possibile individuare i file di risorse PE non Win32 chiamando la funzione [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) come descritto in [individuazione di risorse PE non Win32](locating-non-win32-pe-resources.md), ma l'applicazione deve fornire le proprie funzionalità per individuare e caricare le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="263fb-108">Non-Win32 PE resource files can be located by calling the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function as described in [Locating Non-Win32 PE Resources](locating-non-win32-pe-resources.md), but the application must provide its own functionality to find and load the required resources.</span></span>

 

<span data-ttu-id="263fb-109">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="263fb-109">This section contains the following topics:</span></span>

-   [<span data-ttu-id="263fb-110">Creazione del file di risorse della lingua di base</span><span class="sxs-lookup"><span data-stu-id="263fb-110">Creating the Base Language Resource File</span></span>](creating-the-base-language-resource-file.md)
-   [<span data-ttu-id="263fb-111">Uso del reindirizzamento delle stringhe del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="263fb-111">Using Registry String Redirection</span></span>](using-registry-string-redirection.md)
-   [<span data-ttu-id="263fb-112">Preparazione di un file di configurazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="263fb-112">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)

 

 



