---
description: La classe Provider MSFT e le classi wmi per la risoluzione dei problemi sono un gruppo di classi di \_ evento MSFT associato a eventi del provider WMI.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Classi di configurazione e risoluzione dei problemi del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d37443047e9bbde709fc1c7367f0691d16215eff62e39196987b466aea0830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050499"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a>Classi di configurazione e risoluzione dei problemi del provider

La [**classe \_ Provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) e le classi wmi per la risoluzione dei problemi sono un gruppo di classi di [evento MSFT](msft-classes.md) associato a eventi del provider WMI.

La [**classe \_ Provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) contiene informazioni di configurazione per i provider e include i metodi seguenti che consentono di caricare e scaricare i provider o di sospendere e riprendere le operazioni del provider:

-   [**Metodo Load della classe Providers \_ MSFT**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [**Metodo UnLoad della classe providers \_ MSFT**](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [**Metodo Resume della classe providers \_ MSFT**](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [**Metodo Suspend della classe providers \_ MSFT**](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

Le [classi wmi per la risoluzione dei](wmi-troubleshooting-classes.md) problemi sono denominate per indicare se l'evento viene generato prima o dopo un evento del provider. Ad esempio, l'oggetto [**\_ MSFT WmiProvider \_ AccessCheck \_ Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) viene generato immediatamente prima di chiamare l'implementazione del provider **di IWbemEventSecurity::AccessCheck,** mentre l'oggetto [**\_ MSFT WmiProvider \_ AccessCheck \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) viene chiamato immediatamente dopo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi wmi](wmi-troubleshooting.md)
</dt> <dt>

[Classi wmi per la risoluzione dei problemi](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
