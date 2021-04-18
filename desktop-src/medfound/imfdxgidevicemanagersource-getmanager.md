---
description: Ottiene IMFDXGIDeviceManager dal sink di rendering del video Microsoft Media Foundation.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: 'Metodo IMFDXGIDeviceManagerSource:: GetManager'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310828"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a><span data-ttu-id="d386e-103">Metodo IMFDXGIDeviceManagerSource:: GetManager</span><span class="sxs-lookup"><span data-stu-id="d386e-103">IMFDXGIDeviceManagerSource::GetManager method</span></span>

<span data-ttu-id="d386e-104">Ottiene [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) dal sink di rendering del video Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d386e-104">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="d386e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d386e-105">Syntax</span></span>


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="d386e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d386e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d386e-107">*ppManager* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d386e-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d386e-108">Oggetto [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="d386e-108">The [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d386e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d386e-109">Return value</span></span>

<span data-ttu-id="d386e-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d386e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d386e-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d386e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d386e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d386e-112">Requirements</span></span>



| <span data-ttu-id="d386e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d386e-113">Requirement</span></span> | <span data-ttu-id="d386e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d386e-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d386e-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d386e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d386e-116">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d386e-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d386e-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d386e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d386e-118">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d386e-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="d386e-119">IDL</span><span class="sxs-lookup"><span data-stu-id="d386e-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d386e-120"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d386e-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d386e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d386e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d386e-122">**IMFDXGIDeviceManagerSource**</span><span class="sxs-lookup"><span data-stu-id="d386e-122">**IMFDXGIDeviceManagerSource**</span></span>](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




