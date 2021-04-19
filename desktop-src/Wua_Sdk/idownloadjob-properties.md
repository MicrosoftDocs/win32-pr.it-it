---
description: L'interfaccia IDownloadJob definisce le proprietà seguenti.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Proprietà di IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307656"
---
# <a name="idownloadjob-properties"></a><span data-ttu-id="bcfd3-103">Proprietà di IDownloadJob</span><span class="sxs-lookup"><span data-stu-id="bcfd3-103">IDownloadJob Properties</span></span>

<span data-ttu-id="bcfd3-104">L'interfaccia [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following properties.</span></span>



| <span data-ttu-id="bcfd3-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bcfd3-105">Property</span></span>                                        | <span data-ttu-id="bcfd3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcfd3-106">Description</span></span>                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcfd3-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="bcfd3-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | <span data-ttu-id="bcfd3-108">Ottiene l'oggetto di stato specifico del chiamante passato al metodo [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .</span><span class="sxs-lookup"><span data-stu-id="bcfd3-108">Gets the caller-specific state object that is passed to the [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) method.</span></span>           |
| [<span data-ttu-id="bcfd3-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="bcfd3-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | <span data-ttu-id="bcfd3-110">Ottiene l'impostazione che indica se la chiamata a [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) è stata elaborata completamente.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-110">Gets the setting that indicates whether the call to [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) was processed completely.</span></span> |
| [<span data-ttu-id="bcfd3-111">**Aggiornamenti**</span><span class="sxs-lookup"><span data-stu-id="bcfd3-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | <span data-ttu-id="bcfd3-112">Ottiene un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati in un download.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-112">Gets an interface that contains a read-only collection of the updates that are specified in a download.</span></span>                                                  |



 

 

 



