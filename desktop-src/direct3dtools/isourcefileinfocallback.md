---
description: Callback per restituire informazioni sul file di origine da un stack.
MS-HAID: vspixengine.ISourceFileInfoCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia ISourceFileInfoCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0430DFF0-F3EA-4645-9B91-E849C0F99609
api_name:
- ISourceFileInfoCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c627d07bfbf455a9c62a922f62adcab945d5741
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747583"
---
# <a name="span-idvspixengineisourcefileinfocallbackspanisourcefileinfocallback-interface"></a><span data-ttu-id="f3baf-103"><span id="vspixengine.isourcefileinfocallback"></span>Interfaccia ISourceFileInfoCallback</span><span class="sxs-lookup"><span data-stu-id="f3baf-103"><span id="vspixengine.isourcefileinfocallback"></span>ISourceFileInfoCallback interface</span></span>

<span data-ttu-id="f3baf-104">Callback per restituire informazioni sul file di origine da un stack.</span><span class="sxs-lookup"><span data-stu-id="f3baf-104">Callback to return source file info from a callstack.</span></span>

## <a name="members"></a><span data-ttu-id="f3baf-105">Membri</span><span class="sxs-lookup"><span data-stu-id="f3baf-105">Members</span></span>

<span data-ttu-id="f3baf-106">L'interfaccia **ISourceFileInfoCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f3baf-106">The **ISourceFileInfoCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f3baf-107">**ISourceFileInfoCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f3baf-107">**ISourceFileInfoCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f3baf-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="f3baf-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f3baf-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="f3baf-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f3baf-110">L'interfaccia **ISourceFileInfoCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f3baf-110">The **ISourceFileInfoCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f3baf-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="f3baf-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f3baf-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3baf-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f3baf-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3baf-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f3baf-114">Funzione di callback utilizzata per notificare all'host le informazioni sui file di origine associati a stack.</span><span class="sxs-lookup"><span data-stu-id="f3baf-114">A callback function used to notify the host of information about source files associated with the callstack.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f3baf-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3baf-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f3baf-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3baf-116">Header</span></span></p></td><td><span data-ttu-id="f3baf-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f3baf-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
