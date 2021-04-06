---
title: Metodo WSMan. CreateConnectionOptions (WSManDisp. h)
description: Crea un oggetto ConnectionOptions che specifica il nome utente e la password utilizzati durante la creazione di una sessione.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo CreateConnectionOptions
- Metodo CreateConnectionOptions Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo CreateConnectionOptions
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873541"
---
# <a name="wsmancreateconnectionoptions-method"></a><span data-ttu-id="bad53-106">WSMan. CreateConnectionOptions, metodo</span><span class="sxs-lookup"><span data-stu-id="bad53-106">WSMan.CreateConnectionOptions method</span></span>

<span data-ttu-id="bad53-107">Crea un oggetto [**ConnectionOptions**](connectionoptions.md) che specifica il nome utente e la password utilizzati durante la creazione di una sessione.</span><span class="sxs-lookup"><span data-stu-id="bad53-107">Creates a [**ConnectionOptions**](connectionoptions.md) object that specifies the user name and password used when creating a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad53-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bad53-108">Syntax</span></span>


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a><span data-ttu-id="bad53-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bad53-109">Parameters</span></span>

<span data-ttu-id="bad53-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bad53-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bad53-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bad53-111">Return value</span></span>

<span data-ttu-id="bad53-112">Oggetto [**ConnectionOptions**](connectionoptions.md) utilizzato per specificare una coppia di nome utente e password utilizzata per identificare un utente per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="bad53-112">A [**ConnectionOptions**](connectionoptions.md) object used to specify a user name and password pair that is used to identify a user for authentication.</span></span>

## <a name="remarks"></a><span data-ttu-id="bad53-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bad53-113">Remarks</span></span>

<span data-ttu-id="bad53-114">Per chiamare questo metodo, viene usata la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="bad53-114">The following syntax is used to call this method.</span></span>


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a><span data-ttu-id="bad53-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bad53-115">Requirements</span></span>



| <span data-ttu-id="bad53-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad53-116">Requirement</span></span> | <span data-ttu-id="bad53-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bad53-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bad53-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bad53-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bad53-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bad53-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="bad53-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bad53-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bad53-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bad53-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bad53-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bad53-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bad53-123"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad53-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bad53-124">IDL</span><span class="sxs-lookup"><span data-stu-id="bad53-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bad53-125"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bad53-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="bad53-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="bad53-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="bad53-127"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bad53-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bad53-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bad53-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bad53-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bad53-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bad53-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bad53-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad53-131">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="bad53-131">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="bad53-132">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="bad53-132">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





