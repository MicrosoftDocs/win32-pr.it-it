---
description: La proprietà ProductElevated dell'oggetto Installer restituisce true se il prodotto è gestito o false se il prodotto non è gestito.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Programma di installazione::P proprietà roductElevated
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332947"
---
# <a name="installerproductelevated-property"></a><span data-ttu-id="5e47c-103">Programma di installazione::P proprietà roductElevated</span><span class="sxs-lookup"><span data-stu-id="5e47c-103">Installer::ProductElevated property</span></span>

<span data-ttu-id="5e47c-104">La proprietà **ProductElevated** dell'oggetto [**Installer**](installer-object.md) restituisce true se il prodotto è gestito o false se il prodotto non è gestito.</span><span class="sxs-lookup"><span data-stu-id="5e47c-104">The **ProductElevated** property of the [**Installer**](installer-object.md) object returns True if the product is managed or False if the product is not managed.</span></span>

<span data-ttu-id="5e47c-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5e47c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e47c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e47c-106">Syntax</span></span>


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a><span data-ttu-id="5e47c-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5e47c-107">Property value</span></span>

<span data-ttu-id="5e47c-108">GUID completo del codice prodotto del prodotto.</span><span class="sxs-lookup"><span data-stu-id="5e47c-108">The full product code GUID of the product.</span></span> <span data-ttu-id="5e47c-109">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e47c-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e47c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e47c-110">Remarks</span></span>

<span data-ttu-id="5e47c-111">La proprietà **ProductElevated** usa la funzione [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) .</span><span class="sxs-lookup"><span data-stu-id="5e47c-111">The **ProductElevated** property uses the [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) function.</span></span> <span data-ttu-id="5e47c-112">Il ritorno della proprietà non prende in considerazione il criterio [AlwaysInstallElevated](alwaysinstallelevated.md) .</span><span class="sxs-lookup"><span data-stu-id="5e47c-112">The return of the property does not take into account the [AlwaysInstallElevated](alwaysinstallelevated.md) policy.</span></span>

## <a name="examples"></a><span data-ttu-id="5e47c-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="5e47c-113">Examples</span></span>

<span data-ttu-id="5e47c-114">Lo script di esempio seguente illustra l'uso della proprietà **ProductElevated** .</span><span class="sxs-lookup"><span data-stu-id="5e47c-114">The following sample script demonstrates the use of the **ProductElevated** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a><span data-ttu-id="5e47c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e47c-115">Requirements</span></span>



| <span data-ttu-id="5e47c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e47c-116">Requirement</span></span> | <span data-ttu-id="5e47c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5e47c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e47c-118">Versione</span><span class="sxs-lookup"><span data-stu-id="5e47c-118">Version</span></span><br/> | <span data-ttu-id="5e47c-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e47c-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5e47c-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5e47c-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5e47c-121">Windows Installer 4,5 in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="5e47c-121">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="5e47c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5e47c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5e47c-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e47c-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="5e47c-124">IID</span><span class="sxs-lookup"><span data-stu-id="5e47c-124">IID</span></span><br/>     | <span data-ttu-id="5e47c-125">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5e47c-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="5e47c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e47c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e47c-127">**Programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="5e47c-127">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="5e47c-128">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="5e47c-128">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




