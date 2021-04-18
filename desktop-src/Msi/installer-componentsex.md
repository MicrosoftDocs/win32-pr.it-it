---
description: Restituisce un oggetto elenco che elenca i componenti installati.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Proprietà Installer. ComponentsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a48261a924280999d2b8329d635d4115de35753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330496"
---
# <a name="installercomponentsex-property"></a><span data-ttu-id="30dae-103">Proprietà Installer. ComponentsEx</span><span class="sxs-lookup"><span data-stu-id="30dae-103">Installer.ComponentsEx property</span></span>

<span data-ttu-id="30dae-104">Questa proprietà [**restituisce un oggetto elenco che**](recordlist-object.md) elenca i componenti installati.</span><span class="sxs-lookup"><span data-stu-id="30dae-104">This property returns a [**RecordList**](recordlist-object.md) object that lists installed components.</span></span> <span data-ttu-id="30dae-105">Questa proprietà chiama [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span><span class="sxs-lookup"><span data-stu-id="30dae-105">This property calls [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span></span>

<span data-ttu-id="30dae-106">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="30dae-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="30dae-107">Questa proprietà è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="30dae-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="30dae-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="30dae-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30dae-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30dae-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentsEx
```



## <a name="property-value"></a><span data-ttu-id="30dae-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="30dae-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="30dae-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30dae-111">Requirements</span></span>



| <span data-ttu-id="30dae-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="30dae-112">Requirement</span></span> | <span data-ttu-id="30dae-113">Valore</span><span class="sxs-lookup"><span data-stu-id="30dae-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30dae-114">Versione</span><span class="sxs-lookup"><span data-stu-id="30dae-114">Version</span></span><br/> | <span data-ttu-id="30dae-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="30dae-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="30dae-116">DLL</span><span class="sxs-lookup"><span data-stu-id="30dae-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="30dae-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30dae-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="30dae-118">IID</span><span class="sxs-lookup"><span data-stu-id="30dae-118">IID</span></span><br/>     | <span data-ttu-id="30dae-119">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="30dae-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="30dae-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30dae-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30dae-121">**MsiEnumComponentsEx**</span><span class="sxs-lookup"><span data-stu-id="30dae-121">**MsiEnumComponentsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




