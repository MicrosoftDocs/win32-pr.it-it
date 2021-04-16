---
description: Callback per restituire informazioni sulla presenza o meno nella cache di una richiesta offline.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IOfflineAnalysisCacheCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E226B1A6-D028-4562-9C8C-D25EC91A2DB2
api_name:
- IOfflineAnalysisCacheCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e0107f97353bf7ad5b62472bc54a2b8388fb6aff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522369"
---
# <a name="span-idvspixengineiofflineanalysiscachecallbackspaniofflineanalysiscachecallback-interface"></a><span data-ttu-id="1a855-103"><span id="vspixengine.iofflineanalysiscachecallback"></span>Interfaccia IOfflineAnalysisCacheCallback</span><span class="sxs-lookup"><span data-stu-id="1a855-103"><span id="vspixengine.iofflineanalysiscachecallback"></span>IOfflineAnalysisCacheCallback interface</span></span>

<span data-ttu-id="1a855-104">Callback per restituire informazioni sulla presenza o meno nella cache di una richiesta offline.</span><span class="sxs-lookup"><span data-stu-id="1a855-104">Callback to return information on whether an offline request is cached or not.</span></span>

## <a name="members"></a><span data-ttu-id="1a855-105">Membri</span><span class="sxs-lookup"><span data-stu-id="1a855-105">Members</span></span>

<span data-ttu-id="1a855-106">L'interfaccia **IOfflineAnalysisCacheCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1a855-106">The **IOfflineAnalysisCacheCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1a855-107">**IOfflineAnalysisCacheCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1a855-107">**IOfflineAnalysisCacheCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="1a855-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="1a855-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="1a855-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="1a855-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="1a855-110">L'interfaccia **IOfflineAnalysisCacheCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1a855-110">The **IOfflineAnalysisCacheCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="1a855-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="1a855-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="1a855-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a855-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="1a855-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscachecallback-offlineanalaysisreportavailabilitycallback-dword-dword-arr"><strong>OfflineAnalaysisReportAvailabilityCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a855-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscachecallback-offlineanalaysisreportavailabilitycallback-dword-dword-arr"><strong>OfflineAnalaysisReportAvailabilityCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1a855-114">Funzione di callback utilizzata per notificare all'host i frame con report di analisi offline disponibili.</span><span class="sxs-lookup"><span data-stu-id="1a855-114">A callback function used to notify the host about which frames have offline analysis reports available.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="1a855-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a855-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1a855-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a855-116">Header</span></span></p></td><td><span data-ttu-id="1a855-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1a855-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
