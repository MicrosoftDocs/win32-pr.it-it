---
title: Limiti di caricamento
description: Per limitare le dimensioni dei caricamenti, impostare la proprietà dell'estensione IIS BITSMaximumUploadSize.
ms.assetid: 01ad2f32-18be-43a5-a07f-e6f28f7a471b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647aeefe82cf9c3ab035bc3e233c4157f471110b
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104472267"
---
# <a name="upload-limits"></a><span data-ttu-id="0b3f1-103">Limiti di caricamento</span><span class="sxs-lookup"><span data-stu-id="0b3f1-103">Upload Limits</span></span>

<span data-ttu-id="0b3f1-104">Per limitare le dimensioni dei caricamenti, impostare la proprietà dell'estensione IIS [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="0b3f1-104">To limit the size of uploads, set the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property.</span></span> <span data-ttu-id="0b3f1-105">In IIS 7 potrebbe anche essere necessario modificare l'attributo **MaxAllowedContentLength** .</span><span class="sxs-lookup"><span data-stu-id="0b3f1-105">In IIS 7, you may also have to modify the **maxAllowedContentLength** attribute.</span></span> <span data-ttu-id="0b3f1-106">Per impostazione predefinita, il limite di caricamento di IIS 7 è pari a 30 milioni byte.</span><span class="sxs-lookup"><span data-stu-id="0b3f1-106">By default, the IIS 7 upload limit is 30 million bytes.</span></span> <span data-ttu-id="0b3f1-107">Per informazioni dettagliate e informazioni sulla modifica del valore predefinito di IIS, vedere [KB942074](https://support.microsoft.com//kb/942074).</span><span class="sxs-lookup"><span data-stu-id="0b3f1-107">For details and information on changing the IIS default, see [KB942074](https://support.microsoft.com//kb/942074).</span></span>

 

 




