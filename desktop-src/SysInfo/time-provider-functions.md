---
description: Le funzioni seguenti vengono usate dai provider di servizi temporali.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Funzioni del provider Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316051"
---
# <a name="time-provider-functions"></a><span data-ttu-id="22f6d-103">Funzioni del provider Time</span><span class="sxs-lookup"><span data-stu-id="22f6d-103">Time Provider Functions</span></span>

<span data-ttu-id="22f6d-104">Le funzioni seguenti vengono usate dai provider di servizi temporali.</span><span class="sxs-lookup"><span data-stu-id="22f6d-104">The following functions are used by time providers.</span></span>



| <span data-ttu-id="22f6d-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="22f6d-105">Function</span></span>                                                               | <span data-ttu-id="22f6d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22f6d-106">Description</span></span>                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22f6d-107">**AlertSamplesAvailFunc**</span><span class="sxs-lookup"><span data-stu-id="22f6d-107">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | <span data-ttu-id="22f6d-108">Notifica al sistema che sono disponibili nuovi esempi.</span><span class="sxs-lookup"><span data-stu-id="22f6d-108">Notifies the system that there are new samples available.</span></span>                                              |
| [<span data-ttu-id="22f6d-109">**GetTimeSysInfoFunc**</span><span class="sxs-lookup"><span data-stu-id="22f6d-109">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | <span data-ttu-id="22f6d-110">Recupera le informazioni sullo stato dell'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="22f6d-110">Retrieves the system time state information.</span></span>                                                           |
| [<span data-ttu-id="22f6d-111">**LogTimeProvEventFunc**</span><span class="sxs-lookup"><span data-stu-id="22f6d-111">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | <span data-ttu-id="22f6d-112">Registra un evento del provider di tempo nel registro eventi.</span><span class="sxs-lookup"><span data-stu-id="22f6d-112">Logs a time provider event in the event log.</span></span>                                                           |
| [<span data-ttu-id="22f6d-113">**SetProviderStatusFunc**</span><span class="sxs-lookup"><span data-stu-id="22f6d-113">**SetProviderStatusFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | <span data-ttu-id="22f6d-114">Imposta le informazioni sullo stato del provider di tempo.</span><span class="sxs-lookup"><span data-stu-id="22f6d-114">Sets the time provider's status information.</span></span>                                                           |
| [<span data-ttu-id="22f6d-115">**SetProviderStatusInfoFreeFunc**</span><span class="sxs-lookup"><span data-stu-id="22f6d-115">**SetProviderStatusInfoFreeFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | <span data-ttu-id="22f6d-116">Libera una struttura [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) .</span><span class="sxs-lookup"><span data-stu-id="22f6d-116">Frees a [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) structure.</span></span>                          |
| [<span data-ttu-id="22f6d-117">**TimeProvClose**</span><span class="sxs-lookup"><span data-stu-id="22f6d-117">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | <span data-ttu-id="22f6d-118">Funzione di callback chiamata da gestione provider del tempo per arrestare il provider di tempo.</span><span class="sxs-lookup"><span data-stu-id="22f6d-118">A callback function that is called by the time provider manager to shut down the time provider.</span></span>        |
| [<span data-ttu-id="22f6d-119">**TimeProvCommand**</span><span class="sxs-lookup"><span data-stu-id="22f6d-119">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | <span data-ttu-id="22f6d-120">Funzione di callback chiamata dal gestore del provider di servizi temporali per inviare comandi al provider di servizi temporali.</span><span class="sxs-lookup"><span data-stu-id="22f6d-120">A callback function that is called by the time provider manager to send commands to the time provider.</span></span> |
| [<span data-ttu-id="22f6d-121">**TimeProvOpen**</span><span class="sxs-lookup"><span data-stu-id="22f6d-121">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | <span data-ttu-id="22f6d-122">Funzione di callback chiamata dal gestore del provider di servizi temporali quando viene caricata la DLL del provider di servizi temporali.</span><span class="sxs-lookup"><span data-stu-id="22f6d-122">A callback function that is called by the time provider manager when the time provider DLL is loaded.</span></span>  |



 

 

 



