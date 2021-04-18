---
description: Il metodo ExtractPatchXMLData dell'oggetto Installer estrae le informazioni da una patch come stringa XML. Le informazioni possono essere utilizzate per determinare se la patch viene applicata a un sistema di destinazione. Questo metodo chiama MsiExtractPatchXMLData.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Installer. ExtractPatchXMLData, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324642"
---
# <a name="installerextractpatchxmldata-method"></a><span data-ttu-id="66cea-105">Installer. ExtractPatchXMLData, metodo</span><span class="sxs-lookup"><span data-stu-id="66cea-105">Installer.ExtractPatchXMLData method</span></span>

<span data-ttu-id="66cea-106">Il metodo **ExtractPatchXMLData** dell'oggetto [**Installer**](installer-object.md) estrae le informazioni da una patch come stringa XML.</span><span class="sxs-lookup"><span data-stu-id="66cea-106">The **ExtractPatchXMLData** method of the [**Installer**](installer-object.md) object extracts information from a patch as an XML string.</span></span> <span data-ttu-id="66cea-107">Le informazioni possono essere utilizzate per determinare se la patch viene applicata a un sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="66cea-107">The information can be used to determine whether the patch applies on a target system.</span></span> <span data-ttu-id="66cea-108">Questo metodo chiama [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span><span class="sxs-lookup"><span data-stu-id="66cea-108">This method calls [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span>

## <a name="syntax"></a><span data-ttu-id="66cea-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66cea-109">Syntax</span></span>


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a><span data-ttu-id="66cea-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="66cea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66cea-111">*PatchPath*</span><span class="sxs-lookup"><span data-stu-id="66cea-111">*PatchPath*</span></span> 
</dt> <dd>

<span data-ttu-id="66cea-112">Percorso completo della patch da cui estrarre le informazioni sull'applicabilità.</span><span class="sxs-lookup"><span data-stu-id="66cea-112">Full path to the patch from which the applicability information is to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66cea-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66cea-113">Return value</span></span>

<span data-ttu-id="66cea-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="66cea-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="66cea-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66cea-115">Requirements</span></span>



| <span data-ttu-id="66cea-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="66cea-116">Requirement</span></span> | <span data-ttu-id="66cea-117">Valore</span><span class="sxs-lookup"><span data-stu-id="66cea-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66cea-118">Versione</span><span class="sxs-lookup"><span data-stu-id="66cea-118">Version</span></span><br/> | <span data-ttu-id="66cea-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="66cea-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="66cea-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="66cea-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="66cea-121">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="66cea-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="66cea-122">DLL</span><span class="sxs-lookup"><span data-stu-id="66cea-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="66cea-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66cea-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="66cea-124">IID</span><span class="sxs-lookup"><span data-stu-id="66cea-124">IID</span></span><br/>     | <span data-ttu-id="66cea-125">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="66cea-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="66cea-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66cea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66cea-127">**MsiExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="66cea-127">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[<span data-ttu-id="66cea-128">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="66cea-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




