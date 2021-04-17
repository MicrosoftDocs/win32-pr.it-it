---
description: Recupera il numero di versione del sistema di eventi.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'Metodo IEventSystem2:: GetVersion'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483869"
---
# <a name="ieventsystem2getversion-method"></a><span data-ttu-id="add40-103">Metodo IEventSystem2:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="add40-103">IEventSystem2::GetVersion method</span></span>

<span data-ttu-id="add40-104">Recupera il numero di versione del sistema di eventi.</span><span class="sxs-lookup"><span data-stu-id="add40-104">Retrieves the version number of the event system.</span></span>

## <a name="syntax"></a><span data-ttu-id="add40-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="add40-105">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a><span data-ttu-id="add40-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="add40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add40-107">*pnVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="add40-107">*pnVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="add40-108">Numero di versione del sistema di eventi.</span><span class="sxs-lookup"><span data-stu-id="add40-108">The version number of the event system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add40-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="add40-109">Return value</span></span>

<span data-ttu-id="add40-110">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="add40-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="add40-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="add40-111">Requirements</span></span>



| <span data-ttu-id="add40-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="add40-112">Requirement</span></span> | <span data-ttu-id="add40-113">Valore</span><span class="sxs-lookup"><span data-stu-id="add40-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="add40-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="add40-114">Minimum supported client</span></span><br/> | <span data-ttu-id="add40-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="add40-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="add40-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="add40-116">Minimum supported server</span></span><br/> | <span data-ttu-id="add40-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="add40-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="add40-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="add40-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add40-119">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="add40-119">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




