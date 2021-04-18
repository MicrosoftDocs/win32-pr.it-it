---
title: Categorizzazione di proxy e Stub DCOM
description: Categorizzazione di proxy e Stub DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300540"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a>Categorizzazione di proxy e Stub DCOM

DCOM esegue il marshalling dei riferimenti agli oggetti costruendo OBJREF che contengono CLSID. Questi CLSID sono vulnerabili agli attacchi di sicurezza perché le dll arbitrarie possono essere caricate durante il marshalling. Tuttavia, \_ non \_ \_ è possibile specificare il flag di marshalling personalizzato EOAC quando si chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (vedere [**\_ \_ funzionalità di autenticazione Eole**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)). L'impostazione di questo flag consente di proteggere la sicurezza del server quando si utilizza DCOM perché riduce le probabilità di esecuzione di dll arbitrarie. Quando questo flag è impostato, il server consente il marshalling solo dei CLSID implementati in ole32.dll, comadmin.dll, comsvcs.dll o es.dll o che implementano l' \_ ID di categoria del gestore di marshalling CATID.

\_Il gestore di marshalling CATID è un GUID della categoria di componenti che può essere associato a un CLSID sottoposto a marshalling personalizzato. Le interfacce sottoposte a marshalling personalizzato con questo CLSID sono consentite quando EOAC \_ non \_ \_ è impostato alcun marshalling personalizzato tramite [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

 