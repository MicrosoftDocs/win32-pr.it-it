---
description: Avvia un download di dati al chiamante.
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: Metodo IWiaTransfer::D ownload (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 2863915b850588d4db018693d9081ed2907d644a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526455"
---
# <a name="iwiatransferdownload-method"></a><span data-ttu-id="e16dc-103">IWiaTransfer::D Metodo ownload</span><span class="sxs-lookup"><span data-stu-id="e16dc-103">IWiaTransfer::Download method</span></span>

<span data-ttu-id="e16dc-104">Avvia un download di dati al chiamante.</span><span class="sxs-lookup"><span data-stu-id="e16dc-104">Initiates a data download to the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="e16dc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e16dc-105">Syntax</span></span>


```C++
HRESULT Download(
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="e16dc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e16dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e16dc-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16dc-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16dc-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="e16dc-108">Type: **LONG**</span></span>

<span data-ttu-id="e16dc-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="e16dc-109">Currently unused.</span></span> <span data-ttu-id="e16dc-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="e16dc-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e16dc-111">*pIWiaTransferCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16dc-111">*pIWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16dc-112">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="e16dc-112">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="e16dc-113">Specifica un puntatore all'interfaccia [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) del chiamante.</span><span class="sxs-lookup"><span data-stu-id="e16dc-113">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e16dc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e16dc-114">Return value</span></span>

<span data-ttu-id="e16dc-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e16dc-115">Type: **HRESULT**</span></span>

<span data-ttu-id="e16dc-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e16dc-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e16dc-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e16dc-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e16dc-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e16dc-118">Remarks</span></span>

<span data-ttu-id="e16dc-119">Se viene scaricata una cartella, vengono trasferiti anche tutti gli elementi figlio di tale cartella.</span><span class="sxs-lookup"><span data-stu-id="e16dc-119">If a folder is downloaded, then all the child items of that folder are also transferred.</span></span> <span data-ttu-id="e16dc-120">Ogni elemento viene trasferito in un flusso separato.</span><span class="sxs-lookup"><span data-stu-id="e16dc-120">Each item is transferred in a separate stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="e16dc-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e16dc-121">Requirements</span></span>



| <span data-ttu-id="e16dc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e16dc-122">Requirement</span></span> | <span data-ttu-id="e16dc-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e16dc-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e16dc-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e16dc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e16dc-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e16dc-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e16dc-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e16dc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e16dc-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e16dc-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e16dc-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e16dc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e16dc-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e16dc-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="e16dc-130">IDL</span><span class="sxs-lookup"><span data-stu-id="e16dc-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e16dc-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e16dc-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="e16dc-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="e16dc-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e16dc-133"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e16dc-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




