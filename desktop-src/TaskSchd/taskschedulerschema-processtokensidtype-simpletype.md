---
title: Tipo semplice processTokenSidType
description: Definisce i valori possibili per l'elemento ProcessTokenSidType (principalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Utilità di pianificazione di tipo semplice processTokenSidType
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400472"
---
# <a name="processtokensidtype-simple-type"></a><span data-ttu-id="361d9-104">Tipo semplice processTokenSidType</span><span class="sxs-lookup"><span data-stu-id="361d9-104">processTokenSidType Simple Type</span></span>

<span data-ttu-id="361d9-105">Definisce i valori possibili per l'elemento [**ProcessTokenSidType (PrincipalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="361d9-105">Defines the possible values for the [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="361d9-106">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="361d9-106">Enumeration values</span></span>

<span data-ttu-id="361d9-107">Il tipo semplice **processTokenSidType** definisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="361d9-107">The **processTokenSidType** simple type defines the following values.</span></span>



| <span data-ttu-id="361d9-108">Valore</span><span class="sxs-lookup"><span data-stu-id="361d9-108">Value</span></span>        | <span data-ttu-id="361d9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="361d9-109">Description</span></span>                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="361d9-110">nessuno</span><span class="sxs-lookup"><span data-stu-id="361d9-110">None</span></span>         | <span data-ttu-id="361d9-111">Le attività vengono eseguite in un processo che non contiene un SID del token di processo. non verrà apportata alcuna modifica all'elenco dei gruppi di token di processo.</span><span class="sxs-lookup"><span data-stu-id="361d9-111">Tasks are run in a process that does not contain a process token SID (no changes will be made to the process token groups list).</span></span><br/> |
| <span data-ttu-id="361d9-112">Senza restrizioni</span><span class="sxs-lookup"><span data-stu-id="361d9-112">Unrestricted</span></span> | <span data-ttu-id="361d9-113">Un SID attività sarà derivato dal percorso completo dell'attività e verrà aggiunto all'elenco dei gruppi di token di processo.</span><span class="sxs-lookup"><span data-stu-id="361d9-113">A task SID will be derived from the full task path and will be added to the process token groups list.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="361d9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="361d9-114">Requirements</span></span>



| <span data-ttu-id="361d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="361d9-115">Requirement</span></span> | <span data-ttu-id="361d9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="361d9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="361d9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="361d9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="361d9-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="361d9-118">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="361d9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="361d9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="361d9-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="361d9-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





