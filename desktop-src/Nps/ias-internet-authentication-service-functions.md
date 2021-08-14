---
title: Funzioni delle estensioni NPS
description: Funzioni delle estensioni NPS
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cecf8ead61e94287ba4846b82f922af40068a771a9bcadd8ccb51693709c17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362361"
---
# <a name="nps-extensions-functions"></a>Funzioni delle estensioni NPS

> [!Note]  
> Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente denominate IAS.

 

## <a name="application-defined"></a>Definito dall'applicazione

L'architettura per le DLL di estensione NPS supporta le funzioni esportate seguenti:

-   [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

Le [**funzioni RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) [**e RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) sono facoltative.

La DLL di estensione può esportare [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) anziché [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) [**o RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).

Se la DLL di estensione esporta [**RadiusExtensionProcessEx,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)deve esportare [**anche RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).

## <a name="system-defined"></a>Definito dal sistema

Quando Server dei criteri di rete chiama un'implementazione di [**RadiusExtensionProcess2,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)Server dei criteri di rete passa alla funzione un puntatore a una [**struttura RADIUS \_ EXTENSION CONTROL \_ \_ BLOCK.**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block)

La [**struttura RADIUS \_ EXTENSION CONTROL \_ \_ BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contiene puntatori a funzione alle funzioni seguenti fornite da Server dei criteri di rete:

-   [**Getrequest**](/previous-versions/ms688263(v=vs.85))
-   [**Getresponse**](/previous-versions/ms688270(v=vs.85))
-   [**SetResponseType**](/previous-versions/ms688462(v=vs.85))

Le funzioni [**GetRequest**](/previous-versions/ms688263(v=vs.85)) e [**GetResponse**](/previous-versions/ms688270(v=vs.85)) restituiscono puntatori a una struttura di tipo [**RADIUS \_ ATTRIBUTE \_ ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).

La [**struttura RADIUS \_ ATTRIBUTE \_ ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contiene puntatori a funzione alle funzioni seguenti fornite da Server dei criteri di rete:

-   [**Add**](/previous-versions/ms688246(v=vs.85))
-   [**AttributeAt**](/previous-versions/ms688253(v=vs.85))
-   [**GetSize**](/previous-versions/ms688277(v=vs.85))
-   [**InsertAt**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**SetAt**](/previous-versions/ms688456(v=vs.85))

 

 