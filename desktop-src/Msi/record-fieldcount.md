---
description: La proprietà FieldCount dell'oggetto record è una proprietà di sola lettura che restituisce il numero di campi nel record. L'accesso in lettura ai campi oltre questo conteggio restituisce valori null. Errore di accesso in scrittura.
ms.assetid: 50be848a-2d38-4768-aeb4-25cbaedade01
title: Proprietà record. FieldCount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FieldCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 548c1da4c2a0106cbcd667b5ce3c915ec17bf1ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328771"
---
# <a name="recordfieldcount-property"></a><span data-ttu-id="828d5-105">Proprietà record. FieldCount</span><span class="sxs-lookup"><span data-stu-id="828d5-105">Record.FieldCount property</span></span>

<span data-ttu-id="828d5-106">La proprietà **FieldCount** dell'oggetto [**record**](record-object.md) è una proprietà di sola lettura che restituisce il numero di campi nel record.</span><span class="sxs-lookup"><span data-stu-id="828d5-106">The **FieldCount** property of the [**Record**](record-object.md) object is a read-only property that returns the number of fields in the record.</span></span> <span data-ttu-id="828d5-107">L'accesso in lettura ai campi oltre questo conteggio restituisce valori null.</span><span class="sxs-lookup"><span data-stu-id="828d5-107">Read access to fields beyond this count returns Null values.</span></span> <span data-ttu-id="828d5-108">Errore di accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="828d5-108">Write access fails.</span></span>

<span data-ttu-id="828d5-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="828d5-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="828d5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="828d5-110">Syntax</span></span>


```JScript
propVal = Record.FieldCount
```



## <a name="property-value"></a><span data-ttu-id="828d5-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="828d5-111">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="828d5-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="828d5-112">Requirements</span></span>



| <span data-ttu-id="828d5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="828d5-113">Requirement</span></span> | <span data-ttu-id="828d5-114">Valore</span><span class="sxs-lookup"><span data-stu-id="828d5-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="828d5-115">Versione</span><span class="sxs-lookup"><span data-stu-id="828d5-115">Version</span></span><br/> | <span data-ttu-id="828d5-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="828d5-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="828d5-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="828d5-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="828d5-118">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="828d5-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="828d5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="828d5-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="828d5-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="828d5-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="828d5-121">IID</span><span class="sxs-lookup"><span data-stu-id="828d5-121">IID</span></span><br/>     | <span data-ttu-id="828d5-122">IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="828d5-122">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




