---
title: Prevenzione dell'analisi delle porte
description: Il codice di esempio seguente illustra come impedire l'analisi delle porte usando le eliminazioni mascherate e le eliminazioni invisibile all'utente.
ms.assetid: 9e8f0948-dc83-4e7c-9505-4dfeac8bbcb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e42efe9997587966b0e67eefb9021c46b640fa96fb1faa3828073e967248270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900791"
---
# <a name="preventing-port-scanning"></a>Prevenzione dell'analisi delle porte

Il codice di esempio seguente illustra come impedire l'analisi delle porte usando le eliminazioni mascherate e le eliminazioni invisibile all'utente.


```C++
#include <windows.h>
#include <fwpmu.h>
#include <stdio.h>

#pragma comment(lib, "fwpuclnt.lib")

#define EXIT_ON_ERROR(fnName) \
   if (result != ERROR_SUCCESS) \
   { \
      printf(#fnName " = 0x%08X\n", result); \
      goto CLEANUP; \
   }

DWORD BlockPortScanning(
         __in HANDLE engine,
         __in PCWSTR filterName,
         __in_opt const GUID* providerKey,
         __in_opt const GUID* subLayerKey
         )
{
   DWORD result = ERROR_SUCCESS;
   FWPM_FILTER_CONDITION0 conds[1];
   FWPM_FILTER0 filter;
   BOOL txnInProgress = FALSE;

   // Fill in the common fields shared by all our filters.
   memset(&filter, 0, sizeof(filter));
   // For MUI compatibility, object names should be indirect strings. See
   // SHLoadIndirectString for details.
   filter.displayData.name = (PWSTR)filterName;
   // Link all our objects to our provider. When multiple providers are
   // installed on a computer, this makes it easy to determine who added what.
   filter.providerKey = (GUID*)providerKey;
   // Generally, it's best to add filters to our own sublayer, so we don't have
   // to worry about being overridden by filters added by another provider.
   if (subLayerKey != NULL)
   {
      filter.subLayerKey = *subLayerKey;
   }
   filter.numFilterConditions = 1;
   filter.filterCondition = conds;

   // We add all the objects from within a single transaction to make it easy
   // to clean up partial results in error paths.
   result = FwpmTransactionBegin0(engine, 0);
   EXIT_ON_ERROR(FwpmTransactionBegin0);
   txnInProgress = TRUE;

   //////////
   // Block outbound ICMP Destination Unreachable to prevent UDP port scanning.
   //////////

   // ICMP Type == Destination Unreachable.
   conds[0].fieldKey = FWPM_CONDITION_ICMP_TYPE;
   conds[0].matchType = FWP_MATCH_EQUAL;
   conds[0].conditionValue.type = FWP_UINT16;
   conds[0].conditionValue.uint16 = 3;

   filter.action.type = FWP_ACTION_BLOCK;

   // Add the IPv4 filter.
   filter.layerKey = FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4;
   result = FwpmFilterAdd0(engine, &filter, NULL, NULL);
   EXIT_ON_ERROR(FwpmFilterAdd0);

   // Add the IPv6 filter.
   filter.layerKey = FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6;
   result = FwpmFilterAdd0(engine, &filter, NULL, NULL);
   EXIT_ON_ERROR(FwpmFilterAdd0);


   //////////
   // Block outbound TCP RST to prevent TCP port scanning.
   //////////

   // We don't want to block TCP RST for loopback, so use a condition that
   // matches everything but loopback.
   conds[0].fieldKey = FWPM_CONDITION_FLAGS;
   conds[0].matchType = FWP_MATCH_FLAGS_NONE_SET;
   conds[0].conditionValue.type = FWP_UINT32;
   conds[0].conditionValue.uint32 = FWP_CONDITION_FLAG_IS_LOOPBACK;

   filter.action.type = FWP_ACTION_CALLOUT_TERMINATING;

   // Add the IPv4 filter.
   filter.layerKey = FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD;
   filter.action.calloutKey = FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP;
   result = FwpmFilterAdd0(engine, &filter, NULL, NULL);
   EXIT_ON_ERROR(FwpmFilterAdd0);

   // Add the IPv6 filter.
   filter.layerKey = FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD;
   filter.action.calloutKey = FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP;
   result = FwpmFilterAdd0(engine, &filter, NULL, NULL);
   EXIT_ON_ERROR(FwpmFilterAdd0);

   // Once all the adds have succeeded, we commit the transaction to atomically
   // add all the new objects.
   result = FwpmTransactionCommit0(engine);
   EXIT_ON_ERROR(FwpmTransactionCommit0);
   txnInProgress = FALSE;

CLEANUP:
   if (txnInProgress)
   {
      // Abort any transaction still in progress to clean up partial results.
      FwpmTransactionAbort0(engine);
   }
   return result;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Condizioni di filtro disponibili a ogni livello di filtro**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 




