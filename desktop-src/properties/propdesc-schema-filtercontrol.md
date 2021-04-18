---
description: Specifica il controllo da utilizzare nel menu del filtro di intestazione.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c0de28eaa349b9a999ba39c1bad47aa01d43d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310124"
---
# <a name="filtercontrol"></a><span data-ttu-id="9558c-103">filterControl</span><span class="sxs-lookup"><span data-stu-id="9558c-103">filterControl</span></span>

<span data-ttu-id="9558c-104">Specifica il controllo da utilizzare nel menu del filtro di intestazione.</span><span class="sxs-lookup"><span data-stu-id="9558c-104">Specifies what control to use in the header filter menu.</span></span> <span data-ttu-id="9558c-105">Deve essere presente un solo elemento [filterControl]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9558c-105">There should be only one [filterControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="9558c-106">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="9558c-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="9558c-107">Se non viene specificato alcun elemento [filterControl]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="9558c-107">If no [filterControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9558c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9558c-108">Syntax</span></span>


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="9558c-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9558c-109">Element Information</span></span>



| <span data-ttu-id="9558c-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="9558c-110">Parent Element</span></span>                                   | <span data-ttu-id="9558c-111">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="9558c-111">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="9558c-112">displayInfo</span><span class="sxs-lookup"><span data-stu-id="9558c-112">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="9558c-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="9558c-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="9558c-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="9558c-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9558c-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="9558c-115">Attribute</span></span></th>
<th><span data-ttu-id="9558c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9558c-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9558c-117">controllo</span><span class="sxs-lookup"><span data-stu-id="9558c-117">control</span></span></td>
<td><span data-ttu-id="9558c-118">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="9558c-118">Public.</span></span> <span data-ttu-id="9558c-119">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9558c-119">Optional.</span></span> <span data-ttu-id="9558c-120">Il valore predefinito è &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="9558c-120">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="9558c-121">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9558c-121">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9558c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9558c-122">Value</span></span></th>
<th><span data-ttu-id="9558c-123">Significato</span><span class="sxs-lookup"><span data-stu-id="9558c-123">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9558c-124">Predefinito</span><span class="sxs-lookup"><span data-stu-id="9558c-124">Default</span></span></td>
<td><span data-ttu-id="9558c-125">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="9558c-125">Default.</span></span> <span data-ttu-id="9558c-126">Usa il controllo predefinito, in base all' <typeInfo type=&quot;&quot;> attributo.</span><span class="sxs-lookup"><span data-stu-id="9558c-126">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="9558c-127">Il tipo predefinito è &quot; DateTime &quot; e il controllo predefinito è &quot; Calendar &quot; .</span><span class="sxs-lookup"><span data-stu-id="9558c-127">The default type is &quot;DateTime&quot; and the default control is &quot;Calendar&quot;.</span></span> <span data-ttu-id="9558c-128">Qualsiasi altro tipo non produce alcun controllo filtro speciale.</span><span class="sxs-lookup"><span data-stu-id="9558c-128">Any other type results in no special filter control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9558c-129">Calendario</span><span class="sxs-lookup"><span data-stu-id="9558c-129">Calendar</span></span></td>
<td><span data-ttu-id="9558c-130">Usa il controllo Calendar.</span><span class="sxs-lookup"><span data-stu-id="9558c-130">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9558c-131">Classificazione</span><span class="sxs-lookup"><span data-stu-id="9558c-131">Rating</span></span></td>
<td><span data-ttu-id="9558c-132">Usa il controllo della classificazione a 5 stelle.</span><span class="sxs-lookup"><span data-stu-id="9558c-132">Uses the 5-star rating control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
