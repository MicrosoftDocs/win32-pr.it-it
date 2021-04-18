---
description: 'Il metodo della guida richiama la guida della pagina delle proprietà. Questo metodo implementa il Metodo IPropertyPage:: help.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Metodo CBasePropertyPage. Help (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330690"
---
# <a name="cbasepropertypagehelp-method"></a><span data-ttu-id="f08f1-104">Metodo CBasePropertyPage. Help</span><span class="sxs-lookup"><span data-stu-id="f08f1-104">CBasePropertyPage.Help method</span></span>

<span data-ttu-id="f08f1-105">Il `Help` metodo richiama la guida della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="f08f1-105">The `Help` method invokes the property page help.</span></span> <span data-ttu-id="f08f1-106">Questo metodo implementa il metodo **IPropertyPage:: Help** .</span><span class="sxs-lookup"><span data-stu-id="f08f1-106">This method implements the **IPropertyPage::Help** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f08f1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f08f1-107">Syntax</span></span>


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a><span data-ttu-id="f08f1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f08f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f08f1-109">*lpszHelpDir*</span><span class="sxs-lookup"><span data-stu-id="f08f1-109">*lpszHelpDir*</span></span> 
</dt> <dd>

<span data-ttu-id="f08f1-110">Puntatore alla stringa sotto la chiave **helpDir** nelle informazioni sul CLSID della pagina delle proprietà nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f08f1-110">Pointer to the string under the **HelpDir** key in the property page's CLSID information in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f08f1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f08f1-111">Return value</span></span>

<span data-ttu-id="f08f1-112">Restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="f08f1-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f08f1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f08f1-113">Remarks</span></span>

<span data-ttu-id="f08f1-114">Nella classe base il metodo restituisce sempre E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="f08f1-114">In the base class, the method always returns E\_NOTIMPL.</span></span> <span data-ttu-id="f08f1-115">Quando il metodo ha esito negativo, il frame chiama **IPropertyPage:: GetPageInfo** per ottenere il nome del file della guida e l'identificatore di contesto.</span><span class="sxs-lookup"><span data-stu-id="f08f1-115">When the method fails, the frame calls **IPropertyPage::GetPageInfo** to get the name of the help file and context identifier.</span></span> <span data-ttu-id="f08f1-116">Per impostazione predefinita, questi **valori sono null**.</span><span class="sxs-lookup"><span data-stu-id="f08f1-116">By default, these are **NULL**.</span></span> <span data-ttu-id="f08f1-117">Per fornire la guida, pertanto, la classe derivata può eseguire l'override del metodo `Help` o del metodo [**CBasePropertyPage:: GetPageInfo**](cbasepropertypage-getpageinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f08f1-117">To provide help, therefore, the derived class can override either the `Help` method or the [**CBasePropertyPage::GetPageInfo**](cbasepropertypage-getpageinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f08f1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f08f1-118">Requirements</span></span>



| <span data-ttu-id="f08f1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f08f1-119">Requirement</span></span> | <span data-ttu-id="f08f1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f08f1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f08f1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f08f1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f08f1-122"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f08f1-122"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f08f1-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f08f1-123">Library</span></span><br/> | <dl> <span data-ttu-id="f08f1-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f08f1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f08f1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f08f1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f08f1-126">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="f08f1-126">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




