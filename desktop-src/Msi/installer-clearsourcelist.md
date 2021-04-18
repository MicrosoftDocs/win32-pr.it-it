---
description: Il metodo ClearSourceList dell'oggetto Installer rimuove tutte le origini di rete dall'elenco di origine.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Installer. ClearSourceList, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f9468775c75533b766a160a390410908d04bf6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326985"
---
# <a name="installerclearsourcelist-method"></a><span data-ttu-id="35832-103">Installer. ClearSourceList, metodo</span><span class="sxs-lookup"><span data-stu-id="35832-103">Installer.ClearSourceList method</span></span>

<span data-ttu-id="35832-104">Il metodo **ClearSourceList** dell'oggetto [**Installer**](installer-object.md) rimuove tutte le origini di rete dall'elenco di origine.</span><span class="sxs-lookup"><span data-stu-id="35832-104">The **ClearSourceList** method of the [**Installer**](installer-object.md) object removes all network sources from the source list.</span></span>

## <a name="syntax"></a><span data-ttu-id="35832-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35832-105">Syntax</span></span>


```JScript
Installer.ClearSourceList(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="35832-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35832-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35832-107">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="35832-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="35832-108">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="35832-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="35832-109">*Utente*</span><span class="sxs-lookup"><span data-stu-id="35832-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="35832-110">Nome utente per l'installazione per utente; stringa null o vuota per l'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="35832-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35832-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35832-111">Return value</span></span>

<span data-ttu-id="35832-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="35832-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="35832-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35832-113">Requirements</span></span>



| <span data-ttu-id="35832-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="35832-114">Requirement</span></span> | <span data-ttu-id="35832-115">Valore</span><span class="sxs-lookup"><span data-stu-id="35832-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35832-116">Versione</span><span class="sxs-lookup"><span data-stu-id="35832-116">Version</span></span><br/> | <span data-ttu-id="35832-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="35832-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="35832-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="35832-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="35832-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="35832-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="35832-120">DLL</span><span class="sxs-lookup"><span data-stu-id="35832-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="35832-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35832-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="35832-122">IID</span><span class="sxs-lookup"><span data-stu-id="35832-122">IID</span></span><br/>     | <span data-ttu-id="35832-123">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="35832-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="35832-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35832-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35832-125">**MsiSourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="35832-125">**MsiSourceListClearAll**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[<span data-ttu-id="35832-126">Resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="35832-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




