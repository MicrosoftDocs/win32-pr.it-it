---
description: La \_ classe dei provider MSFT e le classi di risoluzione dei problemi WMI sono un gruppo di classi di evento MSFT associate agli eventi del provider WMI.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Classi di configurazione e risoluzione dei problemi del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313180"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a>Classi di configurazione e risoluzione dei problemi del provider

La classe dei [**\_ provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) e le classi di risoluzione dei problemi WMI sono un gruppo di [classi di evento MSFT](msft-classes.md) associate agli eventi del provider WMI.

La [**classe \_ provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) contiene le informazioni di configurazione per i provider e include i metodi seguenti che consentono di caricare e scaricare i provider oppure sospendere e riprendere le operazioni del provider:

-   [**Metodo Load della \_ classe Providers MSFT**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [**Metodo UnLoad della \_ classe Providers MSFT**](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [**Metodo Resume della \_ classe Providers MSFT**](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [**Metodo Suspend della \_ classe Providers MSFT**](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

Le [classi di risoluzione dei problemi WMI](wmi-troubleshooting-classes.md) sono denominate per indicare se l'evento viene generato prima o dopo un evento del provider. Ad esempio, l' [**oggetto \_ \_ \_ precedente MSFT provider WMI AccessCheck**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) viene generato immediatamente prima di chiamare l'implementazione del provider di **IWbemEventSecurity:: AccessCheck**, mentre l'oggetto [**MSFT \_ provider WMI \_ AccessCheck \_ post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) viene chiamato immediatamente dopo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> <dt>

[Classi di risoluzione dei problemi WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
