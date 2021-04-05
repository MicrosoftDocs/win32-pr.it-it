---
description: Per mantenere un'installazione software protetta nei computer bloccati, attenersi a queste linee guida quando si crea il pacchetto di Windows Installer.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Protezione dei pacchetti nei computer bloccati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8380ad7e342d35bff80da4d4d86c37759a80a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882958"
---
# <a name="securing-packages-on-locked-down-computers"></a><span data-ttu-id="99926-103">Protezione dei pacchetti nei computer bloccati</span><span class="sxs-lookup"><span data-stu-id="99926-103">Securing Packages on Locked-Down Computers</span></span>

<span data-ttu-id="99926-104">Rispetto alle linee guida seguenti quando si crea un pacchetto di Windows Installer che verrà usato nei computer bloccati consente di mantenere un ambiente protetto durante l'installazione:</span><span class="sxs-lookup"><span data-stu-id="99926-104">Adherence to the following guidelines when authoring a Windows Installer package that will be used on locked-down computers helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="99926-105">Testare il pacchetto per la compatibilità con i [criteri di sistema](system-policy.md)del computer Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="99926-105">Test your package for compatibility with the Windows Installer machine [System Policy](system-policy.md).</span></span>
-   <span data-ttu-id="99926-106">Assicurarsi di eseguire il pacchetto con tutti i [livelli di interfaccia utente](user-interface-levels.md), nessuno, Basic, Limited e Full.</span><span class="sxs-lookup"><span data-stu-id="99926-106">Make sure you package runs with all [user interface levels](user-interface-levels.md), none, basic, limited, and full.</span></span>
-   <span data-ttu-id="99926-107">Testare il pacchetto in partizioni NTFS, con privilegi [*elevati*](e-gly.md) e non elevati.</span><span class="sxs-lookup"><span data-stu-id="99926-107">Test your package on NTFS partitions, both with [*elevated*](e-gly.md) and non-elevated privileges.</span></span>
-   <span data-ttu-id="99926-108">A partire da Windows Installer 3,0, il [controllo dell'account utente (UAC)](user-account-control--uac--patching.md) consente agli utenti non amministratori di applicare patch alle applicazioni installate nel contesto per computer.</span><span class="sxs-lookup"><span data-stu-id="99926-108">Starting with Windows Installer 3.0, [User Account Control (UAC) Patching](user-account-control--uac--patching.md) enables non-administrator users to patch applications installed in the per-machine context.</span></span> <span data-ttu-id="99926-109">Testare il pacchetto di patch in Windows Vista e Windows XP per l'installazione da parte di utenti con accesso amministratore e da utenti non amministratori.</span><span class="sxs-lookup"><span data-stu-id="99926-109">Test your patch package on Windows Vista and Windows XP for both installation by users with administrator access and by non-administrator users.</span></span>

 

 



