---
description: L'oggetto Component rappresenta un'istanza univoca di un componente disponibile per l'enumerazione.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Oggetto Component
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328012"
---
# <a name="component-object"></a><span data-ttu-id="a3367-103">Oggetto Component</span><span class="sxs-lookup"><span data-stu-id="a3367-103">Component object</span></span>

<span data-ttu-id="a3367-104">L'oggetto Component rappresenta un'istanza univoca di un componente disponibile per l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="a3367-104">The Component object represents a unique instance of a component that is available for enumeration.</span></span>

<span data-ttu-id="a3367-105">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="a3367-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="a3367-106">Questo oggetto è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="a3367-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="a3367-107">Membri</span><span class="sxs-lookup"><span data-stu-id="a3367-107">Members</span></span>

<span data-ttu-id="a3367-108">L'oggetto **Component** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a3367-108">The **Component** object has these types of members:</span></span>

-   [<span data-ttu-id="a3367-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a3367-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3367-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a3367-110">Properties</span></span>

<span data-ttu-id="a3367-111">L'oggetto **Component** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a3367-111">The **Component** object has these properties.</span></span>



| <span data-ttu-id="a3367-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a3367-112">Property</span></span>                                                    | <span data-ttu-id="a3367-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3367-113">Description</span></span>                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3367-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="a3367-114">**ComponentCode**</span></span>](component-componentcode.md)<br/> | <span data-ttu-id="a3367-115">Codice del componente in questione.</span><span class="sxs-lookup"><span data-stu-id="a3367-115">The component code of the component in question.</span></span><br/>                               |
| [<span data-ttu-id="a3367-116">**Context**</span><span class="sxs-lookup"><span data-stu-id="a3367-116">**Context**</span></span>](component-context.md)<br/>             | <span data-ttu-id="a3367-117">Contesto che è stato determinato come applicabile al componente in questione.</span><span class="sxs-lookup"><span data-stu-id="a3367-117">The context that was determined to be applicable to the component in question.</span></span><br/> |
| [<span data-ttu-id="a3367-118">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="a3367-118">**UserSID**</span></span>](component-usersid.md)<br/>             | <span data-ttu-id="a3367-119">SID utente per il componente enumerato.</span><span class="sxs-lookup"><span data-stu-id="a3367-119">The user SID for the enumerated component.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="a3367-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3367-120">Requirements</span></span>



| <span data-ttu-id="a3367-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3367-121">Requirement</span></span> | <span data-ttu-id="a3367-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a3367-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3367-123">Versione</span><span class="sxs-lookup"><span data-stu-id="a3367-123">Version</span></span><br/> | <span data-ttu-id="a3367-124">Windows Installer 5,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="a3367-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="a3367-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a3367-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3367-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3367-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="a3367-127">IID</span><span class="sxs-lookup"><span data-stu-id="a3367-127">IID</span></span><br/>     | <span data-ttu-id="a3367-128">IID \_ IComponent è definito come 000C1097-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a3367-128">IID\_IComponent is defined as 000C1097-0000-0000-C000-000000000046</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="a3367-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3367-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3367-130">Uso dell'interfaccia di automazione</span><span class="sxs-lookup"><span data-stu-id="a3367-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="a3367-131">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a3367-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




