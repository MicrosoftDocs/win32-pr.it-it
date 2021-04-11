---
description: Determina se un dispositivo di input supporta il multitouch.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'Metodo ITablet3:: datamultitouch'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233174"
---
# <a name="itablet3ismultitouch-method"></a><span data-ttu-id="09d99-103">Metodo ITablet3:: datamultitouch</span><span class="sxs-lookup"><span data-stu-id="09d99-103">ITablet3::IsMultiTouch method</span></span>

<span data-ttu-id="09d99-104">Determina se un dispositivo di input supporta il multitouch.</span><span class="sxs-lookup"><span data-stu-id="09d99-104">Determines whether an input device supports multitouch.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d99-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09d99-105">Syntax</span></span>


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a><span data-ttu-id="09d99-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="09d99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d99-107">*bIsMultiTouch* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="09d99-107">*bIsMultiTouch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09d99-108">Indica se il dispositivo è multitouch.</span><span class="sxs-lookup"><span data-stu-id="09d99-108">Indicates whether the device is multitouch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09d99-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09d99-109">Return value</span></span>

<span data-ttu-id="09d99-110">Restituisce **\_ OK** in caso di esito positivo; in caso contrario, restituisce un codice di errore, ad esempio **E \_ Fail**.</span><span class="sxs-lookup"><span data-stu-id="09d99-110">Returns **S\_OK** on success, otherwise returns an error code such as **E\_FAIL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="09d99-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="09d99-111">Remarks</span></span>

<span data-ttu-id="09d99-112">Dopo aver determinato l'utilizzo di [**IRealTimeStylus3:: MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) o **ITablet3::** multitouch, il multitouch è disponibile, un'applicazione può scegliere di acconsentire esplicitamente ai messaggi di input multitouch.</span><span class="sxs-lookup"><span data-stu-id="09d99-112">After determining through [**IRealTimeStylus3::MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) or **ITablet3::IsMultiTouch** that multitouch is available, an application may choose to opt in for multitouch input messages.</span></span> <span data-ttu-id="09d99-113">Altre informazioni sul filtro dei metodi multitouch sono disponibili nella sezione proprietà **IRealTimeStylus3:: MultiTouchEnabled** .</span><span class="sxs-lookup"><span data-stu-id="09d99-113">Additional information on filtering multitouch methods is available in the **IRealTimeStylus3::MultiTouchEnabled** property section.</span></span>

## <a name="examples"></a><span data-ttu-id="09d99-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="09d99-114">Examples</span></span>


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a><span data-ttu-id="09d99-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09d99-115">Requirements</span></span>



| <span data-ttu-id="09d99-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="09d99-116">Requirement</span></span> | <span data-ttu-id="09d99-117">Valore</span><span class="sxs-lookup"><span data-stu-id="09d99-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09d99-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09d99-118">Minimum supported client</span></span><br/> | <span data-ttu-id="09d99-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="09d99-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="09d99-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09d99-120">Minimum supported server</span></span><br/> | <span data-ttu-id="09d99-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="09d99-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="09d99-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="09d99-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="09d99-123"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09d99-123"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09d99-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09d99-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d99-125">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="09d99-125">**ITablet3**</span></span>](itablet3.md)
</dt> <dt>

[<span data-ttu-id="09d99-126">**MultiTouchEnabled**</span><span class="sxs-lookup"><span data-stu-id="09d99-126">**MultiTouchEnabled**</span></span>](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




