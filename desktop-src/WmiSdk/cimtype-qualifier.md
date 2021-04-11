---
description: Il qualificatore CIMType contiene testo che descrive il tipo di una proprietà.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: Qualificatore CIMType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131983"
---
# <a name="cimtype-qualifier"></a><span data-ttu-id="7d98e-103">Qualificatore CIMType</span><span class="sxs-lookup"><span data-stu-id="7d98e-103">CIMType Qualifier</span></span>

<span data-ttu-id="7d98e-104">Il qualificatore **CimType** contiene testo che descrive il tipo di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="7d98e-104">The **CIMType** qualifier contains text describing the type of a property.</span></span>

<span data-ttu-id="7d98e-105">Questo testo può essere il tipo MOF, ad esempio "String" e "sint32", oppure il tipo CIM, ad esempio "CIM \_ String" e "CIM \_ sint32".</span><span class="sxs-lookup"><span data-stu-id="7d98e-105">This text can be the MOF type such as "string" and "sint32" or the CIM type such as "CIM\_STRING" and "CIM\_SINT32".</span></span> <span data-ttu-id="7d98e-106">Esiste una corrispondenza uno-a-uno tra il qualificatore **CimType** e il tipo della proprietà utilizzata nel parametro *PvtType* del metodo [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .</span><span class="sxs-lookup"><span data-stu-id="7d98e-106">There is a one-to-one correspondence between the **CIMType** qualifier and the type of the property used in the *pvtType* parameter of the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="7d98e-107">Le due eccezioni sono:</span><span class="sxs-lookup"><span data-stu-id="7d98e-107">The two exceptions are:</span></span>

-   <span data-ttu-id="7d98e-108">[*Proprietà di riferimento*](gloss-r.md), che hanno il tipo **CIM \_ Reference**, che contiene il valore "Ref: NomeClasse".</span><span class="sxs-lookup"><span data-stu-id="7d98e-108">[*Reference properties*](gloss-r.md), which have the type **CIM\_REFERENCE**, that contains the "REF:classname" value.</span></span> <span data-ttu-id="7d98e-109">Il valore ClassName descrive il tipo di classe della proprietà Reference.</span><span class="sxs-lookup"><span data-stu-id="7d98e-109">The classname value describes the class type of the reference property.</span></span>
-   <span data-ttu-id="7d98e-110">Proprietà dell'oggetto incorporato, che hanno il tipo di **\_ oggetto CIM** .</span><span class="sxs-lookup"><span data-stu-id="7d98e-110">Embedded object properties, which have the **CIM\_OBJECT** type.</span></span>

<span data-ttu-id="7d98e-111">Si noti, tuttavia, che il qualificatore **CimType** può e deve essere usato per digitare più esattamente una proprietà di riferimento.</span><span class="sxs-lookup"><span data-stu-id="7d98e-111">Please note, however, that the **CIMType** qualifier can and should be used to type a reference property more exactly.</span></span> <span data-ttu-id="7d98e-112">Se, ad esempio, la proprietà si riferisce sempre a istanze della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , il relativo qualificatore **CimType** deve essere impostato su:</span><span class="sxs-lookup"><span data-stu-id="7d98e-112">For example, if the property always refers to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class, its **CIMType** qualifier should be set to:</span></span>


```mof
"ref:Win32_LogicalDisk"
```



<span data-ttu-id="7d98e-113">Per impostazione predefinita, il qualificatore **CimType** di una proprietà Reference dispone del tipo **ref**.</span><span class="sxs-lookup"><span data-stu-id="7d98e-113">By default, the **CIMType** qualifier of a reference property has the type **ref**.</span></span>

<span data-ttu-id="7d98e-114">Come per le proprietà di riferimento, il qualificatore **CimType** deve essere usato per digitare più esattamente una proprietà dell'oggetto incorporato con la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="7d98e-114">As with reference properties, the **CIMType** qualifier should used to type an embedded object property more exactly with the following syntax:</span></span>


```mof
"object:EmbedClass"
```



<span data-ttu-id="7d98e-115">Poiché WMI consente più tipi rispetto a quelli che possono essere espressi dalle costanti standard con il \_ prefisso VT, il qualificatore **CimType** può essere utile per interpretare i valori di tipo.</span><span class="sxs-lookup"><span data-stu-id="7d98e-115">Because WMI allows more types than can be expressed by standard constants with the VT\_ prefix, the **CIMType** qualifier can help interpret type values.</span></span> <span data-ttu-id="7d98e-116">Il qualificatore **CimType** viene aggiunto automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7d98e-116">The **CIMType** qualifier is added automatically.</span></span> <span data-ttu-id="7d98e-117">Per ulteriori informazioni, vedere [tipi di dati MOF](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="7d98e-117">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d98e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d98e-118">Requirements</span></span>



| <span data-ttu-id="7d98e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d98e-119">Requirement</span></span> | <span data-ttu-id="7d98e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7d98e-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7d98e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d98e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7d98e-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d98e-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7d98e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d98e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7d98e-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d98e-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d98e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d98e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d98e-126">**Qualificatori WMI standard**</span><span class="sxs-lookup"><span data-stu-id="7d98e-126">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="7d98e-127">Qualificatori WMI</span><span class="sxs-lookup"><span data-stu-id="7d98e-127">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="7d98e-128">Aggiunta di un qualificatore</span><span class="sxs-lookup"><span data-stu-id="7d98e-128">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

