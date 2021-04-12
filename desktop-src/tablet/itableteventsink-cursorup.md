---
description: Si verifica quando l'utente ha generato lo stilo dalla superficie del digitalizzatore del Tablet PC.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'Metodo ITabletEventSink:: CursorUp'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233872"
---
# <a name="itableteventsinkcursorup-method"></a><span data-ttu-id="0c712-103">Metodo ITabletEventSink:: CursorUp</span><span class="sxs-lookup"><span data-stu-id="0c712-103">ITabletEventSink::CursorUp method</span></span>

<span data-ttu-id="0c712-104">Si verifica quando l'utente ha generato lo stilo dalla superficie del digitalizzatore del Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0c712-104">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c712-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c712-105">Syntax</span></span>


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="0c712-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c712-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c712-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c712-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c712-108">Identificatore del tablet.</span><span class="sxs-lookup"><span data-stu-id="0c712-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="0c712-109">*CID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c712-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c712-110">Identificatore dello stilo.</span><span class="sxs-lookup"><span data-stu-id="0c712-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="0c712-111">*nSerialNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c712-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c712-112">Numero di serie dello stilo.</span><span class="sxs-lookup"><span data-stu-id="0c712-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="0c712-113">*cbPkt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c712-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c712-114">Numero di byte in un pacchetto di dati Stilo.</span><span class="sxs-lookup"><span data-stu-id="0c712-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="0c712-115">*pbPkt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c712-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c712-116">Dati dello stilo che indicano la posizione in cui lo stilo è stato rimosso dal tablet.</span><span class="sxs-lookup"><span data-stu-id="0c712-116">The stylus data indicating the location where the stylus was lifted from the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c712-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c712-117">Return value</span></span>

<span data-ttu-id="0c712-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0c712-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c712-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c712-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c712-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c712-120">Requirements</span></span>



| <span data-ttu-id="0c712-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c712-121">Requirement</span></span> | <span data-ttu-id="0c712-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0c712-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c712-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c712-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0c712-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0c712-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0c712-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c712-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0c712-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0c712-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0c712-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="0c712-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="0c712-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c712-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c712-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c712-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c712-130">**Interfaccia ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="0c712-130">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




