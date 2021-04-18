---
description: Utilizzato per assegnare il testo enumerato a valori discreti.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312551"
---
# <a name="enum"></a><span data-ttu-id="fd788-103">enum</span><span class="sxs-lookup"><span data-stu-id="fd788-103">enum</span></span>

<span data-ttu-id="fd788-104">Utilizzato per assegnare il testo enumerato a valori discreti.</span><span class="sxs-lookup"><span data-stu-id="fd788-104">Used to assign enumerated text to discrete values.</span></span> <span data-ttu-id="fd788-105">In [enumeratedList](./propdesc-schema-enumeratedlist.md)è possibile che esista un numero qualsiasi di questi elementi.</span><span class="sxs-lookup"><span data-stu-id="fd788-105">Any number of these elements may exist under an [enumeratedList](./propdesc-schema-enumeratedlist.md).</span></span> <span data-ttu-id="fd788-106">A livello di codice, questi sono rappresentati come oggetti IPropertyEnumType, il cui metodo [**IPropertyEnumType:: GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) restituisce PET \_ DISCRETEVALUE.</span><span class="sxs-lookup"><span data-stu-id="fd788-106">Programmatically, these are represented as IPropertyEnumType objects, whose [**IPropertyEnumType::GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) method returns PET\_DISCRETEVALUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd788-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd788-107">Syntax</span></span>


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="fd788-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fd788-108">Element Information</span></span>



| <span data-ttu-id="fd788-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="fd788-109">Parent Element</span></span>                                         | <span data-ttu-id="fd788-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fd788-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="fd788-111">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="fd788-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="fd788-112">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fd788-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="fd788-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="fd788-113">Attributes</span></span>



| <span data-ttu-id="fd788-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="fd788-114">Attribute</span></span> | <span data-ttu-id="fd788-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd788-115">Description</span></span>                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd788-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fd788-116">value</span></span>     | <span data-ttu-id="fd788-117">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="fd788-117">Public.</span></span> <span data-ttu-id="fd788-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fd788-118">Required.</span></span> <span data-ttu-id="fd788-119">Valore discreto (stringa o numero) a cui assegnare il testo enumerato.</span><span class="sxs-lookup"><span data-stu-id="fd788-119">The discrete value (string or number) to be assigned enumerated text to.</span></span>                                                                                                                           |
| <span data-ttu-id="fd788-120">text</span><span class="sxs-lookup"><span data-stu-id="fd788-120">text</span></span>      | <span data-ttu-id="fd788-121">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="fd788-121">Public.</span></span> <span data-ttu-id="fd788-122">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fd788-122">Required.</span></span> <span data-ttu-id="fd788-123">Testo utilizzato per visualizzare il valore enumerato.</span><span class="sxs-lookup"><span data-stu-id="fd788-123">The text used to display the enumerated value.</span></span> <span data-ttu-id="fd788-124">La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto a una stringa di visualizzazione. utilizzare la stringa di visualizzazione indiretta in modo che possa essere localizzata.</span><span class="sxs-lookup"><span data-stu-id="fd788-124">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span> |
| <span data-ttu-id="fd788-125">tasti di scelta</span><span class="sxs-lookup"><span data-stu-id="fd788-125">mnemonics</span></span> | <span data-ttu-id="fd788-126">**Windows 7 e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="fd788-126">**Windows 7 and later.**</span></span> <span data-ttu-id="fd788-127">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="fd788-127">Public.</span></span> <span data-ttu-id="fd788-128">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fd788-128">Optional.</span></span> <span data-ttu-id="fd788-129">Elenco di valori mnemonico che possono essere usati per fare riferimento alla proprietà nelle query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="fd788-129">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="fd788-130">L'elenco è delimitato dal carattere " \| ".</span><span class="sxs-lookup"><span data-stu-id="fd788-130">The list is delimited with the '\|' character.</span></span>                                     |



 

 

 
