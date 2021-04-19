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
# <a name="provider-configuration-and-troubleshooting-classes"></a><span data-ttu-id="0fc5e-103">Classi di configurazione e risoluzione dei problemi del provider</span><span class="sxs-lookup"><span data-stu-id="0fc5e-103">Provider Configuration and Troubleshooting Classes</span></span>

<span data-ttu-id="0fc5e-104">La classe dei [**\_ provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) e le classi di risoluzione dei problemi WMI sono un gruppo di [classi di evento MSFT](msft-classes.md) associate agli eventi del provider WMI.</span><span class="sxs-lookup"><span data-stu-id="0fc5e-104">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class and the WMI troubleshooting classes are a group of the [MSFT event classes](msft-classes.md) coupled to WMI provider events.</span></span>

<span data-ttu-id="0fc5e-105">La [**classe \_ provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) contiene le informazioni di configurazione per i provider e include i metodi seguenti che consentono di caricare e scaricare i provider oppure sospendere e riprendere le operazioni del provider:</span><span class="sxs-lookup"><span data-stu-id="0fc5e-105">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class contains configuration information for providers and includes the following methods that allow you to load and unload providers, or suspend and resume provider operations:</span></span>

-   [<span data-ttu-id="0fc5e-106">**Metodo Load della \_ classe Providers MSFT**</span><span class="sxs-lookup"><span data-stu-id="0fc5e-106">**Load Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [<span data-ttu-id="0fc5e-107">**Metodo UnLoad della \_ classe Providers MSFT**</span><span class="sxs-lookup"><span data-stu-id="0fc5e-107">**UnLoad Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [<span data-ttu-id="0fc5e-108">**Metodo Resume della \_ classe Providers MSFT**</span><span class="sxs-lookup"><span data-stu-id="0fc5e-108">**Resume Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [<span data-ttu-id="0fc5e-109">**Metodo Suspend della \_ classe Providers MSFT**</span><span class="sxs-lookup"><span data-stu-id="0fc5e-109">**Suspend Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

<span data-ttu-id="0fc5e-110">Le [classi di risoluzione dei problemi WMI](wmi-troubleshooting-classes.md) sono denominate per indicare se l'evento viene generato prima o dopo un evento del provider.</span><span class="sxs-lookup"><span data-stu-id="0fc5e-110">The [WMI troubleshooting classes](wmi-troubleshooting-classes.md) are named to indicate whether the event is fired before or after a provider event.</span></span> <span data-ttu-id="0fc5e-111">Ad esempio, l' [**oggetto \_ \_ \_ precedente MSFT provider WMI AccessCheck**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) viene generato immediatamente prima di chiamare l'implementazione del provider di **IWbemEventSecurity:: AccessCheck**, mentre l'oggetto [**MSFT \_ provider WMI \_ AccessCheck \_ post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) viene chiamato immediatamente dopo.</span><span class="sxs-lookup"><span data-stu-id="0fc5e-111">For example, the [**MSFT\_WmiProvider\_AccessCheck\_Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) object is generated immediately before calling the provider's implementation of **IWbemEventSecurity::AccessCheck**, while the [**MSFT\_WmiProvider\_AccessCheck\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) object is called immediately after.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fc5e-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0fc5e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fc5e-113">Risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="0fc5e-113">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="0fc5e-114">Classi di risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="0fc5e-114">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
