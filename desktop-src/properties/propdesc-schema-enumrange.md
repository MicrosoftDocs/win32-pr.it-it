---
description: Assegna il testo di enumerazione a un intervallo di valori. Ogni elemento enumRange specifica un valore minimo e si estende fino al valore minimo dell'elemento successivo o fino a quando non sono presenti altri elementi enumRange.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967111"
---
# <a name="enumrange"></a><span data-ttu-id="215e5-104">enumRange</span><span class="sxs-lookup"><span data-stu-id="215e5-104">enumRange</span></span>

<span data-ttu-id="215e5-105">Assegna il testo di enumerazione a un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="215e5-105">Assigns enumeration text to a range of values.</span></span> <span data-ttu-id="215e5-106">Ogni elemento [enumRange]() specifica un valore minimo e si estende fino al valore minimo dell'elemento successivo o fino a quando non sono presenti altri elementi enumRange.</span><span class="sxs-lookup"><span data-stu-id="215e5-106">Each [enumRange]() element specifies a minimum value, and extends until the next element minimum value, or until there are no more enumRange elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="215e5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="215e5-107">Syntax</span></span>

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="215e5-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="215e5-108">Element Information</span></span>



| <span data-ttu-id="215e5-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="215e5-109">Parent Element</span></span>                                         | <span data-ttu-id="215e5-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="215e5-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="215e5-111">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="215e5-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="215e5-112">Nessuno</span><span class="sxs-lookup"><span data-stu-id="215e5-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="215e5-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="215e5-113">Attributes</span></span>



| <span data-ttu-id="215e5-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="215e5-114">Attribute</span></span> | <span data-ttu-id="215e5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="215e5-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="215e5-116">minValue</span><span class="sxs-lookup"><span data-stu-id="215e5-116">minValue</span></span>  | <span data-ttu-id="215e5-117">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="215e5-117">Public.</span></span> <span data-ttu-id="215e5-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="215e5-118">Required.</span></span> <span data-ttu-id="215e5-119">Valore minimo nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="215e5-119">The minimum value in the range.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="215e5-120">setValue</span><span class="sxs-lookup"><span data-stu-id="215e5-120">setValue</span></span>  | <span data-ttu-id="215e5-121">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="215e5-121">Public.</span></span> <span data-ttu-id="215e5-122">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="215e5-122">Optional.</span></span> <span data-ttu-id="215e5-123">Quando un utente seleziona questa enumerazione da un controllo Proprietà ListBox, questo valore discreto viene assegnato come valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="215e5-123">When a user selects this enumeration from a listbox property control, this discrete value is assigned as the property value.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="215e5-124">text</span><span class="sxs-lookup"><span data-stu-id="215e5-124">text</span></span>      | <span data-ttu-id="215e5-125">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="215e5-125">Public.</span></span> <span data-ttu-id="215e5-126">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="215e5-126">Optional.</span></span> <span data-ttu-id="215e5-127">Testo utilizzato per visualizzare il valore enumerato.</span><span class="sxs-lookup"><span data-stu-id="215e5-127">The text used to display the enumerated value.</span></span> <span data-ttu-id="215e5-128">La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto a una stringa di visualizzazione. utilizzare la stringa di visualizzazione indiretta in modo che possa essere localizzata.</span><span class="sxs-lookup"><span data-stu-id="215e5-128">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="215e5-129">tasti di scelta</span><span class="sxs-lookup"><span data-stu-id="215e5-129">mnemonics</span></span> | <span data-ttu-id="215e5-130">**Windows 7 e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="215e5-130">**Windows 7 and later.**</span></span> <span data-ttu-id="215e5-131">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="215e5-131">Public.</span></span> <span data-ttu-id="215e5-132">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="215e5-132">Optional.</span></span> <span data-ttu-id="215e5-133">Elenco di valori mnemonico che possono essere usati per fare riferimento alla proprietà nelle query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="215e5-133">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="215e5-134">L'elenco è delimitato dal carattere " \| ".</span><span class="sxs-lookup"><span data-stu-id="215e5-134">The list is delimited with the '\|' character.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="215e5-135">name</span><span class="sxs-lookup"><span data-stu-id="215e5-135">name</span></span>      | <span data-ttu-id="215e5-136">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="215e5-136">Required.</span></span> <span data-ttu-id="215e5-137">Nome di proprietà canonico, univoco per il sistema; ad esempio, System. rating.</span><span class="sxs-lookup"><span data-stu-id="215e5-137">The canonical property name, unique to the system; for example, System.Rating.</span></span> <span data-ttu-id="215e5-138">Questo attributo è limitato a 64 caratteri.</span><span class="sxs-lookup"><span data-stu-id="215e5-138">This attribute is limited to 64 characters.</span></span> <span data-ttu-id="215e5-139">Il nome fa distinzione tra maiuscole e minuscole e deve usare la sintassi seguente: Publisher. Application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="215e5-139">The name is case sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="215e5-140">I metodi seguenti restituiscono questo valore: [**IExplorerCommand:: GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2:: GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)e [**IPropertyUI:: GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="215e5-140">The following methods return this value: [**IExplorerCommand::GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2::GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2), and [**IPropertyUI::GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span></span> |



 

 

 
