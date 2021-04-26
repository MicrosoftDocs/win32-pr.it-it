---
description: Indica se WsdCodeGen deve provare a contrassegnare automaticamente determinati campi generati come statici.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: Elemento autoStatic
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994928"
---
# <a name="autostatic-element"></a><span data-ttu-id="8e240-103">Elemento autoStatic</span><span class="sxs-lookup"><span data-stu-id="8e240-103">autoStatic element</span></span>

<span data-ttu-id="8e240-104">Indica se WsdCodeGen deve provare a contrassegnare automaticamente determinati campi generati come statici.</span><span class="sxs-lookup"><span data-stu-id="8e240-104">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="8e240-105">Questo comportamento è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8e240-105">This behavior is enabled by default.</span></span>

## <a name="usage"></a><span data-ttu-id="8e240-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8e240-106">Usage</span></span>

``` syntax
<autoStatic/>
```

## <a name="attributes"></a><span data-ttu-id="8e240-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="8e240-107">Attributes</span></span>

<span data-ttu-id="8e240-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="8e240-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8e240-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8e240-109">Child elements</span></span>

<span data-ttu-id="8e240-110">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="8e240-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8e240-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="8e240-111">Parent elements</span></span>



| <span data-ttu-id="8e240-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="8e240-112">Element</span></span>                                     | <span data-ttu-id="8e240-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e240-113">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e240-114">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="8e240-114">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="8e240-115">Elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="8e240-115">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8e240-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e240-116">Remarks</span></span>

<span data-ttu-id="8e240-117">**L'elemento autoStatic** non è obbligatorio e può essere omesso dal file di configurazione XML.</span><span class="sxs-lookup"><span data-stu-id="8e240-117">The **autoStatic** element is not required and may be omitted from the XML configuration file.</span></span> <span data-ttu-id="8e240-118">L'elemento può essere usato per disabilitare il flag dei campi generati come statici o per forzare in modo esplicito il flag di determinati campi generati come statici.</span><span class="sxs-lookup"><span data-stu-id="8e240-118">The element can be used to disable the flagging of generated fields as static or to explicitly force the flagging of certain generated fields as static.</span></span>

<span data-ttu-id="8e240-119">I valori possibili sono 1 (abilitato, predefinito) e 0 (disabilitato).</span><span class="sxs-lookup"><span data-stu-id="8e240-119">Possible values are 1 (enabled, default) and 0 (disabled).</span></span> <span data-ttu-id="8e240-120">**L'abilitazione di autoStatic** può causare problemi di compilazione a seconda del modo in cui il generatore di codice viene indirizzato ai dati di output.</span><span class="sxs-lookup"><span data-stu-id="8e240-120">Enabling **autoStatic** may cause compilation issues depending on how the code generator is directed to output data.</span></span>

## <a name="element-information"></a><span data-ttu-id="8e240-121">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8e240-121">Element information</span></span>



| <span data-ttu-id="8e240-122">Label</span><span class="sxs-lookup"><span data-stu-id="8e240-122">Label</span></span> | <span data-ttu-id="8e240-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8e240-123">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8e240-124">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e240-124">Minimum supported system</span></span><br/> | <span data-ttu-id="8e240-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e240-125">Windows Vista</span></span> |
| <span data-ttu-id="8e240-126">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="8e240-126">Can be empty</span></span>                        | <span data-ttu-id="8e240-127">Sì</span><span class="sxs-lookup"><span data-stu-id="8e240-127">Yes</span></span>           |



 

 




