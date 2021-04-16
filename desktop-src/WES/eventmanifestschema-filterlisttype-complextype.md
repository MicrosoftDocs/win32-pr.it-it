---
title: Tipo complesso FilterListType
description: Definisce un elenco di filtri che un controller ETW può passare al provider per limitare ulteriormente gli eventi scritti.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Log eventi di tipo complesso FilterListType
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341213"
---
# <a name="filterlisttype-complex-type"></a><span data-ttu-id="955fd-104">Tipo complesso FilterListType</span><span class="sxs-lookup"><span data-stu-id="955fd-104">FilterListType Complex Type</span></span>

<span data-ttu-id="955fd-105">Definisce un elenco di filtri che un controller ETW può passare al provider per limitare ulteriormente gli eventi scritti.</span><span class="sxs-lookup"><span data-stu-id="955fd-105">Defines a list of filters that an ETW controller can pass to your provider to further limit the events that it writes.</span></span>

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="955fd-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="955fd-106">Child elements</span></span>



| <span data-ttu-id="955fd-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="955fd-107">Element</span></span>    | <span data-ttu-id="955fd-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="955fd-108">Type</span></span>                                                             | <span data-ttu-id="955fd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="955fd-109">Description</span></span>                   |
|------------|------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="955fd-110">**filter**</span><span class="sxs-lookup"><span data-stu-id="955fd-110">**filter**</span></span> | [<span data-ttu-id="955fd-111">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="955fd-111">**FilterType**</span></span>](eventmanifestschema-filtertype-complextype.md) | <span data-ttu-id="955fd-112">Elenco di filtri.</span><span class="sxs-lookup"><span data-stu-id="955fd-112">A list of filters.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="955fd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="955fd-113">Remarks</span></span>

<span data-ttu-id="955fd-114">Un controller ETW è un'applicazione che chiama la funzione [**StartTrace**](/windows/desktop/ETW/starttrace) per creare una sessione ETW.</span><span class="sxs-lookup"><span data-stu-id="955fd-114">An ETW controller is an application that calls the [**StartTrace**](/windows/desktop/ETW/starttrace) function to create an ETW session.</span></span> <span data-ttu-id="955fd-115">Per informazioni dettagliate, vedere [controllo delle sessioni di traccia eventi](/windows/desktop/ETW/controlling-event-tracing-sessions).</span><span class="sxs-lookup"><span data-stu-id="955fd-115">For details, see [Controlling Event Tracing Sessions](/windows/desktop/ETW/controlling-event-tracing-sessions).</span></span> <span data-ttu-id="955fd-116">Il controller può utilizzare la funzione [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) per enumerare i filtri definiti.</span><span class="sxs-lookup"><span data-stu-id="955fd-116">The controller can use the [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) function to enumerate the filters that you define.</span></span> <span data-ttu-id="955fd-117">Il controller può quindi passare uno o più filtri quando chiama la funzione [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) per abilitare il provider.</span><span class="sxs-lookup"><span data-stu-id="955fd-117">The controller can then pass one or more of the filters when it calls the [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) function to enable your provider.</span></span> <span data-ttu-id="955fd-118">Il provider riceve i filtri, insieme al resto dei parametri enable, nella funzione di callback [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) .</span><span class="sxs-lookup"><span data-stu-id="955fd-118">Your provider receives the filters, along with the rest of the enable parameters, in your [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="955fd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="955fd-119">Requirements</span></span>



| <span data-ttu-id="955fd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="955fd-120">Requirement</span></span> | <span data-ttu-id="955fd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="955fd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="955fd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="955fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="955fd-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="955fd-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="955fd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="955fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="955fd-125">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="955fd-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

