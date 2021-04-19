---
description: Aggiorna il digitalizzatore del Tablet alle coordinate del mapping della posizione della finestra.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: 'Metodo ITabletContextP:: TrackInputRect'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317924"
---
# <a name="itabletcontextptrackinputrect-method"></a><span data-ttu-id="f9bfe-103">Metodo ITabletContextP:: TrackInputRect</span><span class="sxs-lookup"><span data-stu-id="f9bfe-103">ITabletContextP::TrackInputRect method</span></span>

<span data-ttu-id="f9bfe-104">Aggiorna il digitalizzatore del Tablet alle coordinate del mapping della posizione della finestra.</span><span class="sxs-lookup"><span data-stu-id="f9bfe-104">Updates the tablet digitizer to window location mapping coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9bfe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9bfe-105">Syntax</span></span>


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="f9bfe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9bfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9bfe-107">*prcInput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f9bfe-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9bfe-108">Nuovo rettangolo della finestra di input dopo l'aggiornamento del mapping tra le coordinate della finestra e del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="f9bfe-108">The new input window rectangle after updating the mapping between the window and digitizer coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9bfe-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9bfe-109">Return value</span></span>

<span data-ttu-id="f9bfe-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f9bfe-110">This method can return one of these values.</span></span>



| <span data-ttu-id="f9bfe-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f9bfe-111">Return code</span></span>                                                                            | <span data-ttu-id="f9bfe-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9bfe-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="f9bfe-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9bfe-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="f9bfe-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f9bfe-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="f9bfe-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="f9bfe-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="f9bfe-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="f9bfe-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9bfe-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9bfe-117">Remarks</span></span>

<span data-ttu-id="f9bfe-118">Chiamare questo metodo ogni volta che viene modificata la posizione della finestra sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="f9bfe-118">Call this method anytime the location of the window on the screen changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9bfe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9bfe-119">Requirements</span></span>



| <span data-ttu-id="f9bfe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9bfe-120">Requirement</span></span> | <span data-ttu-id="f9bfe-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f9bfe-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9bfe-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9bfe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9bfe-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f9bfe-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f9bfe-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9bfe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9bfe-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f9bfe-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f9bfe-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="f9bfe-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9bfe-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f9bfe-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9bfe-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9bfe-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9bfe-129">**Interfaccia ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="f9bfe-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




