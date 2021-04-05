---
description: Recupera le impostazioni di contesto predefinite per il tablet.
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: 'Metodo ITablet:: GetDefaultContextSettings'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7e2f0977257553d8405b337dcc1f22d8b0fdff5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757349"
---
# <a name="itabletgetdefaultcontextsettings-method"></a><span data-ttu-id="9f901-103">Metodo ITablet:: GetDefaultContextSettings</span><span class="sxs-lookup"><span data-stu-id="9f901-103">ITablet::GetDefaultContextSettings method</span></span>

<span data-ttu-id="9f901-104">Recupera le impostazioni di contesto predefinite per il tablet.</span><span class="sxs-lookup"><span data-stu-id="9f901-104">Retrieves the default context settings for the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f901-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f901-105">Syntax</span></span>


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a><span data-ttu-id="9f901-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f901-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f901-107">*ppTCS* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9f901-107">*ppTCS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f901-108">Impostazioni di contesto predefinite per il tablet.</span><span class="sxs-lookup"><span data-stu-id="9f901-108">The default context settings for the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f901-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f901-109">Return value</span></span>

<span data-ttu-id="9f901-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="9f901-110">This method can return one of these values.</span></span>



| <span data-ttu-id="9f901-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9f901-111">Return code</span></span>                                                                            | <span data-ttu-id="9f901-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f901-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="9f901-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9f901-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="9f901-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9f901-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="9f901-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="9f901-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="9f901-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="9f901-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9f901-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f901-117">Remarks</span></span>

<span data-ttu-id="9f901-118">È responsabilità del chiamante liberare la memoria restituita da questo metodo usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="9f901-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f901-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f901-119">Requirements</span></span>



| <span data-ttu-id="9f901-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f901-120">Requirement</span></span> | <span data-ttu-id="9f901-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9f901-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f901-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f901-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9f901-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9f901-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9f901-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f901-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9f901-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9f901-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9f901-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f901-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f901-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f901-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f901-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f901-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f901-129">**Interfaccia ITablet**</span><span class="sxs-lookup"><span data-stu-id="9f901-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

