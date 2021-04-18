---
description: L'oggetto client rappresenta una relazione tra un componente e un prodotto client.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Oggetto client
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328438"
---
# <a name="client-object"></a><span data-ttu-id="c528e-103">Oggetto client</span><span class="sxs-lookup"><span data-stu-id="c528e-103">Client object</span></span>

<span data-ttu-id="c528e-104">L'oggetto client rappresenta una relazione tra un componente e un prodotto client.</span><span class="sxs-lookup"><span data-stu-id="c528e-104">The Client object represents a relationship between a component and client product.</span></span>

<span data-ttu-id="c528e-105">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="c528e-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="c528e-106">Questo oggetto è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="c528e-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="c528e-107">Membri</span><span class="sxs-lookup"><span data-stu-id="c528e-107">Members</span></span>

<span data-ttu-id="c528e-108">L'oggetto **client** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c528e-108">The **Client** object has these types of members:</span></span>

-   [<span data-ttu-id="c528e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c528e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c528e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c528e-110">Properties</span></span>

<span data-ttu-id="c528e-111">L'oggetto **client** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c528e-111">The **Client** object has these properties.</span></span>



| <span data-ttu-id="c528e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c528e-112">Property</span></span>                                                 | <span data-ttu-id="c528e-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c528e-113">Description</span></span>                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="c528e-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="c528e-114">**ComponentCode**</span></span>](client-componentcode.md)<br/> | <span data-ttu-id="c528e-115">Codice del componente in questione.</span><span class="sxs-lookup"><span data-stu-id="c528e-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="c528e-116">**Context**</span><span class="sxs-lookup"><span data-stu-id="c528e-116">**Context**</span></span>](client-context.md)<br/>             | <span data-ttu-id="c528e-117">Contesto del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c528e-117">The context of the product.</span></span><br/>                      |
| [<span data-ttu-id="c528e-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="c528e-118">**ProductCode**</span></span>](client-productcode.md)<br/>     | <span data-ttu-id="c528e-119">Prodotto client del componente in questione.</span><span class="sxs-lookup"><span data-stu-id="c528e-119">The client product of the component in question.</span></span><br/> |
| [<span data-ttu-id="c528e-120">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="c528e-120">**UserSID**</span></span>](client-usersid.md)<br/>             | <span data-ttu-id="c528e-121">SID utente per il componente.</span><span class="sxs-lookup"><span data-stu-id="c528e-121">The user SID for the component.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="c528e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c528e-122">Requirements</span></span>



| <span data-ttu-id="c528e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c528e-123">Requirement</span></span> | <span data-ttu-id="c528e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c528e-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c528e-125">Versione</span><span class="sxs-lookup"><span data-stu-id="c528e-125">Version</span></span><br/> | <span data-ttu-id="c528e-126">Windows Installer 5,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c528e-126">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="c528e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c528e-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="c528e-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c528e-128"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="c528e-129">IID</span><span class="sxs-lookup"><span data-stu-id="c528e-129">IID</span></span><br/>     | <span data-ttu-id="c528e-130">IID \_ IClient è definito come 000C1098-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c528e-130">IID\_IClient is defined as 000C1098-0000-0000-C000-000000000046</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="c528e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c528e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c528e-132">Uso dell'interfaccia di automazione</span><span class="sxs-lookup"><span data-stu-id="c528e-132">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="c528e-133">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c528e-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




