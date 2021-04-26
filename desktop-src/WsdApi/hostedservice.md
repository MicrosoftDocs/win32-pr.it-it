---
description: Definisce un servizio da ospitare in una funzione del generatore di host.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: elemento hostedService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96c9f6e010989f4844d93299bb34f1ab8893236
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994788"
---
# <a name="hostedservice-element"></a><span data-ttu-id="2ffcf-103">elemento hostedService</span><span class="sxs-lookup"><span data-stu-id="2ffcf-103">hostedService element</span></span>

<span data-ttu-id="2ffcf-104">Definisce un servizio da ospitare in una funzione del generatore di host.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="2ffcf-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="2ffcf-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="2ffcf-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="2ffcf-106">Attributes</span></span>

<span data-ttu-id="2ffcf-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2ffcf-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2ffcf-108">Child elements</span></span>



| <span data-ttu-id="2ffcf-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="2ffcf-109">Element</span></span>                                     | <span data-ttu-id="2ffcf-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ffcf-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ffcf-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="2ffcf-112">Specifica il nome da utilizzare per il tipo di porta nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="2ffcf-113">Per impostazione predefinita, il nome in codice viene generato dal nome completo del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="2ffcf-114">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="2ffcf-115">Tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="2ffcf-116">**classe proxy**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="2ffcf-117">Nome della classe da generare dalla funzione del generatore.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="2ffcf-118">**SERVICEID**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="2ffcf-119">URI che rappresenta l'identificatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="2ffcf-120">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2ffcf-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="2ffcf-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="2ffcf-121">Parent elements</span></span>



| <span data-ttu-id="2ffcf-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="2ffcf-122">Element</span></span>                         | <span data-ttu-id="2ffcf-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ffcf-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="2ffcf-124">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="2ffcf-125">Specifica del file di output per il generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="2ffcf-126">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2ffcf-126">Element information</span></span>



| <span data-ttu-id="2ffcf-127">Label</span><span class="sxs-lookup"><span data-stu-id="2ffcf-127">Label</span></span> | <span data-ttu-id="2ffcf-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2ffcf-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="2ffcf-129">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ffcf-129">Minimum supported system</span></span><br/> | <span data-ttu-id="2ffcf-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ffcf-130">Windows Vista</span></span> |
| <span data-ttu-id="2ffcf-131">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="2ffcf-131">Can be empty</span></span>                        | <span data-ttu-id="2ffcf-132">No</span><span class="sxs-lookup"><span data-stu-id="2ffcf-132">No</span></span>            |



 

 




