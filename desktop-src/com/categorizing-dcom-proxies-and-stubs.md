---
title: Categorizzazione di proxy e stub DCOM
description: Categorizzazione di proxy e stub DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45f61d89e31316975685d3e603a93d30559546c86abc3b63e8e7e8a0c83ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310868"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a>Categorizzazione di proxy e stub DCOM

DCOM effettua il marshalling dei riferimenti agli oggetti mediante la creazione di OBJREF contenenti CLSID. Questi CLSID sono vulnerabili agli attacchi alla sicurezza perché le DLL arbitrarie possono essere caricate durante il marshalling. Tuttavia, il flag EOAC NO CUSTOM MARSHAL può essere specificato quando si \_ \_ chiama \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (vedere [**EOLE AUTHENTICATION \_ \_ CAPABILITIES).**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities) L'impostazione di questo flag consente di proteggere la sicurezza del server quando si usa DCOM perché riduce le probabilità di esecuzione di DLL arbitrarie. Quando questo flag è impostato, il server consente il marshalling solo dei CLSID implementati in ole32.dll, comadmin.dll, comsvcs.dll o es.dll o che implementano l'ID categoria \_ MARSHALER CATID.

CATID MARSHALER è un GUID di categoria di componenti che può \_ essere associato a un CLSID di cui viene effettuato il marshalling personalizzato. Le interfacce di cui viene effettuato il marshalling personalizzato con questo CLSID sono consentite quando eOAC NO CUSTOM MARSHAL viene \_ \_ impostato tramite \_ [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

 