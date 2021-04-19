---
title: Personalizzare l'anteprima di un'icona e una bitmap di anteprima in tempo reale
description: Mostra come personalizzare un'anteprima iconica e una bitmap di anteprima in tempo reale (denominata anche anteprima di anteprima).
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323874"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a><span data-ttu-id="6b563-103">Personalizzare l'anteprima di un'icona e una bitmap di anteprima in tempo reale</span><span class="sxs-lookup"><span data-stu-id="6b563-103">Customize an Iconic Thumbnail and a Live Preview Bitmap</span></span>

## <a name="description"></a><span data-ttu-id="6b563-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b563-104">Description</span></span>

<span data-ttu-id="6b563-105">È possibile personalizzare un'anteprima iconica e una bitmap in *tempo reale* (o *Anteprima*) utilizzando le funzioni e i messaggi introdotti nelle api di Windows 7 Gestione finestre desktop (DWM).</span><span class="sxs-lookup"><span data-stu-id="6b563-105">You can customize an iconic thumbnail and a *live preview* (or *Peek preview*) bitmap by using functions and messages that are introduced in the Windows 7 Desktop Window Manager (DWM) APIs.</span></span>

<span data-ttu-id="6b563-106">In particolare, è possibile usare la funzione [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) e il messaggio [**WM \_ SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) per personalizzare un'anteprima iconica.</span><span class="sxs-lookup"><span data-stu-id="6b563-106">Specifically, you use the [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function and the [**WM\_SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) message to customize an iconic thumbnail.</span></span> <span data-ttu-id="6b563-107">È anche possibile usare la funzione [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) e il messaggio [**WM \_ SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) per impostare una bitmap di anteprima dinamica iconica.</span><span class="sxs-lookup"><span data-stu-id="6b563-107">You can also use the [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function and the [**WM\_SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) message to set an iconic live preview bitmap.</span></span>

<span data-ttu-id="6b563-108">Per un'applicazione di esempio che usa la funzione **DwmSetIconicThumbnail** , vedere [esempio di TabThumbnails](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span><span class="sxs-lookup"><span data-stu-id="6b563-108">For a sample application that uses the **DwmSetIconicThumbnail** function, see [TabThumbnails sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span></span>

<span data-ttu-id="6b563-109">Nella figura seguente viene illustrata un'anteprima predefinita trasformata in un'anteprima personalizzata.</span><span class="sxs-lookup"><span data-stu-id="6b563-109">The following illustration shows a default thumbnail transformed into a customized thumbnail.</span></span>

![illustrazione di un'immagine di anteprima originale e di un'immagine di anteprima modificata con una bitmap personalizzata](images/customthumbnail.jpg)

## <a name="requirements"></a><span data-ttu-id="6b563-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b563-111">Requirements</span></span>

| <span data-ttu-id="6b563-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b563-112">Requirement</span></span> | <span data-ttu-id="6b563-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6b563-113">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b563-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b563-114">Minimum supported client</span></span> | <span data-ttu-id="6b563-115">Windows 7 o Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b563-115">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>                          |
| <span data-ttu-id="6b563-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b563-116">Minimum supported server</span></span> | <span data-ttu-id="6b563-117">Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b563-117">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span> |
| <span data-ttu-id="6b563-118">Windows SDK minimo</span><span class="sxs-lookup"><span data-stu-id="6b563-118">Minimum Windows SDK</span></span>      | [<span data-ttu-id="6b563-119">Windows Software Development Kit (SDK) per Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b563-119">Windows Software Development Kit (SDK) for Windows 7</span></span>](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a><span data-ttu-id="6b563-120">Compilazione dell'esempio TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="6b563-120">Building the TabThumbnails sample</span></span>

<span data-ttu-id="6b563-121">**Per compilare l'esempio utilizzando Microsoft Visual Studio (metodo preferito)**</span><span class="sxs-lookup"><span data-stu-id="6b563-121">**To build the sample by using Microsoft Visual Studio (preferred method)**</span></span>

1.  <span data-ttu-id="6b563-122">Aprire Esplora risorse e passare alla cartella in cui si trova il file TabThumbnails. sln.</span><span class="sxs-lookup"><span data-stu-id="6b563-122">Open Windows Explorer and browse to the folder where the TabThumbnails.sln file is located.</span></span>
2.  <span data-ttu-id="6b563-123">Fare doppio clic sul file di soluzione (con estensione sln) per aprire il file in Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6b563-123">Double-click the solution file (.sln) to open the file in Microsoft Visual Studio.</span></span>
3.  <span data-ttu-id="6b563-124">Nel menu **Compila** scegliere **Compila soluzione**.</span><span class="sxs-lookup"><span data-stu-id="6b563-124">On the **Build** menu, click **Build Solution**.</span></span> <span data-ttu-id="6b563-125">L'applicazione viene compilata nella \\ directory di debug o di \\ versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6b563-125">The application is built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="6b563-126">**Per compilare l'esempio utilizzando il prompt dei comandi**</span><span class="sxs-lookup"><span data-stu-id="6b563-126">**To build the sample by using the command prompt**</span></span>

1.  <span data-ttu-id="6b563-127">Aprire una finestra del prompt dei comandi e passare alla directory di esempio.</span><span class="sxs-lookup"><span data-stu-id="6b563-127">Open a Command Prompt window and browse to the sample directory.</span></span>
2.  <span data-ttu-id="6b563-128">Immettere `msbuild TabThumbnails.sln`.</span><span class="sxs-lookup"><span data-stu-id="6b563-128">Enter `msbuild TabThumbnails.sln`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b563-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b563-129">Related topics</span></span>

[<span data-ttu-id="6b563-130">Gestione finestre desktop</span><span class="sxs-lookup"><span data-stu-id="6b563-130">Desktop Window Manager</span></span>](dwm-overview.md)

[<span data-ttu-id="6b563-131">Sviluppo per Windows</span><span class="sxs-lookup"><span data-stu-id="6b563-131">Windows Development</span></span>](/windows/desktop/win32-and-com-development)
