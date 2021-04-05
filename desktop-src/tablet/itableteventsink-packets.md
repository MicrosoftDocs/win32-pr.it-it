---
description: Si verifica quando lo stilo viene spostato sul digitalizzatore.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: ITabletEventSink::P metodo ackets
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fb671b0556cf121e28ae81c5dcfa804208e00006
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967929"
---
# <a name="itableteventsinkpackets-method"></a><span data-ttu-id="eb210-103">ITabletEventSink::P metodo ackets</span><span class="sxs-lookup"><span data-stu-id="eb210-103">ITabletEventSink::Packets method</span></span>

<span data-ttu-id="eb210-104">Si verifica quando lo stilo viene spostato sul digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="eb210-104">Occurs when the stylus is moving on the digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb210-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb210-105">Syntax</span></span>


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="eb210-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb210-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb210-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb210-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb210-108">Identificatore del tablet.</span><span class="sxs-lookup"><span data-stu-id="eb210-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="eb210-109">*cPkts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb210-109">*cPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb210-110">Numero di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="eb210-110">The number of packets.</span></span>

</dd> <dt>

<span data-ttu-id="eb210-111">*cbPkts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb210-111">*cbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb210-112">Dimensioni del buffer di pacchetti</span><span class="sxs-lookup"><span data-stu-id="eb210-112">The size of packet buffer</span></span>

</dd> <dt>

<span data-ttu-id="eb210-113">*pbPkts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb210-113">*pbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb210-114">Buffer del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="eb210-114">The packet buffer.</span></span>

</dd> <dt>

<span data-ttu-id="eb210-115">*pnSerialNumbers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb210-115">*pnSerialNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb210-116">Matrice di numeri di serie.</span><span class="sxs-lookup"><span data-stu-id="eb210-116">The serial number array.</span></span>

</dd> <dt>

<span data-ttu-id="eb210-117">*CID*</span><span class="sxs-lookup"><span data-stu-id="eb210-117">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="eb210-118">Identificatore dello stilo.</span><span class="sxs-lookup"><span data-stu-id="eb210-118">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb210-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb210-119">Return value</span></span>

<span data-ttu-id="eb210-120">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="eb210-120">This method can return one of these values.</span></span>



| <span data-ttu-id="eb210-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="eb210-121">Return code</span></span>                                                                            | <span data-ttu-id="eb210-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb210-122">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="eb210-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eb210-123"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="eb210-124">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="eb210-124">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="eb210-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="eb210-125"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="eb210-126">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="eb210-126">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="eb210-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb210-127">Requirements</span></span>



| <span data-ttu-id="eb210-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb210-128">Requirement</span></span> | <span data-ttu-id="eb210-129">Valore</span><span class="sxs-lookup"><span data-stu-id="eb210-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb210-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb210-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eb210-131">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="eb210-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="eb210-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb210-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eb210-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="eb210-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eb210-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb210-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb210-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb210-135"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb210-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb210-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb210-137">**Interfaccia ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="eb210-137">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




