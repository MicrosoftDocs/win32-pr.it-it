---
description: Per garantire la protezione di un'installazione software, attenersi a queste linee guida durante la creazione di un Windows Installer azione personalizzata.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Linee guida per la protezione di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232253"
---
# <a name="guidelines-for-securing-custom-actions"></a><span data-ttu-id="d6ea2-103">Linee guida per la protezione di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="d6ea2-103">Guidelines for Securing Custom Actions</span></span>

<span data-ttu-id="d6ea2-104">La conformità alle linee guida seguenti quando si crea un pacchetto di Windows Installer con azioni personalizzate consente di mantenere un ambiente protetto durante l'installazione:</span><span class="sxs-lookup"><span data-stu-id="d6ea2-104">Adherence to the following guidelines when authoring a Windows Installer package with custom actions helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="d6ea2-105">Proteggere tutti i file aggiuntivi scritti dall'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-105">Secure any additional files written by your custom action.</span></span>
-   <span data-ttu-id="d6ea2-106">Controllare le lunghezze del buffer e la validità di tutti i dati letti dall'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-106">Check buffer lengths and validity of all data read by your custom action.</span></span> <span data-ttu-id="d6ea2-107">Sono incluse le proprietà che possono fornire dati all'azione personalizzata, in particolare quelle che utilizzano proprietà pubbliche fornite da un utente.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-107">This includes properties that may supply data to your custom action, particularly those that use public properties provided by a user.</span></span>
-   <span data-ttu-id="d6ea2-108">Non fare affidamento su dll esterne non ritenuti attendibili dal sistema in tutte le piattaforme in cui è previsto l'esecuzione del pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-108">Do not rely on external DLLs that are not trusted by the system on all platforms on which your installation package is intended to run.</span></span>
-   <span data-ttu-id="d6ea2-109">Valutare attentamente se usare azioni personalizzate che usano privilegi [*elevati*](e-gly.md) o la rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-109">Carefully consider whether to use custom actions that use [*elevated*](e-gly.md) privileges or impersonation.</span></span> <span data-ttu-id="d6ea2-110">Azioni personalizzate, ad esempio "apertura di un URL dopo il completamento dell'installazione", "avvio del software dopo il completamento dell'installazione" o "avvio del file Leggimi al termine dell'installazione" non richiede in genere privilegi elevati per funzionare.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-110">Custom actions such as “open a URL after installation is completed,” “launch the software after installation is complete,” or “launch ReadMe after installation is complete” would not usually require elevated privileges to function.</span></span> <span data-ttu-id="d6ea2-111">Se l'azione personalizzata deve essere eseguita con privilegi *elevati* , assicurarsi che il codice dell'azione personalizzata protegga dai sovraccarichi del buffer e dal caricamento accidentale del codice unsafe.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-111">If your custom action must run with *elevated* privileges, be sure that the custom action code guards against buffer overruns and inadvertent loading of unsafe code.</span></span> <span data-ttu-id="d6ea2-112">Si noti che durante la fase di esecuzione dell'installazione, il programma di installazione passa informazioni a un processo con privilegi *elevati* ed esegue lo script.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-112">Note that during the execution phase of the installation, the installer passes information to a process with *elevated* privileges and runs the script.</span></span> <span data-ttu-id="d6ea2-113">Qualsiasi azione personalizzata eseguita durante la fase di esecuzione può essere eseguita con privilegi *elevati* .</span><span class="sxs-lookup"><span data-stu-id="d6ea2-113">Any custom actions that run during the execution phase may run with *elevated* privileges.</span></span>
-   <span data-ttu-id="d6ea2-114">Consente di raccogliere tutte le informazioni fornite dall'utente durante la sequenza dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-114">Gather all information provided by the user during the UI sequence.</span></span> <span data-ttu-id="d6ea2-115">Non richiedere all'utente le informazioni che non possono essere impostate con una proprietà pubblica.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-115">Do not prompt the user for any information that can't be set using a public property.</span></span>
-   <span data-ttu-id="d6ea2-116">Se l'azione personalizzata dello script espande le proprietà, adottare le precauzioni per garantire che l'azione personalizzata sia protetta dalla possibilità di inserimento di script.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-116">If your script custom action expands properties, take precautions that the custom action is secured against the possibility of script injection.</span></span> <span data-ttu-id="d6ea2-117">È possibile che lo script venga registrato come testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="d6ea2-117">Script may be logged in clear text.</span></span>

<span data-ttu-id="d6ea2-118">Vedere anche [sicurezza dell'azione personalizzata](custom-action-security.md).</span><span class="sxs-lookup"><span data-stu-id="d6ea2-118">See also [Custom Action Security](custom-action-security.md).</span></span>

 

 



