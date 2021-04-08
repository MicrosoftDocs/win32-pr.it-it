---
title: Ribbon. HelpButton, proprietà
description: Rappresenta un contenitore per il pulsante della guida.
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Barra multifunzione di Windows della proprietà Ribbon. HelpButton
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742295"
---
# <a name="ribbonhelpbutton-property"></a><span data-ttu-id="9b610-104">Ribbon. HelpButton, proprietà</span><span class="sxs-lookup"><span data-stu-id="9b610-104">Ribbon.HelpButton property</span></span>

<span data-ttu-id="9b610-105">Rappresenta un contenitore per il [pulsante della Guida](windowsribbon-controls-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="9b610-105">Represents a container for the [Help Button](windowsribbon-controls-helpbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="9b610-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="9b610-106">Usage</span></span>

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a><span data-ttu-id="9b610-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="9b610-107">Attributes</span></span>

<span data-ttu-id="9b610-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="9b610-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9b610-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="9b610-109">Child elements</span></span>



| <span data-ttu-id="9b610-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="9b610-110">Element</span></span>                                                           | <span data-ttu-id="9b610-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b610-111">Description</span></span>                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="9b610-112">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="9b610-112">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)<br/> | <span data-ttu-id="9b610-113">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="9b610-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="9b610-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="9b610-114">Parent elements</span></span>



| <span data-ttu-id="9b610-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="9b610-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="9b610-116">**Barra multifunzione**</span><span class="sxs-lookup"><span data-stu-id="9b610-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9b610-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b610-117">Remarks</span></span>

<span data-ttu-id="9b610-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9b610-118">Optional.</span></span>

<span data-ttu-id="9b610-119">Può essere presente al massimo una volta per ogni [**barra multifunzione**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="9b610-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9b610-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="9b610-120">Examples</span></span>

<span data-ttu-id="9b610-121">Nell'esempio seguente viene illustrato il markup di base necessario per implementare un pulsante della guida della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="9b610-121">The following example demonstrates the basic markup that is required to implement a Ribbon Help button.</span></span>

<span data-ttu-id="9b610-122">Questa sezione di codice mostra la dichiarazione del comando **Ribbon. HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="9b610-122">This section of code shows the **Ribbon.HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="9b610-123">Questa sezione di codice mostra la dichiarazione di controllo **Ribbon. HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="9b610-123">This section of code shows the **Ribbon.HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a><span data-ttu-id="9b610-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b610-124">Requirements</span></span>



| <span data-ttu-id="9b610-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b610-125">Requirement</span></span> | <span data-ttu-id="9b610-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9b610-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9b610-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b610-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9b610-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9b610-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9b610-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b610-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9b610-130">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b610-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





