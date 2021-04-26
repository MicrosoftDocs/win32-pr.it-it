---
description: Specifica l'identificatore hardware PnP-X del servizio.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996528"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="2aa1f-103">Elemento PnPXHardwareId</span><span class="sxs-lookup"><span data-stu-id="2aa1f-103">PnPXHardwareId element</span></span>

<span data-ttu-id="2aa1f-104">Specifica l'identificatore hardware PnP-X del servizio.</span><span class="sxs-lookup"><span data-stu-id="2aa1f-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="2aa1f-105">PnP corrisponde a questo elemento con le descrizioni hardware fornite nella sezione \[ PnpxDevice \] del file INF del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2aa1f-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="2aa1f-106">In base a queste informazioni, il servizio PnP seleziona e carica il driver di dispositivo più appropriato.</span><span class="sxs-lookup"><span data-stu-id="2aa1f-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="2aa1f-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="2aa1f-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="2aa1f-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="2aa1f-108">Attributes</span></span>

<span data-ttu-id="2aa1f-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="2aa1f-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2aa1f-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2aa1f-110">Child elements</span></span>

<span data-ttu-id="2aa1f-111">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="2aa1f-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2aa1f-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="2aa1f-112">Parent elements</span></span>



| <span data-ttu-id="2aa1f-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="2aa1f-113">Element</span></span>                             | <span data-ttu-id="2aa1f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aa1f-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aa1f-115">**Ospitato da**</span><span class="sxs-lookup"><span data-stu-id="2aa1f-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="2aa1f-116">Definisce gli elementi per i servizi definiti dall'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="2aa1f-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2aa1f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2aa1f-117">Remarks</span></span>

<span data-ttu-id="2aa1f-118">Per specificare più ID hardware, separare gli identificatori con uno spazio, ad esempio "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".</span><span class="sxs-lookup"><span data-stu-id="2aa1f-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="2aa1f-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2aa1f-119">Element information</span></span>



| <span data-ttu-id="2aa1f-120">Label</span><span class="sxs-lookup"><span data-stu-id="2aa1f-120">Label</span></span> | <span data-ttu-id="2aa1f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2aa1f-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="2aa1f-122">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2aa1f-122">Minimum supported system</span></span><br/> | <span data-ttu-id="2aa1f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2aa1f-123">Windows Vista</span></span> |
| <span data-ttu-id="2aa1f-124">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="2aa1f-124">Can be empty</span></span>                        | <span data-ttu-id="2aa1f-125">Sì</span><span class="sxs-lookup"><span data-stu-id="2aa1f-125">Yes</span></span>           |



 

 




