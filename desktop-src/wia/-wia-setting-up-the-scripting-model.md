---
description: Per utilizzare il modello di scripting Windows Image Acquisition (WIA), è necessario che il file Wiascr.dll installato e registrato nel computer.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Configurazione dell'ambiente di sviluppo del modello di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226141"
---
# <a name="setting-up-the-scripting-model-development-environment"></a><span data-ttu-id="34c22-103">Configurazione dell'ambiente di sviluppo del modello di scripting</span><span class="sxs-lookup"><span data-stu-id="34c22-103">Setting up the Scripting Model Development Environment</span></span>

<span data-ttu-id="34c22-104">Per utilizzare il modello di scripting Windows Image Acquisition (WIA), è necessario che il file Wiascr.dll installato e registrato nel computer.</span><span class="sxs-lookup"><span data-stu-id="34c22-104">To use the Windows Image Acquisition (WIA) scripting model, you must have the file Wiascr.dll installed and registered on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="34c22-105">Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="34c22-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="34c22-106">Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="34c22-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="34c22-107">Copiare questo file da WIA SDK nella directory *% windir%*/system32 (ad esempio, c: \\ Windows \\ System32).</span><span class="sxs-lookup"><span data-stu-id="34c22-107">Copy this file from the WIA SDK into the *%windir%*/System32 (for example, c:\\windows\\System32) directory.</span></span> <span data-ttu-id="34c22-108">Nella riga di comando passare a questa directory e digitare **regsvr32 Wiascr.dll**.</span><span class="sxs-lookup"><span data-stu-id="34c22-108">At the command line, navigate to this directory, and type **regsvr32 Wiascr.dll**.</span></span>

<span data-ttu-id="34c22-109">Questa operazione immette le informazioni necessarie nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="34c22-109">This enters the necessary information in the system registry.</span></span>

<span data-ttu-id="34c22-110">A questo punto è possibile usare il modello di scripting WIA.</span><span class="sxs-lookup"><span data-stu-id="34c22-110">You are now ready to use the WIA scripting model.</span></span>

 

 
