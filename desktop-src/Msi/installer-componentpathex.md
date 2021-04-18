---
description: Restituisce un oggetto di record che fornisce il percorso completo di un componente installato specificato.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Proprietà Installer. ComponentPathEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329025"
---
# <a name="installercomponentpathex-property"></a><span data-ttu-id="63347-103">Proprietà Installer. ComponentPathEx</span><span class="sxs-lookup"><span data-stu-id="63347-103">Installer.ComponentPathEx property</span></span>

<span data-ttu-id="63347-104">Questa proprietà restituisce un oggetto di [**record**](recordlist-object.md) che fornisce il percorso completo di un componente installato specificato.</span><span class="sxs-lookup"><span data-stu-id="63347-104">This property returns a [**RecordList**](recordlist-object.md) object that gives the full path of a specified installed component.</span></span> <span data-ttu-id="63347-105">Questa proprietà chiama [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span><span class="sxs-lookup"><span data-stu-id="63347-105">This property calls [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span></span>

<span data-ttu-id="63347-106">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="63347-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="63347-107">Questa proprietà è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="63347-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="63347-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="63347-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63347-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63347-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a><span data-ttu-id="63347-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="63347-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="63347-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63347-111">Requirements</span></span>



| <span data-ttu-id="63347-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="63347-112">Requirement</span></span> | <span data-ttu-id="63347-113">Valore</span><span class="sxs-lookup"><span data-stu-id="63347-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63347-114">Versione</span><span class="sxs-lookup"><span data-stu-id="63347-114">Version</span></span><br/> | <span data-ttu-id="63347-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="63347-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="63347-116">DLL</span><span class="sxs-lookup"><span data-stu-id="63347-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="63347-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63347-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="63347-118">IID</span><span class="sxs-lookup"><span data-stu-id="63347-118">IID</span></span><br/>     | <span data-ttu-id="63347-119">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="63347-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="63347-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63347-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63347-121">**MsiGetComponentPathEx**</span><span class="sxs-lookup"><span data-stu-id="63347-121">**MsiGetComponentPathEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




