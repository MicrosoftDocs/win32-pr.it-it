---
description: Si verifica quando la punta dello stilo contatta la superficie del Tablet di digitalizzazione.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: 'Metodo ITabletEventSink:: CursorDown'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757055"
---
# <a name="itableteventsinkcursordown-method"></a><span data-ttu-id="6cc91-103">Metodo ITabletEventSink:: CursorDown</span><span class="sxs-lookup"><span data-stu-id="6cc91-103">ITabletEventSink::CursorDown method</span></span>

<span data-ttu-id="6cc91-104">Si verifica quando la punta dello stilo contatta la superficie del Tablet di digitalizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cc91-104">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc91-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6cc91-105">Syntax</span></span>


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="6cc91-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6cc91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc91-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cc91-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc91-108">Identificatore del tablet.</span><span class="sxs-lookup"><span data-stu-id="6cc91-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="6cc91-109">*CID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cc91-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc91-110">Identificatore dello stilo.</span><span class="sxs-lookup"><span data-stu-id="6cc91-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="6cc91-111">*nSerialNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cc91-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc91-112">Numero di serie dello stilo.</span><span class="sxs-lookup"><span data-stu-id="6cc91-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="6cc91-113">*cbPkt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cc91-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc91-114">Numero di byte in un pacchetto di dati Stilo.</span><span class="sxs-lookup"><span data-stu-id="6cc91-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="6cc91-115">*pbPkt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cc91-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc91-116">Dati dello stilo che indicano la posizione in cui lo stilo ha toccato il tablet.</span><span class="sxs-lookup"><span data-stu-id="6cc91-116">The stylus data indicating the location where the stylus touched the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc91-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6cc91-117">Return value</span></span>

<span data-ttu-id="6cc91-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="6cc91-118">This method can return one of these values.</span></span>



| <span data-ttu-id="6cc91-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6cc91-119">Return code</span></span>                                                                            | <span data-ttu-id="6cc91-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cc91-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="6cc91-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6cc91-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="6cc91-122">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6cc91-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="6cc91-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="6cc91-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="6cc91-124">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="6cc91-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6cc91-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cc91-125">Requirements</span></span>



| <span data-ttu-id="6cc91-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cc91-126">Requirement</span></span> | <span data-ttu-id="6cc91-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6cc91-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc91-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cc91-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc91-129">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6cc91-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6cc91-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cc91-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc91-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6cc91-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6cc91-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="6cc91-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="6cc91-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6cc91-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cc91-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6cc91-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc91-135">**Interfaccia ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="6cc91-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




