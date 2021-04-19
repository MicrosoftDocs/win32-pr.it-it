---
description: I qualificatori di metadati perfezionano la definizione dei metacostrutti nel modello CIM chiarendo l'utilizzo effettivo di una classe o di una dichiarazione di proprietà all'interno della sintassi MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Qualificatori meta
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314593"
---
# <a name="meta-qualifiers"></a><span data-ttu-id="8fcc0-103">Qualificatori meta</span><span class="sxs-lookup"><span data-stu-id="8fcc0-103">Meta Qualifiers</span></span>

<span data-ttu-id="8fcc0-104">I qualificatori di metadati perfezionano la definizione dei metacostrutti nel modello CIM chiarendo l'utilizzo effettivo di una classe o di una dichiarazione di proprietà all'interno della sintassi MOF.</span><span class="sxs-lookup"><span data-stu-id="8fcc0-104">Meta qualifiers refine the definition of meta-constructs in the CIM model by clarifying the actual usage of a class or property declaration within the MOF syntax.</span></span>

<dt>

<span data-ttu-id="8fcc0-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Associazione**</span><span class="sxs-lookup"><span data-stu-id="8fcc0-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Association**</span></span>
</dt> <dd>

<span data-ttu-id="8fcc0-106">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8fcc0-106">Data type: **boolean**</span></span>

<span data-ttu-id="8fcc0-107">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="8fcc0-107">Applies to: classes</span></span>

<span data-ttu-id="8fcc0-108">Indica se la classe è una classe di associazione utilizzata per descrivere una relazione tra altre due classi.</span><span class="sxs-lookup"><span data-stu-id="8fcc0-108">Indicates whether the class is an association class used to describe a relationship between two other classes.</span></span> <span data-ttu-id="8fcc0-109">L'assenza di questo qualificatore indica che la classe non è una classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="8fcc0-109">The absence of this qualifier indicates that the class is not an association class.</span></span> <span data-ttu-id="8fcc0-110">Questo qualificatore si escludono a vicenda con l' **indicazione**.</span><span class="sxs-lookup"><span data-stu-id="8fcc0-110">This qualifier is mutually exclusive with **Indication**.</span></span> <span data-ttu-id="8fcc0-111">Per ulteriori informazioni, vedere [dichiarazione di una classe di associazione](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="8fcc0-111">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fcc0-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indicazione**</span><span class="sxs-lookup"><span data-stu-id="8fcc0-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indication**</span></span>
</dt> <dd>

<span data-ttu-id="8fcc0-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8fcc0-113">Data type: **boolean**</span></span>

<span data-ttu-id="8fcc0-114">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="8fcc0-114">Applies to: classes</span></span>

<span data-ttu-id="8fcc0-115">Indica se la classe di oggetti definisce un'indicazione.</span><span class="sxs-lookup"><span data-stu-id="8fcc0-115">Indicates whether the object class defines an indication.</span></span> <span data-ttu-id="8fcc0-116">Questo qualificatore si escludono a vicenda con **Association**.</span><span class="sxs-lookup"><span data-stu-id="8fcc0-116">This qualifier is mutually exclusive with **Association**.</span></span> <span data-ttu-id="8fcc0-117">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="8fcc0-117">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fcc0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fcc0-118">Requirements</span></span>



| <span data-ttu-id="8fcc0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fcc0-119">Requirement</span></span> | <span data-ttu-id="8fcc0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8fcc0-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8fcc0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fcc0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8fcc0-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fcc0-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8fcc0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fcc0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8fcc0-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fcc0-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8fcc0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fcc0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcc0-126">Qualificatori WMI</span><span class="sxs-lookup"><span data-stu-id="8fcc0-126">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="8fcc0-127">Aggiunta di un qualificatore</span><span class="sxs-lookup"><span data-stu-id="8fcc0-127">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




