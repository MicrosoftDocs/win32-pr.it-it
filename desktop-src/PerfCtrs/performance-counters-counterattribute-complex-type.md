---
description: Definisce un attributo di un contatore che specifica la modalità di visualizzazione dei dati del contatore in un'applicazione consumer.
ms.assetid: 3749501b-4f3e-42e5-b1d5-2700b6d4a48a
title: Tipo complesso counterAttribute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1b34a3a802f0f7c79815956c3a364522ce0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312134"
---
# <a name="counterattribute-complex-type"></a><span data-ttu-id="ff959-103">Tipo complesso counterAttribute</span><span class="sxs-lookup"><span data-stu-id="ff959-103">counterAttribute Complex Type</span></span>

<span data-ttu-id="ff959-104">Definisce un attributo di un contatore che specifica la modalità di visualizzazione dei dati del contatore in un'applicazione consumer.</span><span class="sxs-lookup"><span data-stu-id="ff959-104">Defines an attribute of a counter that specifies how the counter data is displayed in a consumer application.</span></span>

``` syntax
<xs:complexType name="counterAttribute">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                use="required"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="xs:string"
                    >
                        <xs:enumeration
                            value="reference"
                         />
                        <xs:enumeration
                            value="noDisplay"
                         />
                        <xs:enumeration
                            value="noDigitGrouping"
                         />
                        <xs:enumeration
                            value="displayAsHex"
                         />
                        <xs:enumeration
                            value="displayAsReal"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="ff959-105">Attributi</span><span class="sxs-lookup"><span data-stu-id="ff959-105">Attributes</span></span>



| <span data-ttu-id="ff959-106">Nome</span><span class="sxs-lookup"><span data-stu-id="ff959-106">Name</span></span> | <span data-ttu-id="ff959-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff959-107">Type</span></span> | <span data-ttu-id="ff959-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff959-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff959-109">name</span><span class="sxs-lookup"><span data-stu-id="ff959-109">name</span></span> |      | <span data-ttu-id="ff959-110">Nome dell'attributo di visualizzazione da applicare.</span><span class="sxs-lookup"><span data-stu-id="ff959-110">The name of the display attribute to apply.</span></span> <span data-ttu-id="ff959-111">È possibile specificare uno dei nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff959-111">You can specify one of the following names:</span></span><br/> <dl> <span data-ttu-id="ff959-112"><dt><span id="reference"></span><span id="REFERENCE"></span>riferimento</dt></span><span class="sxs-lookup"><span data-stu-id="ff959-112"><dt><span id="reference"></span><span id="REFERENCE"></span>reference</dt></span></span> <dd> <span data-ttu-id="ff959-113">Recuperare il valore del contatore per riferimento anziché per valore.</span><span class="sxs-lookup"><span data-stu-id="ff959-113">Retrieve the value of the counter by reference as opposed to by value.</span></span><br/> </dd> <span data-ttu-id="ff959-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>nodisplay</dt></span><span class="sxs-lookup"><span data-stu-id="ff959-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>noDisplay</dt></span></span> <dd> <span data-ttu-id="ff959-115">Non visualizzare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="ff959-115">Do not display the counter value.</span></span> <span data-ttu-id="ff959-116">In genere, si utilizza questo attributo se i dati del contatore vengono utilizzati come input per il calcolo del valore di un altro contatore.</span><span class="sxs-lookup"><span data-stu-id="ff959-116">Typically, you use this attribute if the counter's data is used as input for calculating another counter's value.</span></span> <br/> </dd> <span data-ttu-id="ff959-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt></span><span class="sxs-lookup"><span data-stu-id="ff959-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt></span></span> <dd> <span data-ttu-id="ff959-118">Le applicazioni consumer o di monitoraggio non devono usare separatori di cifre durante la visualizzazione dei valori dei contatori.</span><span class="sxs-lookup"><span data-stu-id="ff959-118">Consumer or monitoring applications should not use digit separators when displaying counter values.</span></span> <br/> </dd> <span data-ttu-id="ff959-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt></span><span class="sxs-lookup"><span data-stu-id="ff959-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt></span></span> <dd> <span data-ttu-id="ff959-120">Le applicazioni consumer o di monitoraggio devono visualizzare il valore del contatore come valore esadecimale anziché come valore intero predefinito.</span><span class="sxs-lookup"><span data-stu-id="ff959-120">Consumer or monitoring applications should display the counter value as a hexadecimal, instead of the default integer value.</span></span><br/> </dd> <span data-ttu-id="ff959-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt></span><span class="sxs-lookup"><span data-stu-id="ff959-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt></span></span> <dd> <span data-ttu-id="ff959-122">Le applicazioni consumer o di monitoraggio devono visualizzare il valore del contatore come numero reale, anziché il valore intero predefinito.</span><span class="sxs-lookup"><span data-stu-id="ff959-122">Consumer or monitoring applications should display the counter value as a real number, instead of the default integer value.</span></span> <br/> </dd> </dl> |



## <a name="requirements"></a><span data-ttu-id="ff959-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff959-123">Requirements</span></span>



| <span data-ttu-id="ff959-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff959-124">Requirement</span></span> | <span data-ttu-id="ff959-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ff959-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff959-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff959-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ff959-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff959-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff959-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff959-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ff959-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff959-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




