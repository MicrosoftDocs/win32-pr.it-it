---
title: Metodo WSMan. EnumerationFlagNonXmlText (WSManDisp. h)
description: Restituisce il valore della costante di enumerazione WSManFlagNonXmlText per l'utilizzo nel parametro Flags del metodo Session. enumerate.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo EnumerationFlagNonXmlText
- Metodo EnumerationFlagNonXmlText Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo EnumerationFlagNonXmlText
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a9547f85a07702dc3735129842e5bc286ee9b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742359"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a><span data-ttu-id="03083-106">WSMan. EnumerationFlagNonXmlText, metodo</span><span class="sxs-lookup"><span data-stu-id="03083-106">WSMan.EnumerationFlagNonXmlText method</span></span>

<span data-ttu-id="03083-107">**WSMan. EnumerationFlagNonXmlText** restituisce il valore della costante di enumerazione **WSManFlagNonXmlText** da usare nel parametro *Flags* del metodo [**Session. enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="03083-107">The **WSMan.EnumerationFlagNonXmlText** returns the value of the enumeration constant **WSManFlagNonXmlText** for use in the *flags* parameter of the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="03083-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="03083-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="03083-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="03083-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="03083-110">**WSManFlagNonXmlText** è una costante nell'enumerazione **\_ \_ WSManEnumFlags** .</span><span class="sxs-lookup"><span data-stu-id="03083-110">**WSManFlagNonXmlText** is a constant in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="03083-111">Per altre informazioni, vedere [**costanti di enumerazione**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="03083-111">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03083-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03083-112">Syntax</span></span>


```VB
WSMan.EnumerationFlagNonXmlText( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="03083-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="03083-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03083-114">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="03083-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03083-115">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="03083-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03083-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03083-116">Return value</span></span>

<span data-ttu-id="03083-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="03083-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03083-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03083-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="03083-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03083-119">Requirements</span></span>



| <span data-ttu-id="03083-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="03083-120">Requirement</span></span> | <span data-ttu-id="03083-121">Valore</span><span class="sxs-lookup"><span data-stu-id="03083-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="03083-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03083-122">Minimum supported client</span></span><br/> | <span data-ttu-id="03083-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03083-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="03083-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03083-124">Minimum supported server</span></span><br/> | <span data-ttu-id="03083-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03083-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="03083-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03083-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="03083-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="03083-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="03083-128">IDL</span><span class="sxs-lookup"><span data-stu-id="03083-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="03083-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03083-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="03083-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="03083-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="03083-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="03083-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="03083-132">DLL</span><span class="sxs-lookup"><span data-stu-id="03083-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03083-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03083-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="03083-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03083-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03083-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="03083-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="03083-136">**IWSManEx**</span><span class="sxs-lookup"><span data-stu-id="03083-136">**IWSManEx**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[<span data-ttu-id="03083-137">**IWSManSession**</span><span class="sxs-lookup"><span data-stu-id="03083-137">**IWSManSession**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





