---
description: Il metodo ViewBillboard dell'oggetto UIPreview Visualizza un cartellone creato con il controllo host nella finestra di dialogo attualmente visualizzata.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: UIPreview. ViewBillboard, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327914"
---
# <a name="uipreviewviewbillboard-method"></a><span data-ttu-id="0baff-103">UIPreview. ViewBillboard, metodo</span><span class="sxs-lookup"><span data-stu-id="0baff-103">UIPreview.ViewBillboard method</span></span>

<span data-ttu-id="0baff-104">Il metodo **ViewBillboard** dell'oggetto [**UIPreview**](uipreview-object.md) Visualizza un cartellone creato con il controllo host nella finestra di dialogo attualmente visualizzata.</span><span class="sxs-lookup"><span data-stu-id="0baff-104">The **ViewBillboard** method of the [**UIPreview**](uipreview-object.md) object displays an authored billboard using the host control in the currently displayed dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="0baff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0baff-105">Syntax</span></span>


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a><span data-ttu-id="0baff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0baff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0baff-107">*control*</span><span class="sxs-lookup"><span data-stu-id="0baff-107">*control*</span></span> 
</dt> <dd>

<span data-ttu-id="0baff-108">Nome obbligatorio del controllo che ospita il tabellone, con distinzione tra maiuscole e minuscole, con la finestra di dialogo e con le chiavi primarie della tabella del database del controllo.</span><span class="sxs-lookup"><span data-stu-id="0baff-108">Required name of the control hosting the billboard, case-sensitive, along with the dialog box, and the primary keys of the Control database table.</span></span>

</dd> <dt>

<span data-ttu-id="0baff-109">*Billboard*</span><span class="sxs-lookup"><span data-stu-id="0baff-109">*billboard*</span></span> 
</dt> <dd>

<span data-ttu-id="0baff-110">Nome obbligatorio del tabellone da visualizzare utilizzando il controllo specificato e la finestra di dialogo corrente e la chiave primaria della tabella del database Billboard.</span><span class="sxs-lookup"><span data-stu-id="0baff-110">Required name of the billboard to display using the specified control and current dialog box, and the primary key of the Billboard database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0baff-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0baff-111">Return value</span></span>

<span data-ttu-id="0baff-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0baff-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0baff-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0baff-113">Requirements</span></span>



| <span data-ttu-id="0baff-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0baff-114">Requirement</span></span> | <span data-ttu-id="0baff-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0baff-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0baff-116">Versione</span><span class="sxs-lookup"><span data-stu-id="0baff-116">Version</span></span><br/> | <span data-ttu-id="0baff-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0baff-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0baff-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0baff-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0baff-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0baff-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0baff-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0baff-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="0baff-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0baff-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0baff-122">IID</span><span class="sxs-lookup"><span data-stu-id="0baff-122">IID</span></span><br/>     | <span data-ttu-id="0baff-123">IID \_ IUIPreview è definito come 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0baff-123">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




