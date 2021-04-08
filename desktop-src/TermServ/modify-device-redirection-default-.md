---
title: Modificare il reindirizzamento dei dispositivi predefinito
description: Poiché Desktop remoto server gateway tentano di applicare criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client tramite a un server host sessione Desktop remoto, potrebbe essere necessario disabilitare questa impostazione predefinita in alcuni casi.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856293"
---
# <a name="modify-device-redirection-default"></a><span data-ttu-id="cadc8-103">Modificare il reindirizzamento dei dispositivi predefinito</span><span class="sxs-lookup"><span data-stu-id="cadc8-103">Modify Device Redirection Default</span></span>

<span data-ttu-id="cadc8-104">Poiché Desktop remoto server gateway tentano di applicare criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client tramite a un server host sessione Desktop remoto, potrebbe essere necessario disabilitare questa impostazione predefinita in alcuni casi.</span><span class="sxs-lookup"><span data-stu-id="cadc8-104">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

<span data-ttu-id="cadc8-105">In Windows Server 2008 R2 e versioni successive, per impostazione predefinita Desktop remoto server gateway tenterà di applicare i criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client tramite a un server host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="cadc8-105">On Windows Server 2008 R2 and later, Remote Desktop Gateway servers will by default attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server.</span></span> <span data-ttu-id="cadc8-106">Questa funzionalità, tuttavia, non è supportata da alcuni server.</span><span class="sxs-lookup"><span data-stu-id="cadc8-106">However, this feature is not supported by some servers.</span></span> <span data-ttu-id="cadc8-107">Ad esempio, questa operazione non è supportata per le connessioni alle sessioni della console Hyper-V e potrebbe essere necessario disabilitare l'impostazione predefinita per supportare l'autenticazione federata.</span><span class="sxs-lookup"><span data-stu-id="cadc8-107">For example, this is not supported for connections to Hyper-V console sessions, and it may be necessary to disable the default to support federated authentication.</span></span> <span data-ttu-id="cadc8-108">In questi casi, è possibile disabilitare questa funzionalità creando la seguente chiave del registro di sistema per consentire le connessioni.</span><span class="sxs-lookup"><span data-stu-id="cadc8-108">In these cases, this feature can be disabled by creating the following registry key to allow connections to go through.</span></span>

<span data-ttu-id="cadc8-109">**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ terminal server gateway \\ preRDPDisableRegKey**</span><span class="sxs-lookup"><span data-stu-id="cadc8-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server Gateway\\preRDPDisableRegKey**</span></span>

<span data-ttu-id="cadc8-110">Quando questa chiave esiste, il Gateway Desktop remoto non impone il reindirizzamento dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="cadc8-110">When this key exists, the Remote Desktop Gateway will not enforce device redirection.</span></span>

 

 




