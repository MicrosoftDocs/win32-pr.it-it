---
description: Il metodo CreaRecord dell'oggetto Installer restituisce un nuovo oggetto record con il numero di campi richiesto.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Installer. CreaRecord, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333877"
---
# <a name="installercreaterecord-method"></a><span data-ttu-id="e153a-103">Installer. CreaRecord, metodo</span><span class="sxs-lookup"><span data-stu-id="e153a-103">Installer.CreateRecord method</span></span>

<span data-ttu-id="e153a-104">Il metodo **CreaRecord** dell'oggetto [**Installer**](installer-object.md) restituisce un nuovo oggetto [**record**](record-object.md) con il numero di campi richiesto.</span><span class="sxs-lookup"><span data-stu-id="e153a-104">The **CreateRecord** method of the [**Installer**](installer-object.md) object returns a new [**Record**](record-object.md) object with the requested number of fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="e153a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e153a-105">Syntax</span></span>


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a><span data-ttu-id="e153a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e153a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e153a-107">*count*</span><span class="sxs-lookup"><span data-stu-id="e153a-107">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="e153a-108">Numero di campi obbligatorio, che può essere 0.</span><span class="sxs-lookup"><span data-stu-id="e153a-108">Required number of fields, which may be 0.</span></span> <span data-ttu-id="e153a-109">Il numero massimo di campi in un record è limitato a 65535.</span><span class="sxs-lookup"><span data-stu-id="e153a-109">The maximum number of fields in a record is limited to 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e153a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e153a-110">Return value</span></span>

<span data-ttu-id="e153a-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e153a-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e153a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e153a-112">Remarks</span></span>

<span data-ttu-id="e153a-113">Il campo 0, non uno dei campi in *count*, viene in genere usato per gli elementi orientati ai record, ad esempio le stringhe di formato o i codici op di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e153a-113">Field 0, not one of the fields in *count*, is normally used for record-oriented items such as format strings or execution op-codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="e153a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e153a-114">Requirements</span></span>



| <span data-ttu-id="e153a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e153a-115">Requirement</span></span> | <span data-ttu-id="e153a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e153a-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e153a-117">Versione</span><span class="sxs-lookup"><span data-stu-id="e153a-117">Version</span></span><br/> | <span data-ttu-id="e153a-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e153a-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e153a-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e153a-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e153a-120">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e153a-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e153a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e153a-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e153a-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e153a-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e153a-123">IID</span><span class="sxs-lookup"><span data-stu-id="e153a-123">IID</span></span><br/>     | <span data-ttu-id="e153a-124">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e153a-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




