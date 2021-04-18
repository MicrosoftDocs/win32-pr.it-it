---
description: Dopo aver creato un'estensione dello snap-in allegati, è necessario registrarla affinché gli snap-in MMC e configurazione di sicurezza vengano individuati e usati.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registrazione di un'estensione dello snap-in allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306425"
---
# <a name="registering-an-attachment-snap-in-extension"></a><span data-ttu-id="10407-103">Registrazione di un'estensione dello snap-in allegati</span><span class="sxs-lookup"><span data-stu-id="10407-103">Registering an Attachment Snap-in Extension</span></span>

<span data-ttu-id="10407-104">Dopo aver creato un'estensione dello snap-in allegati, è necessario registrarla affinché gli snap-in MMC e configurazione di sicurezza vengano individuati e usati.</span><span class="sxs-lookup"><span data-stu-id="10407-104">After you create an attachment snap-in extension, you must register it in order for the MMC and the Security Configuration snap-ins to locate and use it.</span></span>

<span data-ttu-id="10407-105">Lo snap-in allegato deve estendere lo spazio dei nomi degli snap-in configurazione di sicurezza aggiungendo il proprio nodo, come descritto nella procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="10407-105">Your attachment snap-in must extend the Security Configuration snap-ins namespace by adding its own node as described in the following procedure.</span></span>

<span data-ttu-id="10407-106">**Per installare e registrare l'estensione dello snap-in allegati**</span><span class="sxs-lookup"><span data-stu-id="10407-106">**To install and register the attachment snap-in extension**</span></span>

1.  <span data-ttu-id="10407-107">Registrare l'estensione dello snap-in nella seguente chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="10407-107">Register the snap-in extension under the following registry key.</span></span> <span data-ttu-id="10407-108">Non creare una chiave autonoma nello snap-in; le estensioni degli snap-in allegati devono essere solo estensioni.</span><span class="sxs-lookup"><span data-stu-id="10407-108">Do not create a StandAlone key under the snap-in; attachment snap-ins extensions must only be extensions.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  <span data-ttu-id="10407-109">Registrare l'estensione dello snap-in allegati nelle sottochiavi seguenti.</span><span class="sxs-lookup"><span data-stu-id="10407-109">Register the attachment snap-in extension under the following subkeys.</span></span> <span data-ttu-id="10407-110">Questa operazione può essere eseguita come parte delle implementazioni delle funzioni **DllRegisterServer** e **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="10407-110">This can be done as part of your **DllRegisterServer** and **DllUnregisterServer** function implementations.</span></span>

    <span data-ttu-id="10407-111">Spazio dei nomi [modelli di sicurezza](security-templates.md) :</span><span class="sxs-lookup"><span data-stu-id="10407-111">[Security Templates](security-templates.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    <span data-ttu-id="10407-112">[Configurazione della sicurezza e](security-configuration-and-analysis.md) spazio dei nomi di analisi:</span><span class="sxs-lookup"><span data-stu-id="10407-112">[Security Configuration and Analysis](security-configuration-and-analysis.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



