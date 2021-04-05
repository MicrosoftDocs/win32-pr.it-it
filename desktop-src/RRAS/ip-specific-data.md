---
title: Struttura IP_SPECIFIC_DATA (RTM. h)
description: La \_ struttura dei dati specifici dell'IP contiene dati specifici dell'IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- RAS struttura IP_SPECIFIC_DATA
- RAS puntatore alla struttura PIP_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120435"
---
# <a name="ip_specific_data-structure"></a><span data-ttu-id="afb09-105">\_ \_ Struttura dati specifica IP</span><span class="sxs-lookup"><span data-stu-id="afb09-105">IP\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="afb09-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="afb09-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="afb09-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="afb09-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="afb09-108">La **struttura \_ dei dati specifici dell'IP** contiene dati specifici dell'IP.</span><span class="sxs-lookup"><span data-stu-id="afb09-108">The **IP\_SPECIFIC DATA** structure contains IP-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="afb09-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afb09-109">Syntax</span></span>


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="afb09-110">Members</span><span class="sxs-lookup"><span data-stu-id="afb09-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="afb09-111">**\_Tipo FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-111">**FSD\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-112">Specifica il tipo di route come definito nella [specifica RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="afb09-112">Specifies the route type as defined in [RFC 1354](routing-protocols-request-for-comments.md).</span></span> <span data-ttu-id="afb09-113">Nella tabella seguente sono riportati i valori possibili per il membro.</span><span class="sxs-lookup"><span data-stu-id="afb09-113">The following table shows the possible values for this member.</span></span>



| <span data-ttu-id="afb09-114">Membro</span><span class="sxs-lookup"><span data-stu-id="afb09-114">Member</span></span>                                                                                               | <span data-ttu-id="afb09-115">Significato</span><span class="sxs-lookup"><span data-stu-id="afb09-115">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="afb09-116"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="afb09-116"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="afb09-117">Il tipo di route non è specificato.</span><span class="sxs-lookup"><span data-stu-id="afb09-117">The route type is not specified.</span></span> <span data-ttu-id="afb09-118">Il tipo è diverso da quelli elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="afb09-118">The type is different from those listed here.</span></span><br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <span data-ttu-id="afb09-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="afb09-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="afb09-120">Route non valida.</span><span class="sxs-lookup"><span data-stu-id="afb09-120">The route is invalid.</span></span> <span data-ttu-id="afb09-121">In genere, questo valore viene usato per invalidare una route.</span><span class="sxs-lookup"><span data-stu-id="afb09-121">Normally, this value is used to invalidate a route.</span></span> <span data-ttu-id="afb09-122">Tuttavia, poiché l'invalidamento non è supportato da Gestione tabelle di routing, la route viene ancora considerata nei calcoli con la migliore route.</span><span class="sxs-lookup"><span data-stu-id="afb09-122">However, since invalidation is not supported by the routing table manager, the route is still considered in best-route computations.</span></span> <span data-ttu-id="afb09-123">Pertanto, i protocolli di routing non devono usare questo valore.</span><span class="sxs-lookup"><span data-stu-id="afb09-123">Therefore, routing protocols should not use this value.</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="afb09-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="afb09-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="afb09-125">La route è una route locale, ovvero l'hop successivo è la destinazione finale.</span><span class="sxs-lookup"><span data-stu-id="afb09-125">The route is a local route, that is, the next hop is the final destination.</span></span><br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <span data-ttu-id="afb09-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="afb09-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="afb09-127">La route è una route remota, ovvero l'hop successivo non è la destinazione finale.</span><span class="sxs-lookup"><span data-stu-id="afb09-127">The route is a remote route, that is, the next hop is not the final destination.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="afb09-128">**\_Criteri FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-128">**FSD\_Policy**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-129">Specifica il set di condizioni che causerebbero la selezione di una route a percorsi multipli.</span><span class="sxs-lookup"><span data-stu-id="afb09-129">Specifies the set of conditions that would cause the selection of a multi-path route.</span></span> <span data-ttu-id="afb09-130">Questo membro è in genere in formato IP TOS.</span><span class="sxs-lookup"><span data-stu-id="afb09-130">This member is typically in IP TOS format.</span></span> <span data-ttu-id="afb09-131">Per ulteriori informazioni, vedere [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="afb09-131">For more information, see [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="afb09-132">**\_NEXTHOPAS FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-132">**FSD\_NextHopAS**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-133">Specifica il numero di sistema autonomo dell'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="afb09-133">Specifies the autonomous system number of the next hop.</span></span>

</dd> <dt>

<span data-ttu-id="afb09-134">**\_Priorità FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-134">**FSD\_Priority**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-135">Specifica un valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="afb09-135">Specifies a metric value.</span></span> <span data-ttu-id="afb09-136">Gestione tabelle di routing utilizza questo valore per confrontare questa voce di route con le voci di route ottenute da altri protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="afb09-136">The routing table manager uses this value to compare this route entry to route entries obtained from other routing protocols.</span></span> <span data-ttu-id="afb09-137">Il valore di questo membro viene impostato da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="afb09-137">The value of this member is set by the routing table manager.</span></span>

</dd> <dt>

<span data-ttu-id="afb09-138">**\_Metrica FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-138">**FSD\_Metric**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-139">Specifica un valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="afb09-139">Specifies a metric value.</span></span> <span data-ttu-id="afb09-140">Gestione tabelle di routing utilizza questo valore per confrontare questa voce di route con altre voci di route ottenute dallo stesso protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="afb09-140">The routing table manager uses this value to compare this route entry to other route entries obtained from the same routing protocol.</span></span> <span data-ttu-id="afb09-141">Il valore di questo membro viene impostato dal protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="afb09-141">The value of this member is set by the routing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="afb09-142">**\_METRIC1 FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-142">**FSD\_Metric1**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-143">Specifica un valore di metrica specifico del protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="afb09-143">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="afb09-144">Questo valore della metrica è documentato nella [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="afb09-144">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="afb09-145">**\_METRIC2 FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-145">**FSD\_Metric2**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-146">Specifica un valore di metrica specifico del protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="afb09-146">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="afb09-147">Questo valore della metrica è documentato nella [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="afb09-147">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="afb09-148">**\_METRIC3 FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-148">**FSD\_Metric3**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-149">Specifica un valore di metrica specifico del protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="afb09-149">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="afb09-150">Questo valore della metrica è documentato nella [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="afb09-150">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="afb09-151">**\_METRIC4 FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-151">**FSD\_Metric4**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-152">Specifica un valore di metrica specifico del protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="afb09-152">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="afb09-153">Questo valore della metrica è documentato nella [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="afb09-153">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="afb09-154">**\_METRICA5 FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-154">**FSD\_Metric5**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-155">Specifica un valore di metrica specifico del protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="afb09-155">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="afb09-156">Questo valore della metrica è documentato nella [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="afb09-156">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="afb09-157">**\_Flag FSD**</span><span class="sxs-lookup"><span data-stu-id="afb09-157">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="afb09-158">Specifica se la route è valida.</span><span class="sxs-lookup"><span data-stu-id="afb09-158">Specifies whether the route is valid.</span></span> <span data-ttu-id="afb09-159">Il protocollo di routing deve prima cancellare questi flag, quindi impostare la route come valida o non valida.</span><span class="sxs-lookup"><span data-stu-id="afb09-159">The routing protocol should first clear these flags, then set the route as either valid or invalid.</span></span> <span data-ttu-id="afb09-160">Per eseguire queste operazioni, il protocollo di routing deve usare le macro **ClearRouteFlags ()**, **SetRouteValid ()** e **ClearRouteValid ()** .</span><span class="sxs-lookup"><span data-stu-id="afb09-160">The routing protocol should use the macros **ClearRouteFlags()**, **SetRouteValid()**, and **ClearRouteValid()** to perform these operations.</span></span> <span data-ttu-id="afb09-161">Queste macro sono definite in RTM. h.</span><span class="sxs-lookup"><span data-stu-id="afb09-161">These macros are defined in Rtm.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afb09-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="afb09-162">Remarks</span></span>

<span data-ttu-id="afb09-163">Gestione tabelle di routing utilizza i membri della **\_ metrica** **FSD \_ Priority** e FSD per calcolare la migliore route a una determinata rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="afb09-163">The routing table manager uses the **FSD\_Priority** and **FSD\_Metric** members to compute the best route to a particular destination network.</span></span>

<span data-ttu-id="afb09-164">I membri della **\_ metrica FSD \[ 1-5 \]** sono per la conformità a MIB II.</span><span class="sxs-lookup"><span data-stu-id="afb09-164">The **FSD\_Metric\[1-5\]** members are for MIB II conformance.</span></span> <span data-ttu-id="afb09-165">Gli agenti MIB II visualizzano solo questi valori di metrica.</span><span class="sxs-lookup"><span data-stu-id="afb09-165">MIB II agents display only these metric values.</span></span> <span data-ttu-id="afb09-166">Non visualizzano il valore della metrica della **\_ metrica FSD** .</span><span class="sxs-lookup"><span data-stu-id="afb09-166">They do not display the **FSD\_Metric** metric value.</span></span> <span data-ttu-id="afb09-167">Per visualizzare la **\_ metrica FSD** , il protocollo di routing deve archiviare anche il valore in uno dei membri **della \_ metrica \[ FSD \] 1-5** .</span><span class="sxs-lookup"><span data-stu-id="afb09-167">To have the **FSD\_Metric** displayed, the routing protocol should also store the value in one of the **FSD\_Metric\[1-5\]** members.</span></span>

<span data-ttu-id="afb09-168">Gestione tabelle di routing non usa i valori delle metriche nei membri **della \_ metrica \[ FSD \] 1-5** durante il calcolo della migliore route a una rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="afb09-168">The routing table manager does not use the metric values in the **FSD\_Metric\[1-5\]** members when computing the best route to a destination network.</span></span> <span data-ttu-id="afb09-169">Il protocollo di routing deve pertanto garantire che il membro della **\_ metrica FSD** disponga di un valore di metrica appropriato.</span><span class="sxs-lookup"><span data-stu-id="afb09-169">Therefore, the routing protocol should ensure that the **FSD\_Metric** member has an appropriate metric value.</span></span>

<span data-ttu-id="afb09-170">Un protocollo di routing può utilizzare **i \_ flag FSD** per contrassegnare una route come non valida, se la route non deve essere utilizzata da altri protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="afb09-170">A routing protocol could use the **FSD\_Flags** to mark a route as invalid, if the route should not be used by other routing protocols.</span></span>

## <a name="requirements"></a><span data-ttu-id="afb09-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afb09-171">Requirements</span></span>



| <span data-ttu-id="afb09-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="afb09-172">Requirement</span></span> | <span data-ttu-id="afb09-173">Valore</span><span class="sxs-lookup"><span data-stu-id="afb09-173">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="afb09-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afb09-174">Minimum supported client</span></span><br/> | <span data-ttu-id="afb09-175">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="afb09-175">None supported</span></span><br/>                                                        |
| <span data-ttu-id="afb09-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afb09-176">Minimum supported server</span></span><br/> | <span data-ttu-id="afb09-177">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="afb09-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="afb09-178">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="afb09-178">End of server support</span></span><br/>    | <span data-ttu-id="afb09-179">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afb09-179">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="afb09-180">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afb09-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="afb09-181"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="afb09-181"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afb09-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afb09-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afb09-183">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="afb09-183">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="afb09-184">Strutture di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="afb09-184">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="afb09-185">**\_route IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="afb09-185">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





