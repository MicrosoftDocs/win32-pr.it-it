---
description: La proprietà ProductState è una proprietà di sola lettura che restituisce le informazioni sullo stato di installazione di un prodotto.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Metodo della proprietà Installer. ProductState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329130"
---
# <a name="installerproductstate-property-method"></a><span data-ttu-id="7995e-103">Metodo della proprietà Installer. ProductState</span><span class="sxs-lookup"><span data-stu-id="7995e-103">Installer.ProductState Property method</span></span>

<span data-ttu-id="7995e-104">La **Proprietà ProductState** è una proprietà di sola lettura che restituisce le informazioni sullo stato di installazione di un prodotto.</span><span class="sxs-lookup"><span data-stu-id="7995e-104">The **ProductState property** is a read-only property that returns the install state information for a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="7995e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7995e-105">Syntax</span></span>


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="7995e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7995e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7995e-107">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="7995e-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="7995e-108">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="7995e-108">Specifies the product code of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7995e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7995e-109">Return value</span></span>

<span data-ttu-id="7995e-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7995e-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7995e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7995e-111">Remarks</span></span>

<span data-ttu-id="7995e-112">Restituisce uno dei valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7995e-112">Returns one of the values shown in the following table.</span></span>



| <span data-ttu-id="7995e-113">Stato dell'installazione</span><span class="sxs-lookup"><span data-stu-id="7995e-113">Installation state</span></span>        | <span data-ttu-id="7995e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7995e-114">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="7995e-115">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="7995e-115">msiInstallStateAbsent</span></span>     | <span data-ttu-id="7995e-116">Il prodotto viene installato per un utente diverso.</span><span class="sxs-lookup"><span data-stu-id="7995e-116">The product is installed for a different user.</span></span>   |
| <span data-ttu-id="7995e-117">msiInstallStateDefault</span><span class="sxs-lookup"><span data-stu-id="7995e-117">msiInstallStateDefault</span></span>    | <span data-ttu-id="7995e-118">Il prodotto è installato per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="7995e-118">The product is installed for the current user.</span></span>   |
| <span data-ttu-id="7995e-119">msiInstallStateAdvertised</span><span class="sxs-lookup"><span data-stu-id="7995e-119">msiInstallStateAdvertised</span></span> | <span data-ttu-id="7995e-120">Il prodotto è annunciato ma non è installato.</span><span class="sxs-lookup"><span data-stu-id="7995e-120">The product is advertised but not installed.</span></span>     |
| <span data-ttu-id="7995e-121">msiInstallStateInvalidArg</span><span class="sxs-lookup"><span data-stu-id="7995e-121">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="7995e-122">Un parametro non valido è stato passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="7995e-122">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="7995e-123">msiInstallStateUnknown</span><span class="sxs-lookup"><span data-stu-id="7995e-123">msiInstallStateUnknown</span></span>    | <span data-ttu-id="7995e-124">Il prodotto non è né annunciato né installato.</span><span class="sxs-lookup"><span data-stu-id="7995e-124">The product is neither advertised nor installed.</span></span> |
| <span data-ttu-id="7995e-125">msiInstallStateBadConfig</span><span class="sxs-lookup"><span data-stu-id="7995e-125">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="7995e-126">I dati di configurazione sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="7995e-126">The configuration data is corrupt.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="7995e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7995e-127">Requirements</span></span>



| <span data-ttu-id="7995e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7995e-128">Requirement</span></span> | <span data-ttu-id="7995e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7995e-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7995e-130">Versione</span><span class="sxs-lookup"><span data-stu-id="7995e-130">Version</span></span><br/> | <span data-ttu-id="7995e-131">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7995e-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7995e-132">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7995e-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7995e-133">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="7995e-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7995e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7995e-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="7995e-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7995e-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7995e-136">IID</span><span class="sxs-lookup"><span data-stu-id="7995e-136">IID</span></span><br/>     | <span data-ttu-id="7995e-137">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7995e-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="7995e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7995e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7995e-139">**MsiQueryProductState**</span><span class="sxs-lookup"><span data-stu-id="7995e-139">**MsiQueryProductState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




