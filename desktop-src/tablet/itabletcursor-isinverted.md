---
description: Indica se lo stilo è capovolto.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'Metodo ITabletCursor:: ininverted'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314914"
---
# <a name="itabletcursorisinverted-method"></a><span data-ttu-id="c06a9-103">Metodo ITabletCursor:: ininverted</span><span class="sxs-lookup"><span data-stu-id="c06a9-103">ITabletCursor::IsInverted method</span></span>

<span data-ttu-id="c06a9-104">Indica se lo stilo è capovolto.</span><span class="sxs-lookup"><span data-stu-id="c06a9-104">Indicates if the stylus is upside down.</span></span>

## <a name="syntax"></a><span data-ttu-id="c06a9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c06a9-105">Syntax</span></span>


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a><span data-ttu-id="c06a9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c06a9-106">Parameters</span></span>

<span data-ttu-id="c06a9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c06a9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c06a9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c06a9-108">Return value</span></span>

<span data-ttu-id="c06a9-109">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="c06a9-109">This method can return one of these values.</span></span>



| <span data-ttu-id="c06a9-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c06a9-110">Return code</span></span>                                                                             | <span data-ttu-id="c06a9-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c06a9-111">Description</span></span>                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="c06a9-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c06a9-112"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c06a9-113">Lo stilo è invertito.</span><span class="sxs-lookup"><span data-stu-id="c06a9-113">The stylus is inverted.</span></span><br/>        |
| <dl> <span data-ttu-id="c06a9-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c06a9-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c06a9-115">Lo stilo non è invertito.</span><span class="sxs-lookup"><span data-stu-id="c06a9-115">The stylus is not inverted.</span></span><br/>    |
| <dl> <span data-ttu-id="c06a9-116"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="c06a9-116"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="c06a9-117">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="c06a9-117">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c06a9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c06a9-118">Requirements</span></span>



| <span data-ttu-id="c06a9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c06a9-119">Requirement</span></span> | <span data-ttu-id="c06a9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c06a9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c06a9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c06a9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c06a9-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c06a9-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c06a9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c06a9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c06a9-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c06a9-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c06a9-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="c06a9-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c06a9-126"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c06a9-126"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c06a9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c06a9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c06a9-128">**ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="c06a9-128">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="c06a9-129">**Interfaccia ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="c06a9-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




