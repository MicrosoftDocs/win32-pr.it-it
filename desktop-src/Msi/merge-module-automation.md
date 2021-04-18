---
description: Mergemod.dll fornisce un oggetto COM che implementa le operazioni di merge e la generazione dell'immagine di origine per i moduli unione. L'oggetto Main implementa le interfacce per i programmi C/C++ e i client di automazione, inclusi Visual Basic e VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Automazione del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319013"
---
# <a name="merge-module-automation"></a><span data-ttu-id="96b4e-104">Automazione del modulo merge</span><span class="sxs-lookup"><span data-stu-id="96b4e-104">Merge Module Automation</span></span>

<span data-ttu-id="96b4e-105">Mergemod.dll fornisce un oggetto COM che implementa le operazioni di merge e la generazione dell'immagine di origine per i moduli unione.</span><span class="sxs-lookup"><span data-stu-id="96b4e-105">Mergemod.dll provides a COM object that implements merge operations and source image generation for merge modules.</span></span> <span data-ttu-id="96b4e-106">L'oggetto Main implementa le interfacce per i programmi C/C++ e i client di automazione, inclusi Visual Basic e VBScript.</span><span class="sxs-lookup"><span data-stu-id="96b4e-106">The main object implements interfaces for C/C++ programs and automation clients, including Visual Basic and VBScript.</span></span>

<span data-ttu-id="96b4e-107">Il metodo preferito per l'installazione di Mergemod.dll consiste nell'utilizzare l'Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="96b4e-107">The preferred method for installing Mergemod.dll is by using the Windows Installer.</span></span> <span data-ttu-id="96b4e-108">L'ID componente per il componente che contiene il Mergemod.dll interfaccia COM è {FD153241-37EC-11D2-8892-00A0C981B015}.</span><span class="sxs-lookup"><span data-stu-id="96b4e-108">The Component ID for the component containing the Mergemod.dll COM interface is {FD153241-37EC-11D2-8892-00A0C981B015}.</span></span> <span data-ttu-id="96b4e-109">Lo stesso file binario può essere usato in tutti i sistemi Windows e la dll eseguirà la registrazione automatica tramite regsvr32 nei sistemi meno recenti.</span><span class="sxs-lookup"><span data-stu-id="96b4e-109">The same binary can be used on all Windows systems and the dll will self-register through regsvr32 on older systems.</span></span>

<span data-ttu-id="96b4e-110">Si noti che Mergemod.dll richiede l'installazione del Msvcrt.dll nel sistema.</span><span class="sxs-lookup"><span data-stu-id="96b4e-110">Note that Mergemod.dll requires that the Msvcrt.dll be installed on the system.</span></span>

<span data-ttu-id="96b4e-111">Si noti che Mergemod.dll 2,0 è necessario per creare [moduli unione configurabili](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="96b4e-111">Note that Mergemod.dll 2.0 is required to create [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="96b4e-112">Mergemod.dll versione 2,0 fornisce funzionalità estese in fase di compilazione tramite l'interfaccia [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .</span><span class="sxs-lookup"><span data-stu-id="96b4e-112">Mergemod.dll version 2.0 provides extended functionality at build time through the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Interface.</span></span> <span data-ttu-id="96b4e-113">Questo CLSID supporta tutte le funzionalità esistenti dell'interfaccia [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) fornita dalla versione Mergemod.dll 1,0.</span><span class="sxs-lookup"><span data-stu-id="96b4e-113">This CLSID supports all the existing functionality of the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) Interface provided by Mergemod.dll version 1.0.</span></span> <span data-ttu-id="96b4e-114">L'interfaccia predefinita nell'oggetto [**merge**](merge-object.md) di Mergemod.dll 2,0 è l'interfaccia **IMsmMerge2** invece dell'interfaccia **IMsmMerge** .</span><span class="sxs-lookup"><span data-stu-id="96b4e-114">The default interface on the [**Merge**](merge-object.md) object of Mergemod.dll 2.0 is the **IMsmMerge2** interface instead of the **IMsmMerge** interface.</span></span>

[<span data-ttu-id="96b4e-115">Modello a oggetti per Mergemod.dll versione 1,0</span><span class="sxs-lookup"><span data-stu-id="96b4e-115">Object Model for Mergemod.dll Version 1.0</span></span>](object-model-for-mergemod-dll-version-1-0.md)

[<span data-ttu-id="96b4e-116">Modello a oggetti per Mergemod.dll versione 2,0</span><span class="sxs-lookup"><span data-stu-id="96b4e-116">Object Model for Mergemod.dll Version 2.0</span></span>](object-model-for-mergemod-dll-version-2-0.md)

 

 
