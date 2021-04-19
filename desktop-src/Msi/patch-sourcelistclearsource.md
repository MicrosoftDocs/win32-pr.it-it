---
description: Rimuove un'origine di rete o URL.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Patch. SourceListClearSource, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325900"
---
# <a name="patchsourcelistclearsource-method"></a><span data-ttu-id="e2871-103">Patch. SourceListClearSource, metodo</span><span class="sxs-lookup"><span data-stu-id="e2871-103">Patch.SourceListClearSource method</span></span>

<span data-ttu-id="e2871-104">Il metodo **SourceListClearSource** rimuove un'origine di rete o URL.</span><span class="sxs-lookup"><span data-stu-id="e2871-104">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="e2871-105">Questo metodo chiama [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span><span class="sxs-lookup"><span data-stu-id="e2871-105">This method calls [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2871-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2871-106">Syntax</span></span>


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="e2871-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2871-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2871-108">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="e2871-108">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="e2871-109">Tipo di origine da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e2871-109">Type of source to be removed.</span></span>

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

<span data-ttu-id="e2871-110">**\_rete MSISOURCETYPE**</span><span class="sxs-lookup"><span data-stu-id="e2871-110">**MSISOURCETYPE\_NETWORK**</span></span>
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

<span data-ttu-id="e2871-111">**\_URL MSISOURCETYPE**</span><span class="sxs-lookup"><span data-stu-id="e2871-111">**MSISOURCETYPE\_URL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="e2871-112">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="e2871-112">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="e2871-113">Percorso dell'origine da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e2871-113">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2871-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2871-114">Return value</span></span>

<span data-ttu-id="e2871-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e2871-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2871-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2871-116">Requirements</span></span>



| <span data-ttu-id="e2871-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2871-117">Requirement</span></span> | <span data-ttu-id="e2871-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e2871-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2871-119">Versione</span><span class="sxs-lookup"><span data-stu-id="e2871-119">Version</span></span><br/> | <span data-ttu-id="e2871-120">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e2871-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e2871-121">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2871-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e2871-122">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e2871-122">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e2871-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e2871-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2871-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2871-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e2871-125">IID</span><span class="sxs-lookup"><span data-stu-id="e2871-125">IID</span></span><br/>     | <span data-ttu-id="e2871-126">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e2871-126">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="e2871-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2871-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2871-128">**Patch**</span><span class="sxs-lookup"><span data-stu-id="e2871-128">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="e2871-129">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="e2871-129">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="e2871-130">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="e2871-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




