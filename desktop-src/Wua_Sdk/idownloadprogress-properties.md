---
description: L'interfaccia IDownloadProgress definisce le proprietà seguenti.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Proprietà di IDownloadProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966740"
---
# <a name="idownloadprogress-properties"></a><span data-ttu-id="16f6c-103">Proprietà di IDownloadProgress</span><span class="sxs-lookup"><span data-stu-id="16f6c-103">IDownloadProgress Properties</span></span>

<span data-ttu-id="16f6c-104">L'interfaccia [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="16f6c-104">The [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="16f6c-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16f6c-105">Property</span></span>                                                                               | <span data-ttu-id="16f6c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16f6c-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16f6c-107">**CurrentUpdateBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="16f6c-107">**CurrentUpdateBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | <span data-ttu-id="16f6c-108">Ottiene una stringa che specifica la quantità di dati trasferiti per il file o i file di contenuto dell'aggiornamento in fase di download, in byte.</span><span class="sxs-lookup"><span data-stu-id="16f6c-108">Gets a string that specifies how much data has been transferred for the content file or files of the update that is being downloaded, in bytes.</span></span>  |
| [<span data-ttu-id="16f6c-109">**CurrentUpdateBytesToDownload**</span><span class="sxs-lookup"><span data-stu-id="16f6c-109">**CurrentUpdateBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | <span data-ttu-id="16f6c-110">Ottiene una stringa che stima la quantità di dati che devono essere trasferiti per il file o i file di contenuto dell'aggiornamento in fase di download, in byte.</span><span class="sxs-lookup"><span data-stu-id="16f6c-110">Gets a string that estimates how much data should be transferred for the content file or files of the update that is being downloaded, in bytes.</span></span> |
| [<span data-ttu-id="16f6c-111">**CurrentUpdateDownloadPhase**</span><span class="sxs-lookup"><span data-stu-id="16f6c-111">**CurrentUpdateDownloadPhase**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | <span data-ttu-id="16f6c-112">Ottiene un valore di enumerazione [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) che specifica la fase del download attualmente in corso.</span><span class="sxs-lookup"><span data-stu-id="16f6c-112">Gets a [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) enumeration value that specifies the phase of the download that is currently in progress.</span></span>          |
| [<span data-ttu-id="16f6c-113">**CurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="16f6c-113">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | <span data-ttu-id="16f6c-114">Ottiene un valore di indice in base zero che specifica l'aggiornamento attualmente in fase di download quando sono stati selezionati più aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="16f6c-114">Gets a zero-based index value that specifies the update that is currently being downloaded when multiple updates have been selected.</span></span>             |
| [<span data-ttu-id="16f6c-115">**CurrentUpdatePercentComplete**</span><span class="sxs-lookup"><span data-stu-id="16f6c-115">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="16f6c-116">Ottiene una stima della percentuale dell'aggiornamento corrente che è stato scaricato.</span><span class="sxs-lookup"><span data-stu-id="16f6c-116">Gets an estimate of the percentage of the current update that has been downloaded.</span></span>                                                               |
| [<span data-ttu-id="16f6c-117">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="16f6c-117">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | <span data-ttu-id="16f6c-118">Ottiene una stima della percentuale di tutti gli aggiornamenti che sono stati scaricati.</span><span class="sxs-lookup"><span data-stu-id="16f6c-118">Gets an estimate of the percentage of all the updates that have been downloaded.</span></span>                                                                 |
| [<span data-ttu-id="16f6c-119">**TotalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="16f6c-119">**TotalBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | <span data-ttu-id="16f6c-120">Ottiene una stringa che specifica la quantità totale di dati scaricati, in byte.</span><span class="sxs-lookup"><span data-stu-id="16f6c-120">Gets a string that specifies the total amount of data that has been downloaded, in bytes.</span></span>                                                        |
| [<span data-ttu-id="16f6c-121">**TotalBytesToDownload**</span><span class="sxs-lookup"><span data-stu-id="16f6c-121">**TotalBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | <span data-ttu-id="16f6c-122">Ottiene una stringa che rappresenta la stima della quantità totale di dati che verrà scaricata in byte.</span><span class="sxs-lookup"><span data-stu-id="16f6c-122">Gets a string that represents the estimate of the total amount of data that will be downloaded, in bytes.</span></span>                                        |



 

 

 



