---
description: Definisce un servizio da ospitare in una funzione del generatore host.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: elemento servizio ospitato
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880634"
---
# <a name="hostedservice-element"></a><span data-ttu-id="a5f4a-103">elemento servizio ospitato</span><span class="sxs-lookup"><span data-stu-id="a5f4a-103">hostedService element</span></span>

<span data-ttu-id="a5f4a-104">Definisce un servizio da ospitare in una funzione del generatore host.</span><span class="sxs-lookup"><span data-stu-id="a5f4a-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="a5f4a-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a5f4a-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="a5f4a-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="a5f4a-106">Attributes</span></span>

<span data-ttu-id="a5f4a-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="a5f4a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a5f4a-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a5f4a-108">Child elements</span></span>



| <span data-ttu-id="a5f4a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a5f4a-109">Element</span></span>                                     | <span data-ttu-id="a5f4a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5f4a-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5f4a-111">**codeName**</span><span class="sxs-lookup"><span data-stu-id="a5f4a-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="a5f4a-112">Specifica il nome da utilizzare per il tipo di porta nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="a5f4a-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="a5f4a-113">Per impostazione predefinita, il nome del codice viene generato dal nome completo del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="a5f4a-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="a5f4a-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="a5f4a-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="a5f4a-115">Tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="a5f4a-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="a5f4a-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="a5f4a-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="a5f4a-117">Nome della classe da generare dalla funzione del generatore.</span><span class="sxs-lookup"><span data-stu-id="a5f4a-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="a5f4a-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="a5f4a-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="a5f4a-119">URI che rappresenta l'identificatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="a5f4a-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="a5f4a-120">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a5f4a-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="a5f4a-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a5f4a-121">Parent elements</span></span>



| <span data-ttu-id="a5f4a-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="a5f4a-122">Element</span></span>                         | <span data-ttu-id="a5f4a-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5f4a-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="a5f4a-124">**file**</span><span class="sxs-lookup"><span data-stu-id="a5f4a-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="a5f4a-125">Specifica del file di output per il generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="a5f4a-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="a5f4a-126">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a5f4a-126">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="a5f4a-127">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5f4a-127">Minimum supported system</span></span><br/> | <span data-ttu-id="a5f4a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5f4a-128">Windows Vista</span></span> |
| <span data-ttu-id="a5f4a-129">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="a5f4a-129">Can be empty</span></span>                        | <span data-ttu-id="a5f4a-130">No</span><span class="sxs-lookup"><span data-stu-id="a5f4a-130">No</span></span>            |



 

 




