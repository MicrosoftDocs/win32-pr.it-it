---
description: Restituisce un oggetto elenco che elenca i prodotti che utilizzano un componente installato specificato.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Proprietà Installer. ClientsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329476"
---
# <a name="installerclientsex-property"></a><span data-ttu-id="7c3c6-103">Proprietà Installer. ClientsEx</span><span class="sxs-lookup"><span data-stu-id="7c3c6-103">Installer.ClientsEx property</span></span>

<span data-ttu-id="7c3c6-104">Questa proprietà restituisce un [**oggetto elenco di elementi**](recordlist-object.md) che elenca i prodotti che utilizzano un componente installato specificato.</span><span class="sxs-lookup"><span data-stu-id="7c3c6-104">This property returns a [**RecordList**](recordlist-object.md) object that lists products that use a specified installed component.</span></span> <span data-ttu-id="7c3c6-105">Questa proprietà chiama [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span><span class="sxs-lookup"><span data-stu-id="7c3c6-105">This property calls [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span></span>

<span data-ttu-id="7c3c6-106">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="7c3c6-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="7c3c6-107">Questa proprietà è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="7c3c6-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="7c3c6-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7c3c6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c3c6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c3c6-109">Syntax</span></span>


```JScript
propVal = Installer.ClientsEx
```



## <a name="property-value"></a><span data-ttu-id="7c3c6-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7c3c6-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3c6-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c3c6-111">Requirements</span></span>



| <span data-ttu-id="7c3c6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c3c6-112">Requirement</span></span> | <span data-ttu-id="7c3c6-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7c3c6-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3c6-114">Versione</span><span class="sxs-lookup"><span data-stu-id="7c3c6-114">Version</span></span><br/> | <span data-ttu-id="7c3c6-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c3c6-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="7c3c6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7c3c6-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c3c6-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c3c6-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="7c3c6-118">IID</span><span class="sxs-lookup"><span data-stu-id="7c3c6-118">IID</span></span><br/>     | <span data-ttu-id="7c3c6-119">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7c3c6-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="7c3c6-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c3c6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c3c6-121">**MsiEnumClientsEx**</span><span class="sxs-lookup"><span data-stu-id="7c3c6-121">**MsiEnumClientsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




