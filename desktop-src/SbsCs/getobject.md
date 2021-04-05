---
description: Il metodo GetObject recupera un'istanza di un oggetto Microsoft. Windows. ActCtx esistente.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx. GetObject, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750962"
---
# <a name="actctxgetobject-method"></a><span data-ttu-id="12ec8-103">ActCtx. GetObject, metodo</span><span class="sxs-lookup"><span data-stu-id="12ec8-103">ActCtx.GetObject method</span></span>

<span data-ttu-id="12ec8-104">Il metodo **GetObject** recupera un'istanza di un oggetto [**Microsoft. Windows. ACTCTX**](microsoft-windows-actctx-object.md) esistente.</span><span class="sxs-lookup"><span data-stu-id="12ec8-104">The **GetObject** method gets an instance of an existing [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="12ec8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12ec8-105">Syntax</span></span>


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a><span data-ttu-id="12ec8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12ec8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ec8-107">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="12ec8-107">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="12ec8-108">Stringa obbligatoria che indica l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="12ec8-108">Required string that indicates the object.</span></span> <span data-ttu-id="12ec8-109">Il nome deve trovarsi nel registro di sistema in **HKEY \_ \_ computer locale** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.</span><span class="sxs-lookup"><span data-stu-id="12ec8-109">The name must be in the registry under **HKEY\_LOCAL\_MACHINE**\\**Microsoft**\\**Visual Studio**\\**6.0**\\**<package>**\\**Automation**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ec8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12ec8-110">Return value</span></span>

<span data-ttu-id="12ec8-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="12ec8-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ec8-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12ec8-112">Requirements</span></span>



| <span data-ttu-id="12ec8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="12ec8-113">Requirement</span></span> | <span data-ttu-id="12ec8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="12ec8-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="12ec8-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12ec8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="12ec8-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12ec8-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="12ec8-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12ec8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="12ec8-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12ec8-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="12ec8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="12ec8-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12ec8-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12ec8-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="12ec8-121">IID</span><span class="sxs-lookup"><span data-stu-id="12ec8-121">IID</span></span><br/>                      | <span data-ttu-id="12ec8-122">IID \_ IActCtx è definito come 8FA7728F-B69B-4ee5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="12ec8-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="12ec8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12ec8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ec8-124">**Metodo CreateObject**</span><span class="sxs-lookup"><span data-stu-id="12ec8-124">**CreateObject Method**</span></span>](createobject.md)
</dt> </dl>

 

 




