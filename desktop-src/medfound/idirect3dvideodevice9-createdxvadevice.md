---
description: Crea un dispositivo di decodificatore DirectX Video Acceleration (DXVA).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'Metodo IDirect3DVideoDevice9:: CreateDXVADevice (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 50ce7cee350479f4286921b6cdf69b319033c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130342"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a><span data-ttu-id="251fd-103">Metodo IDirect3DVideoDevice9:: CreateDXVADevice</span><span class="sxs-lookup"><span data-stu-id="251fd-103">IDirect3DVideoDevice9::CreateDXVADevice method</span></span>

<span data-ttu-id="251fd-104">Crea un dispositivo di decodificatore DirectX Video Acceleration (DXVA).</span><span class="sxs-lookup"><span data-stu-id="251fd-104">Creates a DirectX Video Acceleration (DXVA) decoder device.</span></span>

## <a name="syntax"></a><span data-ttu-id="251fd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="251fd-105">Syntax</span></span>


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a><span data-ttu-id="251fd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="251fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="251fd-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="251fd-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="251fd-108">Puntatore a un GUID che specifica il dispositivo da creare.</span><span class="sxs-lookup"><span data-stu-id="251fd-108">Pointer to a GUID that specifies the device to create.</span></span>

</dd> <dt>

<span data-ttu-id="251fd-109">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="251fd-109">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="251fd-110">Puntatore a una struttura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) che specifica il formato dell'immagine non compressa.</span><span class="sxs-lookup"><span data-stu-id="251fd-110">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the format of the uncompressed image.</span></span>

</dd> <dt>

<span data-ttu-id="251fd-111">*pData*</span><span class="sxs-lookup"><span data-stu-id="251fd-111">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="251fd-112">Puntatore a una struttura **DXVA \_ ConnectMode** che specifica la modalità DXVA e il profilo con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="251fd-112">Pointer to a **DXVA\_ConnectMode** structure that specifies the DXVA mode and restricted profile.</span></span>

</dd> <dt>

<span data-ttu-id="251fd-113">*DataSize*</span><span class="sxs-lookup"><span data-stu-id="251fd-113">*DataSize*</span></span> 
</dt> <dd>

<span data-ttu-id="251fd-114">Dimensione della struttura **\_ ConnectMode di DXVA** in byte.</span><span class="sxs-lookup"><span data-stu-id="251fd-114">Size of the **DXVA\_ConnectMode** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="251fd-115">*ppDXVADevice*</span><span class="sxs-lookup"><span data-stu-id="251fd-115">*ppDXVADevice*</span></span> 
</dt> <dd>

<span data-ttu-id="251fd-116">Riceve un puntatore all'interfaccia [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) .</span><span class="sxs-lookup"><span data-stu-id="251fd-116">Receives a pointer to the [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) interface.</span></span> <span data-ttu-id="251fd-117">Il chiamante deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="251fd-117">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="251fd-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="251fd-118">Return value</span></span>

<span data-ttu-id="251fd-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="251fd-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="251fd-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="251fd-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="251fd-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="251fd-121">Requirements</span></span>



| <span data-ttu-id="251fd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="251fd-122">Requirement</span></span> | <span data-ttu-id="251fd-123">Valore</span><span class="sxs-lookup"><span data-stu-id="251fd-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="251fd-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="251fd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="251fd-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="251fd-125">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="251fd-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="251fd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="251fd-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="251fd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="251fd-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="251fd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="251fd-129"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="251fd-129"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="251fd-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="251fd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="251fd-131">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="251fd-131">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




