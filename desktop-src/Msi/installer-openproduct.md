---
description: Il metodo OpenProduct dell'oggetto Installer apre un pacchetto di installazione per un prodotto installato utilizzando il codice prodotto e restituisce un oggetto sessione.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Installer. OpenProduct, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332178"
---
# <a name="installeropenproduct-method"></a><span data-ttu-id="94fa4-103">Installer. OpenProduct, metodo</span><span class="sxs-lookup"><span data-stu-id="94fa4-103">Installer.OpenProduct method</span></span>

<span data-ttu-id="94fa4-104">Il metodo **OpenProduct** dell'oggetto [**Installer**](installer-object.md) apre un pacchetto di installazione per un prodotto installato utilizzando il codice prodotto e restituisce un oggetto [**sessione**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="94fa4-104">The **OpenProduct** method of the [**Installer**](installer-object.md) object opens an installer package for an installed product using the product code and returns a [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="94fa4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94fa4-105">Syntax</span></span>


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a><span data-ttu-id="94fa4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="94fa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94fa4-107">*productCode*</span><span class="sxs-lookup"><span data-stu-id="94fa4-107">*productCode*</span></span> 
</dt> <dd>

<span data-ttu-id="94fa4-108">Stringa obbligatoria che contiene il codice prodotto univoco ( [GUID](guid.md)) o un descrittore di attivazione scritto dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="94fa4-108">Required string containing the unique product code (a [GUID](guid.md)) or an activation descriptor written by the installer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94fa4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94fa4-109">Return value</span></span>

<span data-ttu-id="94fa4-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="94fa4-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94fa4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="94fa4-111">Remarks</span></span>

<span data-ttu-id="94fa4-112">Si noti che solo un oggetto [**sessione**](session-object.md) può essere aperto da un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="94fa4-112">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="94fa4-113">Non è possibile usare **OpenProduct** in un'azione personalizzata perché l'installazione attiva è l'unica sessione consentita.</span><span class="sxs-lookup"><span data-stu-id="94fa4-113">**OpenProduct** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="94fa4-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94fa4-114">Requirements</span></span>



| <span data-ttu-id="94fa4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="94fa4-115">Requirement</span></span> | <span data-ttu-id="94fa4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="94fa4-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94fa4-117">Versione</span><span class="sxs-lookup"><span data-stu-id="94fa4-117">Version</span></span><br/> | <span data-ttu-id="94fa4-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="94fa4-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="94fa4-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="94fa4-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="94fa4-120">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="94fa4-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="94fa4-121">DLL</span><span class="sxs-lookup"><span data-stu-id="94fa4-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="94fa4-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94fa4-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="94fa4-123">IID</span><span class="sxs-lookup"><span data-stu-id="94fa4-123">IID</span></span><br/>     | <span data-ttu-id="94fa4-124">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="94fa4-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




