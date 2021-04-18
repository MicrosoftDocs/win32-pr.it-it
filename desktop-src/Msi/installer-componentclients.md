---
description: La proprietà ComponentClients di sola lettura restituisce un oggetto String enumerando il set di client di un componente specificato.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Proprietà Installer. ComponentClients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329028"
---
# <a name="installercomponentclients-property"></a><span data-ttu-id="a6614-103">Proprietà Installer. ComponentClients</span><span class="sxs-lookup"><span data-stu-id="a6614-103">Installer.ComponentClients property</span></span>

<span data-ttu-id="a6614-104">La proprietà **ComponentClients** di sola lettura restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di client di un componente specificato.</span><span class="sxs-lookup"><span data-stu-id="a6614-104">The read-only **ComponentClients** property returns a [**StringList**](stringlist-object.md) object enumerating the set of clients of a specified component.</span></span>

<span data-ttu-id="a6614-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a6614-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6614-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6614-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a><span data-ttu-id="a6614-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a6614-107">Property value</span></span>

<span data-ttu-id="a6614-108">GUID di stringa che rappresenta il codice componente del componente.</span><span class="sxs-lookup"><span data-stu-id="a6614-108">A string GUID that represents the component code of the component.</span></span> <span data-ttu-id="a6614-109">I codici dei componenti vengono specificati nella colonna ComponentId della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a6614-109">The component codes are specified in the ComponentId column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6614-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6614-110">Remarks</span></span>

<span data-ttu-id="a6614-111">Per enumerare i client del componente, un'applicazione può eseguire l'iterazione dell'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto.</span><span class="sxs-lookup"><span data-stu-id="a6614-111">To enumerate the component clients, an application may iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="a6614-112">Poiché i client non sono ordinati, eventuali nuovi componenti hanno un indice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="a6614-112">Because clients are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="a6614-113">Ciò significa che la funzione può restituire client in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="a6614-113">This means that the function may return clients in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6614-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6614-114">Requirements</span></span>



| <span data-ttu-id="a6614-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6614-115">Requirement</span></span> | <span data-ttu-id="a6614-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a6614-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6614-117">Versione</span><span class="sxs-lookup"><span data-stu-id="a6614-117">Version</span></span><br/> | <span data-ttu-id="a6614-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a6614-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a6614-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a6614-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a6614-120">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6614-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a6614-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a6614-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a6614-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6614-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a6614-123">IID</span><span class="sxs-lookup"><span data-stu-id="a6614-123">IID</span></span><br/>     | <span data-ttu-id="a6614-124">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a6614-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="a6614-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6614-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6614-126">**MsiEnumClients**</span><span class="sxs-lookup"><span data-stu-id="a6614-126">**MsiEnumClients**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




