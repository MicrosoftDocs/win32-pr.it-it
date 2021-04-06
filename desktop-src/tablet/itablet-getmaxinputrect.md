---
description: Recupera un rettangolo che rappresenta l'area di input massima della tavoletta.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: 'Metodo ITablet:: GetMaxInputRect'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: de2649fe7410e6d335f653c09bfe86a8ddaac813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883742"
---
# <a name="itabletgetmaxinputrect-method"></a><span data-ttu-id="3f223-103">Metodo ITablet:: GetMaxInputRect</span><span class="sxs-lookup"><span data-stu-id="3f223-103">ITablet::GetMaxInputRect method</span></span>

<span data-ttu-id="3f223-104">Recupera un rettangolo che rappresenta l'area di input massima della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="3f223-104">Retrieves a rectangle that represents maximum input area of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f223-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f223-105">Syntax</span></span>


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="3f223-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f223-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f223-107">*prcInput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3f223-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f223-108">Puntatore al rettangolo che rappresenta l'area di input massima della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="3f223-108">Pointer to rectangle that represents maximum input area of the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f223-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f223-109">Return value</span></span>

<span data-ttu-id="3f223-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3f223-110">This method can return one of these values.</span></span>



| <span data-ttu-id="3f223-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3f223-111">Return code</span></span>                                                                            | <span data-ttu-id="3f223-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f223-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3f223-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f223-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3f223-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3f223-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3f223-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="3f223-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3f223-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="3f223-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3f223-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f223-117">Requirements</span></span>



| <span data-ttu-id="3f223-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f223-118">Requirement</span></span> | <span data-ttu-id="3f223-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3f223-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f223-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f223-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3f223-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3f223-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3f223-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f223-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3f223-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3f223-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3f223-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f223-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f223-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f223-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f223-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f223-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f223-127">**Interfaccia ITablet**</span><span class="sxs-lookup"><span data-stu-id="3f223-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




