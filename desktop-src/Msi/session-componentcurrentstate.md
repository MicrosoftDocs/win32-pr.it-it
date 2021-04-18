---
description: La proprietà ComponentCurrentState dell'oggetto Session è una proprietà di sola lettura che restituisce lo stato corrente di installazione del componente designato. Per i valori di stato, vedere la proprietà ComponentRequestState.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Proprietà Session. ComponentCurrentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329111"
---
# <a name="sessioncomponentcurrentstate-property"></a><span data-ttu-id="4e823-104">Proprietà Session. ComponentCurrentState</span><span class="sxs-lookup"><span data-stu-id="4e823-104">Session.ComponentCurrentState property</span></span>

<span data-ttu-id="4e823-105">La proprietà **ComponentCurrentState** dell'oggetto [**Session**](session-object.md) è una proprietà di sola lettura che restituisce lo stato corrente di installazione del componente designato.</span><span class="sxs-lookup"><span data-stu-id="4e823-105">The **ComponentCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated component.</span></span> <span data-ttu-id="4e823-106">Per i valori di stato, vedere la proprietà [**ComponentRequestState**](session-componentrequeststate.md) .</span><span class="sxs-lookup"><span data-stu-id="4e823-106">For state values, see the [**ComponentRequestState**](session-componentrequeststate.md) property.</span></span>

<span data-ttu-id="4e823-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4e823-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e823-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e823-108">Syntax</span></span>


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a><span data-ttu-id="4e823-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4e823-109">Property value</span></span>

<span data-ttu-id="4e823-110">Nome della stringa obbligatoria del componente richiesto, chiave primaria nella tabella dei componenti.</span><span class="sxs-lookup"><span data-stu-id="4e823-110">Required string name of the requested component, primary key into the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e823-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e823-111">Remarks</span></span>

<span data-ttu-id="4e823-112">Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="4e823-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e823-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e823-113">Requirements</span></span>



| <span data-ttu-id="4e823-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e823-114">Requirement</span></span> | <span data-ttu-id="4e823-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4e823-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e823-116">Versione</span><span class="sxs-lookup"><span data-stu-id="4e823-116">Version</span></span><br/> | <span data-ttu-id="4e823-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4e823-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4e823-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4e823-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4e823-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="4e823-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4e823-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4e823-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="4e823-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e823-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4e823-122">IID</span><span class="sxs-lookup"><span data-stu-id="4e823-122">IID</span></span><br/>     | <span data-ttu-id="4e823-123">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4e823-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="4e823-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e823-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e823-125">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="4e823-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="4e823-126">**Proprietà ComponentRequestState**</span><span class="sxs-lookup"><span data-stu-id="4e823-126">**ComponentRequestState property**</span></span>](session-componentrequeststate.md)
</dt> </dl>

 

 




