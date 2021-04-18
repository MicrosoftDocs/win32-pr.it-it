---
description: Crea un enumeratore per i formati di trasferimento supportati dal dispositivo Windows Image Acquisition (WIA) 2,0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'Metodo IWiaTransfer:: EnumWIA_FORMAT_INFO (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307354"
---
# <a name="iwiatransferenumwia_format_info-method"></a><span data-ttu-id="005f1-103">\_Metodo informazioni sul formato IWiaTransfer:: EnumWIA \_</span><span class="sxs-lookup"><span data-stu-id="005f1-103">IWiaTransfer::EnumWIA\_FORMAT\_INFO method</span></span>

<span data-ttu-id="005f1-104">Crea un enumeratore per i formati di trasferimento supportati dal dispositivo Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="005f1-104">Creates an enumerator for the transfer formats that the Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="005f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="005f1-105">Syntax</span></span>


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="005f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="005f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="005f1-107">*ppIEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="005f1-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="005f1-108">Tipo: **[ **IEnumWIA \_ \_ info Format**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="005f1-108">Type: **[**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span></span>

<span data-ttu-id="005f1-109">Indirizzo del puntatore all'interfaccia [**IEnumWIA \_ Format \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) per l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="005f1-109">The address of the pointer to the [**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) interface for the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="005f1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="005f1-110">Return value</span></span>

<span data-ttu-id="005f1-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="005f1-111">Type: **HRESULT**</span></span>

<span data-ttu-id="005f1-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="005f1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="005f1-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="005f1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="005f1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="005f1-114">Remarks</span></span>

<span data-ttu-id="005f1-115">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore a interfaccia ricevuto tramite il parametro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="005f1-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointer received through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="005f1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="005f1-116">Requirements</span></span>



| <span data-ttu-id="005f1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="005f1-117">Requirement</span></span> | <span data-ttu-id="005f1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="005f1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="005f1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="005f1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="005f1-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="005f1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="005f1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="005f1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="005f1-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="005f1-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="005f1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="005f1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="005f1-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="005f1-124"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="005f1-125">IDL</span><span class="sxs-lookup"><span data-stu-id="005f1-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="005f1-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="005f1-126"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="005f1-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="005f1-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="005f1-128"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="005f1-128"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
