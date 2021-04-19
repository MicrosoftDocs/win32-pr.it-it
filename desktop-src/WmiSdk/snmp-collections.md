---
description: Una raccolta SNMP esegue il mapping a una classe CIM e gli elementi di una raccolta vengono mappati alle proprietà di una classe CIM. Tutte le definizioni di classi CIM generate devono essere derivate dalla classe SnmpObjectType.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: Raccolte SNMP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309882"
---
# <a name="snmp-collections"></a><span data-ttu-id="8730c-104">Raccolte SNMP</span><span class="sxs-lookup"><span data-stu-id="8730c-104">SNMP Collections</span></span>

<span data-ttu-id="8730c-105">Una raccolta SNMP esegue il mapping a una classe CIM e gli elementi di una raccolta vengono mappati alle proprietà di una classe CIM.</span><span class="sxs-lookup"><span data-stu-id="8730c-105">An SNMP collection maps to a CIM class and the elements of a collection map to the properties of a CIM class.</span></span> <span data-ttu-id="8730c-106">Tutte le definizioni di classi CIM generate devono essere derivate dalla classe **SnmpObjectType** .</span><span class="sxs-lookup"><span data-stu-id="8730c-106">All generated CIM class definitions must be derived from the **SnmpObjectType** class.</span></span>

> [!Note]  
> <span data-ttu-id="8730c-107">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8730c-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="8730c-108">Le definizioni di classe seguenti controllano tutte le definizioni delle classi generate:</span><span class="sxs-lookup"><span data-stu-id="8730c-108">The following class definitions parent all generated class definitions:</span></span>

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a><span data-ttu-id="8730c-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8730c-109">Remarks</span></span>

<span data-ttu-id="8730c-110">Quando si esegue il mapping di raccolte SNMP a classi CIM, si applicano le regole seguenti.</span><span class="sxs-lookup"><span data-stu-id="8730c-110">The following rules apply when mapping SNMP collections to CIM classes.</span></span> <span data-ttu-id="8730c-111">Se non diversamente specificato, queste regole si applicano alle raccolte scalari e di tabella:</span><span class="sxs-lookup"><span data-stu-id="8730c-111">Unless otherwise specified, these rules apply to both scalar and table collections:</span></span>

-   <span data-ttu-id="8730c-112">Il processo di mapping genera i nomi delle classi CIM concatenando "SNMP \_ ", il nome dell'identità del modulo MIB, " \_ " e il descrittore di oggetto della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8730c-112">The mapping process generates CIM class names by concatenating "SNMP\_", the MIB module identity name, "\_", and the collection's object descriptor.</span></span>

    <span data-ttu-id="8730c-113">Ad esempio: il **sistema** si traduce in **SNMP \_ RFC1213 \_ MIB \_ System**, mentre **iftable** si traduce in **SNMP \_ RFC1213 \_ MIB \_ iftable**.</span><span class="sxs-lookup"><span data-stu-id="8730c-113">For example: **system** translates to **SNMP\_RFC1213\_MIB\_system**, while **ifTable** translates to **SNMP\_RFC1213\_MIB\_ifTable**.</span></span>

-   <span data-ttu-id="8730c-114">In tutti i casi, i trattini (-) negli identificatori MIB SNMP vengono mappati ai caratteri di sottolineatura ( \_ ) nei nomi di classe CIM.</span><span class="sxs-lookup"><span data-stu-id="8730c-114">In all cases, hyphens (-) in SNMP MIB identifiers map to underscores (\_) in CIM class names.</span></span>
-   <span data-ttu-id="8730c-115">I conflitti di denominazione possono verificarsi a causa di un nome CIM senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8730c-115">Naming conflicts can occur due to CIM name case-insensitivity.</span></span> <span data-ttu-id="8730c-116">Se si verifica un conflitto di denominazione, il provider sceglie una delle definizioni di gruppo in conflitto e ignora le definizioni rimanenti.</span><span class="sxs-lookup"><span data-stu-id="8730c-116">If a naming conflict occurs, the provider chooses one of the conflicting group definitions and ignores the remaining definitions.</span></span>
-   <span data-ttu-id="8730c-117">Il nome di identità del modulo MIB che contiene la raccolta è mappato al nome del **modulo \_** qualificatore della classe CIM.</span><span class="sxs-lookup"><span data-stu-id="8730c-117">The identity name of the MIB module that contains the collection maps to the CIM class qualifier **Module\_Name**.</span></span>
-   <span data-ttu-id="8730c-118">L'identificatore di oggetto della raccolta fabbricata viene mappato al gruppo di qualificatori della classe CIM **\_ ObjectID**.</span><span class="sxs-lookup"><span data-stu-id="8730c-118">The object identifier of the fabricated collection maps to the CIM class qualifier **Group\_Objectid**.</span></span>
-   <span data-ttu-id="8730c-119">L'elenco di importazioni del modulo MIB (ottenuto dalla definizione della macro **Module-Identity** ) viene mappato alle **\_ importazioni del modulo** qualificatore di classe CIM.</span><span class="sxs-lookup"><span data-stu-id="8730c-119">The MIB module imports list (obtained from the **MODULE-IDENTITY** macro definition) maps to the CIM class qualifier **module\_imports**.</span></span> <span data-ttu-id="8730c-120">Questo qualificatore contiene un elenco delimitato da virgole di nomi di moduli.</span><span class="sxs-lookup"><span data-stu-id="8730c-120">This qualifier contains a comma-separated list of module names.</span></span>

 

 



