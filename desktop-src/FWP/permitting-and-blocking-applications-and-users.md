---
title: Autorizzazione e blocco di applicazioni e utenti
description: Il codice di esempio seguente illustra come aggiungere un filtro che valuta in base all'ID utente o all'applicazione.
ms.assetid: f1ca483e-cf60-499f-8a4a-29656ed9503a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa513809b294451235c5e14cf8b7c79bf41ca754b27134e9366ffce77b4c7cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078491"
---
# <a name="permitting-and-blocking-applications-and-users"></a>Autorizzazione e blocco di applicazioni e utenti

Il codice di esempio seguente illustra come aggiungere un filtro che valuta in base all'ID utente o all'applicazione.


```C++
#include <windows.h>
#include <fwpmu.h>
#include <accctrl.h>
#include <aclapi.h>
#include <stdio.h>

#pragma comment (lib, "fwpuclnt.lib")
#pragma comment (lib, "advapi32.lib")

#define SESSION_NAME L"SDK Examples"

#define EXIT_ON_ERROR(fnName) \
   if (result != ERROR_SUCCESS) \
   { \
      printf(#fnName " = 0x%08X\n", result); \
      goto CLEANUP; \
   }

DWORD FilterByUserAndApp(
         __in HANDLE engine,
         __in PCWSTR filterName,
         __in_opt const GUID* providerKey,
         __in const GUID* layerKey,
         __in_opt const GUID* subLayerKey,
         __in_opt PCWSTR userName,
         __in_opt PCWSTR appPath,
         __in FWP_ACTION_TYPE actionType,
         __out_opt UINT64* filterId
         )
{
   DWORD result = ERROR_SUCCESS;
   FWPM_FILTER_CONDITION0 conds[2];
   UINT32 numConds = 0;
   EXPLICIT_ACCESS_W access;
   ULONG sdLen;
   PSECURITY_DESCRIPTOR sd = NULL;
   FWP_BYTE_BLOB sdBlob, *appBlob = NULL;
   FWPM_FILTER0 filter;

   // Add an FWPM_CONDITION_ALE_USER_ID condition if requested.
   if (userName != NULL)
   {
      // When evaluating SECURITY_DESCRIPTOR conditions, the filter engine
      // checks for FWP_ACTRL_MATCH_FILTER access. If the DACL grants access,
      // it does not mean that the traffic is allowed; it just means that the
      // condition evaluates to true. Likewise if it denies access, the
      // condition evaluates to false.
      BuildExplicitAccessWithNameW(
         &access,
         (PWSTR)userName,
         FWP_ACTRL_MATCH_FILTER,
         GRANT_ACCESS,
         0
         );

      result = BuildSecurityDescriptorW(
                  NULL,
                  NULL,
                  1,
                  &access,
                  0,
                  NULL,
                  NULL,
                  &sdLen,
                  &sd
                  );
      EXIT_ON_ERROR(BuildSecurityDescriptorW);

      // Security descriptors must be in self-relative form (i.e., contiguous).
      // The security descriptor returned by BuildSecurityDescriptorW is
      // already self-relative, but if you're using another mechanism to build
      // the descriptor, you may have to convert it. See MakeSelfRelativeSD for
      // details.
      sdBlob.size = sdLen;
      sdBlob.data = (UINT8*)sd;

      conds[numConds].fieldKey = FWPM_CONDITION_ALE_USER_ID;
      conds[numConds].matchType = FWP_MATCH_EQUAL;
      conds[numConds].conditionValue.type = FWP_SECURITY_DESCRIPTOR_TYPE;
      conds[numConds].conditionValue.sd = &sdBlob;
      ++numConds;
   }

   // Add an FWPM_CONDITION_ALE_APP_ID condition if requested.
   if (appPath != NULL)
   {
      // appPath must be a fully-qualified file name, and the file must
      // exist on the local machine.
      result = FwpmGetAppIdFromFileName0(appPath, &appBlob);
      EXIT_ON_ERROR(FwpmGetAppIdFromFileName0);

      conds[numConds].fieldKey = FWPM_CONDITION_ALE_APP_ID;
      conds[numConds].matchType = FWP_MATCH_EQUAL;
      conds[numConds].conditionValue.type = FWP_BYTE_BLOB_TYPE;
      conds[numConds].conditionValue.byteBlob = appBlob;
      ++numConds;
   }

   memset(&filter, 0, sizeof(filter));
   // For MUI compatibility, object names should be indirect strings. See
   // SHLoadIndirectString for details.
   filter.displayData.name = (PWSTR)filterName;
   // Link all objects to our provider. When multiple providers are installed
   // on a computer, this makes it easy to determine who added what.
   filter.providerKey = (GUID*)providerKey;
   filter.layerKey = *layerKey;
   // Generally, it's best to add filters to our own sublayer, so we don't have
   // to worry about being overridden by filters added by another provider.
   if (subLayerKey != NULL)
   {
      filter.subLayerKey = *subLayerKey;
   }
   filter.numFilterConditions = numConds;
   if (numConds > 0)
   {
      filter.filterCondition = conds;
   }
   filter.action.type = actionType;

   result = FwpmFilterAdd0(engine, &filter, NULL, filterId);
   EXIT_ON_ERROR(FwpmFilterAdd0);

CLEANUP:
   FwpmFreeMemory0((void**)&appBlob);
   LocalFree(sd);
   return result;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Condizioni di filtro disponibili a ogni livello di filtro**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 




