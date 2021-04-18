---
description: L'oggetto ComponentInfo rappresenta informazioni aggiuntive su un componente che può essere ottenuto tramite una chiamata da MsiGetComponentPathEx.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: Oggetto ComponentInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328013"
---
# <a name="componentinfo-object"></a><span data-ttu-id="9e8c0-103">Oggetto ComponentInfo</span><span class="sxs-lookup"><span data-stu-id="9e8c0-103">ComponentInfo object</span></span>

<span data-ttu-id="9e8c0-104">L'oggetto ComponentInfo rappresenta informazioni aggiuntive su un componente che può essere ottenuto tramite una chiamata da MsiGetComponentPathEx.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-104">The ComponentInfo object represents additional details about a component that may be obtained via a call from MsiGetComponentPathEx.</span></span>

<span data-ttu-id="9e8c0-105">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="9e8c0-106">Questo oggetto è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="9e8c0-107">Membri</span><span class="sxs-lookup"><span data-stu-id="9e8c0-107">Members</span></span>

<span data-ttu-id="9e8c0-108">L'oggetto **ComponentInfo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9e8c0-108">The **ComponentInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="9e8c0-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e8c0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e8c0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e8c0-110">Properties</span></span>

<span data-ttu-id="9e8c0-111">L'oggetto **ComponentInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-111">The **ComponentInfo** object has these properties.</span></span>



| <span data-ttu-id="9e8c0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e8c0-112">Property</span></span>                                                        | <span data-ttu-id="9e8c0-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e8c0-113">Description</span></span>                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="9e8c0-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="9e8c0-114">**ComponentCode**</span></span>](componentinfo-componentcode.md)<br/> | <span data-ttu-id="9e8c0-115">Codice del componente in questione.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="9e8c0-116">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="9e8c0-116">**Path**</span></span>](componentinfo-componentcode.md)<br/>          | <span data-ttu-id="9e8c0-117">Percorso del componente.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-117">The path of the component.</span></span><br/>                       |
| [<span data-ttu-id="9e8c0-118">**State**</span><span class="sxs-lookup"><span data-stu-id="9e8c0-118">**State**</span></span>](componentinfo-state.md)<br/>                 | <span data-ttu-id="9e8c0-119">Stato del componente.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-119">The state of the component.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="9e8c0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e8c0-120">Requirements</span></span>



| <span data-ttu-id="9e8c0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e8c0-121">Requirement</span></span> | <span data-ttu-id="9e8c0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9e8c0-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8c0-123">Versione</span><span class="sxs-lookup"><span data-stu-id="9e8c0-123">Version</span></span><br/> | <span data-ttu-id="9e8c0-124">Windows Installer 5,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="9e8c0-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="9e8c0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9e8c0-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9e8c0-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e8c0-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e8c0-127">IID</span><span class="sxs-lookup"><span data-stu-id="9e8c0-127">IID</span></span><br/>     | <span data-ttu-id="9e8c0-128">IID \_ IComponentInfo è definito come 000C1099-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9e8c0-128">IID\_IComponentInfo is defined as 000C1099-0000-0000-C000-000000000046</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="9e8c0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e8c0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e8c0-130">Uso dell'interfaccia di automazione</span><span class="sxs-lookup"><span data-stu-id="9e8c0-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="9e8c0-131">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="9e8c0-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




