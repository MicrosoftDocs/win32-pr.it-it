---
description: Callback per restituisce dati di analisi offline.
MS-HAID: vspixengine.IOfflineAnalysisCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IOfflineAnalysisCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 39E6B9CA-C17A-42C8-AC6D-118DC8DE3AD9
api_name:
- IOfflineAnalysisCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 496ca07544cdc38ff9f0e3f29c0ebbd2b9e8753c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304343"
---
# <a name="span-idvspixengineiofflineanalysiscallbackspaniofflineanalysiscallback-interface"></a><span data-ttu-id="a323c-103"><span id="vspixengine.iofflineanalysiscallback"></span>Interfaccia IOfflineAnalysisCallback</span><span class="sxs-lookup"><span data-stu-id="a323c-103"><span id="vspixengine.iofflineanalysiscallback"></span>IOfflineAnalysisCallback interface</span></span>

<span data-ttu-id="a323c-104">Callback per restituisce dati di analisi offline.</span><span class="sxs-lookup"><span data-stu-id="a323c-104">Callback to returns offline analysis data.</span></span>

## <a name="members"></a><span data-ttu-id="a323c-105">Membri</span><span class="sxs-lookup"><span data-stu-id="a323c-105">Members</span></span>

<span data-ttu-id="a323c-106">L'interfaccia **IOfflineAnalysisCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a323c-106">The **IOfflineAnalysisCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a323c-107">**IOfflineAnalysisCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a323c-107">**IOfflineAnalysisCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="a323c-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="a323c-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="a323c-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="a323c-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="a323c-110">L'interfaccia **IOfflineAnalysisCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a323c-110">The **IOfflineAnalysisCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="a323c-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="a323c-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="a323c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a323c-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a323c-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>OfflineAnalysisComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="a323c-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>OfflineAnalysisComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a323c-114">Funzione di callback utilizzata per notificare all'host che l'analisi offline è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a323c-114">A callback function used to notify the host that offline analysis has completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="a323c-115"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>OfflineAnalysisProgress</strong></a></span><span class="sxs-lookup"><span data-stu-id="a323c-115"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>OfflineAnalysisProgress</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a323c-116">Funzione di callback utilizzata per notificare all'host lo stato di avanzamento dell'analisi offline.</span><span class="sxs-lookup"><span data-stu-id="a323c-116">A callback function used to notify the host of offline analysis progress.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="a323c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a323c-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a323c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a323c-118">Header</span></span></p></td><td><span data-ttu-id="a323c-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a323c-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
