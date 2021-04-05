---
title: Tipo semplice logonType
description: Definisce i valori possibili dell'elemento LogonType.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- Utilità di pianificazione di tipo semplice logonType
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120794"
---
# <a name="logontype-simple-type"></a><span data-ttu-id="fd470-104">Tipo semplice logonType</span><span class="sxs-lookup"><span data-stu-id="fd470-104">logonType Simple Type</span></span>

<span data-ttu-id="fd470-105">Definisce i valori possibili dell'elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fd470-105">Defines the possible values of the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="fd470-106">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="fd470-106">Enumeration values</span></span>

<span data-ttu-id="fd470-107">Il tipo semplice **LogonType** definisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fd470-107">The **logonType** simple type defines the following values.</span></span>



| <span data-ttu-id="fd470-108">Valore</span><span class="sxs-lookup"><span data-stu-id="fd470-108">Value</span></span>                      | <span data-ttu-id="fd470-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd470-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd470-110">S4U</span><span class="sxs-lookup"><span data-stu-id="fd470-110">S4U</span></span>                        | <span data-ttu-id="fd470-111">L'utente deve accedere utilizzando un servizio per l'accesso utente (S4U).</span><span class="sxs-lookup"><span data-stu-id="fd470-111">User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="fd470-112">Quando si usa un accesso S4U, nessuna password viene archiviata dal sistema e non è possibile accedere alla rete o ai file crittografati.</span><span class="sxs-lookup"><span data-stu-id="fd470-112">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="fd470-113">Password</span><span class="sxs-lookup"><span data-stu-id="fd470-113">Password</span></span>                   | <span data-ttu-id="fd470-114">L'utente deve eseguire l'accesso con una password.</span><span class="sxs-lookup"><span data-stu-id="fd470-114">User must log on using a password.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="fd470-115">InteractiveToken</span><span class="sxs-lookup"><span data-stu-id="fd470-115">InteractiveToken</span></span>           | <span data-ttu-id="fd470-116">L'utente deve essere già connesso.</span><span class="sxs-lookup"><span data-stu-id="fd470-116">User must already be logged on.</span></span> <span data-ttu-id="fd470-117">L'attività verrà eseguita solo in una sessione interattiva esistente.</span><span class="sxs-lookup"><span data-stu-id="fd470-117">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="fd470-118">InteractiveTokenOrPassword</span><span class="sxs-lookup"><span data-stu-id="fd470-118">InteractiveTokenOrPassword</span></span> | <span data-ttu-id="fd470-119">Non più in uso; attualmente identico a una password.</span><span class="sxs-lookup"><span data-stu-id="fd470-119">No longer in use; currently identical to Password.</span></span><br/> <span data-ttu-id="fd470-120">**Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows Vista e Windows server 2008:** L'attività verrà eseguita in una sessione interattiva esistente oppure l'utente dovrà effettuare l'accesso con una password.</span><span class="sxs-lookup"><span data-stu-id="fd470-120">**Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista and Windows Server 2008:** The task will be run in an existing interactive session or the user must log on using a password.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="fd470-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd470-121">Requirements</span></span>



| <span data-ttu-id="fd470-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd470-122">Requirement</span></span> | <span data-ttu-id="fd470-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fd470-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fd470-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd470-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fd470-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd470-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fd470-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd470-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fd470-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd470-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd470-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd470-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd470-129">Tipi semplici dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="fd470-129">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="fd470-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="fd470-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





