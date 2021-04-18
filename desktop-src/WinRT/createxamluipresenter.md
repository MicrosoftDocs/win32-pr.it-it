---
description: Funzione creatrice statica che può creare un XamlUIPresenter per una superficie di rendering in un'applicazione desktop.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: CreateXamlUIPresenter (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333903"
---
# <a name="createxamluipresenter-function"></a><span data-ttu-id="9d715-103">CreateXamlUIPresenter (funzione)</span><span class="sxs-lookup"><span data-stu-id="9d715-103">CreateXamlUIPresenter function</span></span>

<span data-ttu-id="9d715-104">Funzione creatrice statica che può creare un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) per una superficie di rendering in un'applicazione desktop.</span><span class="sxs-lookup"><span data-stu-id="9d715-104">A static creator function that can create a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) for a render surface in a desktop app.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d715-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d715-105">Syntax</span></span>


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a><span data-ttu-id="9d715-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d715-107">*pPresentSite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d715-107">*pPresentSite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d715-108">Interfaccia host esistente.</span><span class="sxs-lookup"><span data-stu-id="9d715-108">An existing hosting interface.</span></span> <span data-ttu-id="9d715-109">Vedere **IViewObjectPresentNotifySite** nella documentazione di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9d715-109">See **IViewObjectPresentNotifySite** in Internet Explorer documentation.</span></span>

</dd> <dt>

<span data-ttu-id="9d715-110">*ppPresenter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d715-110">*ppPresenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d715-111">Interfaccia **\[ ExclusiveTo \]** per un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="9d715-111">The **\[exclusiveto\]** interface for a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d715-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d715-112">Return value</span></span>

<span data-ttu-id="9d715-113">Un **HRESULT** standard, **S \_ OK** per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9d715-113">A standard **HResult**, **S\_OK** for success.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d715-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d715-114">Remarks</span></span>

<span data-ttu-id="9d715-115">Per chiamare questo metodo è necessario un **dllimport** da Windows.UI.Xaml.dll.</span><span class="sxs-lookup"><span data-stu-id="9d715-115">Calling this method requires a **DllImport** from Windows.UI.Xaml.dll.</span></span>

<span data-ttu-id="9d715-116">Non è possibile chiamare questo metodo da un'app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9d715-116">You cannot call this method from a Windows Store app.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d715-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d715-117">Requirements</span></span>



| <span data-ttu-id="9d715-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d715-118">Requirement</span></span> | <span data-ttu-id="9d715-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9d715-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d715-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d715-120">Header</span></span><br/> | <dl> <span data-ttu-id="9d715-121"><dt>Windows. UI. XAML-coretypes. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d715-121"><dt>Windows.ui.xaml-coretypes.idl</dt></span></span> </dl> |
| <span data-ttu-id="9d715-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9d715-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="9d715-123"><dt>Windows.UI.Xaml.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d715-123"><dt>Windows.UI.Xaml.dll</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="9d715-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d715-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d715-125">**XamlUIPresenter**</span><span class="sxs-lookup"><span data-stu-id="9d715-125">**XamlUIPresenter**</span></span>](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
