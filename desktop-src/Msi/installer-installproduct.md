---
description: Il metodo InstallProduct dell'oggetto Installer apre un pacchetto di installazione e Inizializza una sessione di installazione.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Installer. InstallProduct, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324618"
---
# <a name="installerinstallproduct-method"></a><span data-ttu-id="469ed-103">Installer. InstallProduct, metodo</span><span class="sxs-lookup"><span data-stu-id="469ed-103">Installer.InstallProduct method</span></span>

<span data-ttu-id="469ed-104">Il metodo **InstallProduct** dell'oggetto [**Installer**](installer-object.md) apre un pacchetto di installazione e Inizializza una sessione di installazione.</span><span class="sxs-lookup"><span data-stu-id="469ed-104">The **InstallProduct** method of the [**Installer**](installer-object.md) object opens an installer package and initializes an install session.</span></span>

## <a name="syntax"></a><span data-ttu-id="469ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="469ed-105">Syntax</span></span>


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a><span data-ttu-id="469ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="469ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="469ed-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="469ed-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="469ed-108">Stringa obbligatoria contenente il percorso del pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="469ed-108">Required string containing the path to the install package.</span></span>

</dd> <dt>

<span data-ttu-id="469ed-109">*propertyValues*</span><span class="sxs-lookup"><span data-stu-id="469ed-109">*propertyValues*</span></span> 
</dt> <dd>

<span data-ttu-id="469ed-110">Stringa facoltativa che contiene le coppie proprietà = valore separate da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="469ed-110">Optional string containing property=value pairs separated by white space.</span></span>

<span data-ttu-id="469ed-111">Per eseguire un'installazione amministrativa, includere ACTION = ADMIN in *propertyValues*.</span><span class="sxs-lookup"><span data-stu-id="469ed-111">To perform an administrative installation, include ACTION=ADMIN in *propertyValues*.</span></span> <span data-ttu-id="469ed-112">Per ulteriori informazioni, vedere la proprietà [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="469ed-112">For more information, see the [**ACTION**](action.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="469ed-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="469ed-113">Return value</span></span>

<span data-ttu-id="469ed-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="469ed-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="469ed-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="469ed-115">Remarks</span></span>

<span data-ttu-id="469ed-116">Per rimuovere completamente un prodotto, impostare REMOVE = ALL in *propertyValues*.</span><span class="sxs-lookup"><span data-stu-id="469ed-116">To completely remove a product, set REMOVE=ALL in *propertyValues*.</span></span> <span data-ttu-id="469ed-117">Per ulteriori informazioni, vedere [**Remove**](remove.md) Property.</span><span class="sxs-lookup"><span data-stu-id="469ed-117">For more information, see [**REMOVE**](remove.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="469ed-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="469ed-118">Requirements</span></span>



| <span data-ttu-id="469ed-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="469ed-119">Requirement</span></span> | <span data-ttu-id="469ed-120">Valore</span><span class="sxs-lookup"><span data-stu-id="469ed-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="469ed-121">Versione</span><span class="sxs-lookup"><span data-stu-id="469ed-121">Version</span></span><br/> | <span data-ttu-id="469ed-122">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="469ed-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="469ed-123">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="469ed-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="469ed-124">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="469ed-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="469ed-125">DLL</span><span class="sxs-lookup"><span data-stu-id="469ed-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="469ed-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="469ed-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="469ed-127">IID</span><span class="sxs-lookup"><span data-stu-id="469ed-127">IID</span></span><br/>     | <span data-ttu-id="469ed-128">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="469ed-128">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




