---
description: 'Costruttore CBasePropertyPage.CBasePropertyPage : metodo costruttore.'
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Costruttore CBasePropertyPage.CBasePropertyPage (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95821062b6b1199ea98a5329934d76e2197901d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119949"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a><span data-ttu-id="a6ded-103">Costruttore CBasePropertyPage.CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="a6ded-103">CBasePropertyPage.CBasePropertyPage constructor</span></span>

<span data-ttu-id="a6ded-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="a6ded-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ded-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6ded-105">Syntax</span></span>


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a><span data-ttu-id="a6ded-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6ded-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ded-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="a6ded-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ded-108">Stringa che contiene il nome dell'oggetto a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="a6ded-108">String that contains the name of the object, for debugging purposes.</span></span> <span data-ttu-id="a6ded-109">Per altre informazioni, vedere [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="a6ded-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6ded-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="a6ded-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ded-111">Puntatore all'interfaccia **IUnknown aggregata.**</span><span class="sxs-lookup"><span data-stu-id="a6ded-111">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="a6ded-112">*Id dialogo*</span><span class="sxs-lookup"><span data-stu-id="a6ded-112">*DialogId*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ded-113">ID risorsa per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a6ded-113">Resource ID for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="a6ded-114">*TitleId*</span><span class="sxs-lookup"><span data-stu-id="a6ded-114">*TitleId*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ded-115">ID risorsa per la stringa che contiene il titolo della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a6ded-115">Resource ID for the string that contains the dialog box title.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a6ded-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="a6ded-116">Examples</span></span>


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a><span data-ttu-id="a6ded-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6ded-117">Requirements</span></span>



| <span data-ttu-id="a6ded-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6ded-118">Requirement</span></span> | <span data-ttu-id="a6ded-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a6ded-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ded-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6ded-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a6ded-121"><dt>Cprop.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ded-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a6ded-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="a6ded-122">Library</span></span><br/> | <dl> <span data-ttu-id="a6ded-123"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ded-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ded-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6ded-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ded-125">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="a6ded-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




