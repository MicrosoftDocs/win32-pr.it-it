---
description: 'Altre informazioni su: considerazioni sulla programmazione per la scrittura di gestori di risorse'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Considerazioni sulla programmazione per la scrittura di gestori di risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae64ead32c747a0e8499dcdc8821d36f01f06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313363"
---
# <a name="programming-considerations-for-writing-resource-managers"></a><span data-ttu-id="b21a0-103">Considerazioni sulla programmazione per la scrittura di gestori di risorse</span><span class="sxs-lookup"><span data-stu-id="b21a0-103">Programming Considerations For Writing Resource Managers</span></span>

<span data-ttu-id="b21a0-104">Quando si usa l'API di gestione transazioni kernel per aggiungere il supporto delle transazioni alle applicazioni, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b21a0-104">When using the Kernel Transaction Manager API to add transaction support to your applications, consider the following:</span></span>

-   <span data-ttu-id="b21a0-105">Quando si scrive il proprio Resource Manager, è necessario disporre di una conoscenza approfondita del funzionamento delle tecniche e dei protocolli di gestione delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="b21a0-105">When you are writing your own resource manager, you should have a good, working knowledge of transaction management techniques and protocols.</span></span>
-   <span data-ttu-id="b21a0-106">Se non si scrivono correttamente i gestori delle risorse, è possibile danneggiare i propri dati con operazioni di ripristino gestite in modo non corretto.</span><span class="sxs-lookup"><span data-stu-id="b21a0-106">If you do not write resource managers correctly, you can corrupt your own data with improperly handled recovery operations.</span></span> <span data-ttu-id="b21a0-107">È anche possibile aggiungere la parte finale del log delle transazioni e riempire la file system con i log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="b21a0-107">You can also pin the tail of transaction log and fill up your file system with transaction logs.</span></span>
-   <span data-ttu-id="b21a0-108">Se i criteri per le dimensioni del log non sono impostati in modo da impedire l'aumento delle dimensioni del log, Resource Manager non arresterà le transazioni.</span><span class="sxs-lookup"><span data-stu-id="b21a0-108">If your log size policy is not set to prevent the log from increasing in size, your resource manager will not stop transactions.</span></span> <span data-ttu-id="b21a0-109">Resource Manager deve arrestare l'aggiornamento del sistema in modo da non sovraccaricare le risorse file system.</span><span class="sxs-lookup"><span data-stu-id="b21a0-109">Your resource manager must stop updating the system so it does not overrun the file system resources.</span></span>
-   <span data-ttu-id="b21a0-110">I gestori di risorse devono usare gli elenchi di controllo di accesso (ACL) per controllare l'accesso ai file di log. in caso contrario, sono possibili attacchi di tipo Denial of Service.</span><span class="sxs-lookup"><span data-stu-id="b21a0-110">Resource managers should use access control lists (ACLs) to control access to the log files; otherwise, denial of service attacks are possible.</span></span>
-   <span data-ttu-id="b21a0-111">Qualsiasi gestore di risorse o partecipante alla transazione che memorizza nella cache i dati deve integrarsi per le notifiche di pre-preparazione.</span><span class="sxs-lookup"><span data-stu-id="b21a0-111">Any resource manager or transaction participant that caches data must enlist for pre-prepare notifications.</span></span> <span data-ttu-id="b21a0-112">Quando viene ricevuta una notifica preliminare, è necessario scaricare tutti i dati, in modo che qualsiasi gestore di risorse downstream possa integrarsi prima della fase di preparazione.</span><span class="sxs-lookup"><span data-stu-id="b21a0-112">When a pre-prepare notification is received, you must flush all your data, so that any downstream resource managers can enlist before the prepare phase.</span></span> <span data-ttu-id="b21a0-113">Eventuali ulteriori operazioni nella transazione non devono essere memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="b21a0-113">Any further work in that transaction must not be cached.</span></span>
-   <span data-ttu-id="b21a0-114">Non chiudere un handle di integrazione mentre la transazione è ancora attiva. in questo modo verrà eseguito il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="b21a0-114">Do not close an enlistment handle while the transaction is still active; this will cause the transaction to be rolled back.</span></span>

 

 



