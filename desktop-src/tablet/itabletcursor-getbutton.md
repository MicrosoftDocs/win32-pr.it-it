---
description: Recupera l'oggetto pulsante specificato da uno stilo del tablet.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'Metodo ITabletCursor:: GetButton'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314913"
---
# <a name="itabletcursorgetbutton-method"></a><span data-ttu-id="28506-103">Metodo ITabletCursor:: GetButton</span><span class="sxs-lookup"><span data-stu-id="28506-103">ITabletCursor::GetButton method</span></span>

<span data-ttu-id="28506-104">Recupera l'oggetto pulsante specificato da uno stilo del tablet.</span><span class="sxs-lookup"><span data-stu-id="28506-104">Retrieves the specified button object from a tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="28506-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28506-105">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a><span data-ttu-id="28506-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="28506-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28506-107">*IButton* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28506-107">*iButton* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28506-108">Identificatore del pulsante da recuperare.</span><span class="sxs-lookup"><span data-stu-id="28506-108">Identifier of the button to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="28506-109">*ppButton* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="28506-109">*ppButton* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28506-110">Oggetto Button specificato dal parametro *IButton* .</span><span class="sxs-lookup"><span data-stu-id="28506-110">The button object specified by the *iButton* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28506-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28506-111">Return value</span></span>

<span data-ttu-id="28506-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="28506-112">This method can return one of these values.</span></span>



| <span data-ttu-id="28506-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="28506-113">Return code</span></span>                                                                            | <span data-ttu-id="28506-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28506-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="28506-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="28506-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="28506-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="28506-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="28506-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="28506-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="28506-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="28506-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="28506-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28506-119">Requirements</span></span>



| <span data-ttu-id="28506-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="28506-120">Requirement</span></span> | <span data-ttu-id="28506-121">Valore</span><span class="sxs-lookup"><span data-stu-id="28506-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28506-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28506-122">Minimum supported client</span></span><br/> | <span data-ttu-id="28506-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="28506-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="28506-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28506-124">Minimum supported server</span></span><br/> | <span data-ttu-id="28506-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="28506-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="28506-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="28506-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="28506-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28506-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28506-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28506-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28506-129">**Interfaccia ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="28506-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




