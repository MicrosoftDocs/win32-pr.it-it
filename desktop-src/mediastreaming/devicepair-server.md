---
title: Proprietà del server DevicePair (Asptlb. h)
description: Ottiene il server per la coppia di dispositivi di base attiva.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- API di streaming multimediale delle proprietà del server
- API di streaming multimediale delle proprietà del server, interfaccia DevicePair
- API di streaming multimediale dell'interfaccia DevicePair, proprietà del server
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323912"
---
# <a name="devicepairserver-property"></a><span data-ttu-id="999e0-106">Proprietà DevicePair:: Server</span><span class="sxs-lookup"><span data-stu-id="999e0-106">DevicePair::Server property</span></span>

<span data-ttu-id="999e0-107">Ottiene il server per la coppia di dispositivi di base attiva.</span><span class="sxs-lookup"><span data-stu-id="999e0-107">Gets the server for the active basic device pair.</span></span>

<span data-ttu-id="999e0-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="999e0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="999e0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="999e0-109">Syntax</span></span>


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a><span data-ttu-id="999e0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="999e0-110">Property value</span></span>

<span data-ttu-id="999e0-111">Riceve un oggetto [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) che rappresenta il dispositivo server.</span><span class="sxs-lookup"><span data-stu-id="999e0-111">Receives a [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) object that represents the server device.</span></span>

## <a name="requirements"></a><span data-ttu-id="999e0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="999e0-112">Requirements</span></span>



| <span data-ttu-id="999e0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="999e0-113">Requirement</span></span> | <span data-ttu-id="999e0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="999e0-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="999e0-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="999e0-115">Header</span></span><br/> | <dl> <span data-ttu-id="999e0-116"><dt>Asptlb. h</dt></span><span class="sxs-lookup"><span data-stu-id="999e0-116"><dt>Asptlb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="999e0-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="999e0-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="999e0-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="999e0-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span></span>
</dt> </dl>

 

