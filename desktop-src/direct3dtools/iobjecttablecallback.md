---
description: Callback per restituire i dati della tabella degli oggetti.
MS-HAID: vspixengine.IObjectTableCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IObjectTableCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D3B5ECD5-DBE1-4E37-8707-CFAEFEE551F1
api_name:
- IObjectTableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4535164048c92e6af381d15ee388212fdc72da4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125553"
---
# <a name="span-idvspixengineiobjecttablecallbackspaniobjecttablecallback-interface"></a><span data-ttu-id="904a3-103"><span id="vspixengine.iobjecttablecallback"></span>Interfaccia IObjectTableCallback</span><span class="sxs-lookup"><span data-stu-id="904a3-103"><span id="vspixengine.iobjecttablecallback"></span>IObjectTableCallback interface</span></span>

<span data-ttu-id="904a3-104">Callback per restituire i dati della tabella degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="904a3-104">Callback to return object table data.</span></span>

## <a name="members"></a><span data-ttu-id="904a3-105">Membri</span><span class="sxs-lookup"><span data-stu-id="904a3-105">Members</span></span>

<span data-ttu-id="904a3-106">L'interfaccia **IObjectTableCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="904a3-106">The **IObjectTableCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="904a3-107">**IObjectTableCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="904a3-107">**IObjectTableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="904a3-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="904a3-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="904a3-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="904a3-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="904a3-110">L'interfaccia **IObjectTableCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="904a3-110">The **IObjectTableCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="904a3-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="904a3-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="904a3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="904a3-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="904a3-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span><span class="sxs-lookup"><span data-stu-id="904a3-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="904a3-114">Ottiene informazioni sulle colonne (tipi di dati oggetto) supportate dalla tabella oggetti.</span><span class="sxs-lookup"><span data-stu-id="904a3-114">Gets information about which columns (types of object data) are supported by the object table.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="904a3-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="904a3-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="904a3-116">Funzione di callback utilizzata per notificare all'host le informazioni sulla tabella degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="904a3-116">A callback function used to notify the host of object table information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="904a3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="904a3-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="904a3-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="904a3-118">Header</span></span></p></td><td><span data-ttu-id="904a3-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="904a3-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
