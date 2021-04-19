---
description: La proprietà ProductInfoFromScript dell'oggetto Installer restituisce il valore dell'attributo specificato archiviato in uno script di annuncio.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Programma di installazione::P proprietà roductInfoFromScript
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332941"
---
# <a name="installerproductinfofromscript-property"></a><span data-ttu-id="a280f-103">Programma di installazione::P proprietà roductInfoFromScript</span><span class="sxs-lookup"><span data-stu-id="a280f-103">Installer::ProductInfoFromScript property</span></span>

<span data-ttu-id="a280f-104">La proprietà **ProductInfoFromScript** dell'oggetto [**Installer**](installer-object.md) restituisce il valore dell'attributo specificato archiviato in uno script di annuncio.</span><span class="sxs-lookup"><span data-stu-id="a280f-104">The **ProductInfoFromScript** property of the [**Installer**](installer-object.md) object returns the value of the specified attribute that is stored in an advertise script.</span></span>

<span data-ttu-id="a280f-105">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="a280f-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a280f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a280f-106">Syntax</span></span>


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a><span data-ttu-id="a280f-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a280f-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="a280f-108">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a280f-108">Error codes</span></span>

<span data-ttu-id="a280f-109">Stringa o valore integer a seconda dell'attributo richiesto.</span><span class="sxs-lookup"><span data-stu-id="a280f-109">A string or integer value depending upon requested attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="a280f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a280f-110">Remarks</span></span>

<span data-ttu-id="a280f-111">La proprietà **ProductInfoFromScript** usa la funzione [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) .</span><span class="sxs-lookup"><span data-stu-id="a280f-111">The **ProductInfoFromScript** property uses the [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) function.</span></span>

## <a name="examples"></a><span data-ttu-id="a280f-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="a280f-112">Examples</span></span>

<span data-ttu-id="a280f-113">Lo script di esempio seguente illustra l'uso della proprietà **ProductInfoFromScript** .</span><span class="sxs-lookup"><span data-stu-id="a280f-113">The following sample script demonstrates the use of the **ProductInfoFromScript** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
```



## <a name="requirements"></a><span data-ttu-id="a280f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a280f-114">Requirements</span></span>



| <span data-ttu-id="a280f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a280f-115">Requirement</span></span> | <span data-ttu-id="a280f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a280f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a280f-117">Versione</span><span class="sxs-lookup"><span data-stu-id="a280f-117">Version</span></span><br/> | <span data-ttu-id="a280f-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a280f-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a280f-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a280f-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a280f-120">Windows Installer 4,5 in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="a280f-120">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="a280f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a280f-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a280f-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a280f-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="a280f-123">IID</span><span class="sxs-lookup"><span data-stu-id="a280f-123">IID</span></span><br/>     | <span data-ttu-id="a280f-124">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a280f-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="a280f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a280f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a280f-126">**Programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="a280f-126">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="a280f-127">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="a280f-127">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




