---
title: Funzioni di NPS Extensions
description: Funzioni di NPS Extensions
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300155"
---
# <a name="nps-extensions-functions"></a>Funzioni di NPS Extensions

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

## <a name="application-defined"></a>Applicazione definita

L'architettura per le DLL di estensione NPS supporta le funzioni esportate seguenti:

-   [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

Le funzioni [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) e [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) sono facoltative.

La DLL di estensione può esportare [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) invece di [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) o [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).

Se la DLL di estensione Esporta [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), è necessario esportare anche [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).

## <a name="system-defined"></a>Definito dal sistema

Quando NPS chiama un'implementazione di [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS passa la funzione un puntatore a una struttura del [**\_ blocco di \_ controllo \_ dell'estensione RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .

La struttura del [**\_ blocco di \_ controllo \_ dell'estensione RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contiene i puntatori a funzione delle funzioni seguenti fornite da NPS:

-   [**GetRequest**](/previous-versions/ms688263(v=vs.85))
-   [**GetResponse**](/previous-versions/ms688270(v=vs.85))
-   [**SetResponseType**](/previous-versions/ms688462(v=vs.85))

Le funzioni [**GetRequest**](/previous-versions/ms688263(v=vs.85)) e [**GetResponse**](/previous-versions/ms688270(v=vs.85)) restituiscono puntatori a una struttura di tipo [**RADIUS \_ Attribute \_ Array**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).

La struttura della [**\_ \_ matrice di attributi RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contiene i puntatori a funzione delle funzioni seguenti fornite da NPS:

-   [**Aggiungere**](/previous-versions/ms688246(v=vs.85))
-   [**AttributeAt**](/previous-versions/ms688253(v=vs.85))
-   [**GetSize**](/previous-versions/ms688277(v=vs.85))
-   [**InsertAt**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**SetAt**](/previous-versions/ms688456(v=vs.85))

 

 