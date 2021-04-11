---
description: Avvia un caricamento di dati di un singolo elemento dal chiamante.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'Metodo IWiaTransfer:: upload (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226146"
---
# <a name="iwiatransferupload-method"></a><span data-ttu-id="20728-103">Metodo IWiaTransfer:: upload</span><span class="sxs-lookup"><span data-stu-id="20728-103">IWiaTransfer::Upload method</span></span>

<span data-ttu-id="20728-104">Avvia un caricamento di dati di un singolo elemento dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="20728-104">Initiates a data upload of a single item from the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="20728-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20728-105">Syntax</span></span>


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="20728-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20728-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20728-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20728-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20728-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="20728-108">Type: **LONG**</span></span>

<span data-ttu-id="20728-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="20728-109">Currently unused.</span></span> <span data-ttu-id="20728-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="20728-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="20728-111">*pSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20728-111">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20728-112">Tipo: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="20728-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="20728-113">Specifica un puntatore ai dati [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="20728-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) data.</span></span>

</dd> <dt>

<span data-ttu-id="20728-114">_pIWiaTransferCallback \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20728-114">_pIWiaTransferCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20728-115">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="20728-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="20728-116">Specifica un puntatore all'interfaccia [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) del chiamante.</span><span class="sxs-lookup"><span data-stu-id="20728-116">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20728-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20728-117">Return value</span></span>

<span data-ttu-id="20728-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="20728-118">Type: **HRESULT**</span></span>

<span data-ttu-id="20728-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="20728-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="20728-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="20728-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="20728-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20728-121">Requirements</span></span>



| <span data-ttu-id="20728-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="20728-122">Requirement</span></span> | <span data-ttu-id="20728-123">Valore</span><span class="sxs-lookup"><span data-stu-id="20728-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20728-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20728-124">Minimum supported client</span></span><br/> | <span data-ttu-id="20728-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20728-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="20728-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20728-126">Minimum supported server</span></span><br/> | <span data-ttu-id="20728-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20728-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="20728-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20728-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="20728-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="20728-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="20728-130">IDL</span><span class="sxs-lookup"><span data-stu-id="20728-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20728-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20728-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="20728-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="20728-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="20728-133"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20728-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
