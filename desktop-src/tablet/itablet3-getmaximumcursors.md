---
description: Il metodo GetMaximumCursors Recupera il numero massimo di cursori supportati da un dispositivo tablet.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'Metodo ITablet3:: GetMaximumCursors'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313919"
---
# <a name="itablet3getmaximumcursors-method"></a><span data-ttu-id="009d7-103">Metodo ITablet3:: GetMaximumCursors</span><span class="sxs-lookup"><span data-stu-id="009d7-103">ITablet3::GetMaximumCursors method</span></span>

<span data-ttu-id="009d7-104">Il metodo **GetMaximumCursors** Recupera il numero massimo di cursori supportati da un dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="009d7-104">The **GetMaximumCursors** method retrieves the maximum number of cursors that a tablet device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="009d7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="009d7-105">Syntax</span></span>


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a><span data-ttu-id="009d7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="009d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="009d7-107">*pMaximumCursors*</span><span class="sxs-lookup"><span data-stu-id="009d7-107">*pMaximumCursors*</span></span> 
</dt> <dd>

<span data-ttu-id="009d7-108">Numero massimo di input supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="009d7-108">The maximum number of inputs that the device supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="009d7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="009d7-109">Return value</span></span>

<span data-ttu-id="009d7-110">Restituisce \_ OK in caso di esito positivo; in caso contrario, restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="009d7-110">Returns S\_OK on success; otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="009d7-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="009d7-111">Requirements</span></span>



| <span data-ttu-id="009d7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="009d7-112">Requirement</span></span> | <span data-ttu-id="009d7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="009d7-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="009d7-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="009d7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="009d7-115">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="009d7-115">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="009d7-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="009d7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="009d7-117">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="009d7-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="009d7-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="009d7-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="009d7-119"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="009d7-119"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="009d7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="009d7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="009d7-121">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="009d7-121">**ITablet3**</span></span>](itablet3.md)
</dt> </dl>

 

 




