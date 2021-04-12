---
title: Abilitazione di informazioni estese sugli errori
description: Abilitazione di informazioni estese sugli errori per RPC (Remote Procedure Call).
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221688"
---
# <a name="enabling-extended-error-information"></a><span data-ttu-id="4333b-103">Abilitazione di informazioni estese sugli errori</span><span class="sxs-lookup"><span data-stu-id="4333b-103">Enabling Extended Error Information</span></span>

<span data-ttu-id="4333b-104">Per abilitare le informazioni estese sugli errori, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="4333b-104">To enable extended error information, take the following steps:</span></span>

<span data-ttu-id="4333b-105">Aprire i criteri del computer locale usando l'interfaccia gpedit. msc.</span><span class="sxs-lookup"><span data-stu-id="4333b-105">Open the local machine policy using the gpedit.msc interface.</span></span>

<span data-ttu-id="4333b-106">Passare al criterio individuato in configurazione computer/Modelli amministrativi/sistema/chiamata procedura remota/supporto per la risoluzione dei problemi RPC/propagazione delle informazioni sugli errori estesi</span><span class="sxs-lookup"><span data-stu-id="4333b-106">Navigate to the policy located at Computer Configuration/Administrative Templates/System/Remote Procedure Call/Rpc Troubleshooting Support/Propagation of extended error information</span></span>

<span data-ttu-id="4333b-107">Abilitare i criteri e impostare la **propagazione dei campi delle informazioni sugli errori estesi** su "on".</span><span class="sxs-lookup"><span data-stu-id="4333b-107">Enable the policy, and set the field **Propagation of extended error information** to "On".</span></span>

<span data-ttu-id="4333b-108">Questo processo converte la propagazione delle informazioni di errore estese in per tutti i processi nel computer.</span><span class="sxs-lookup"><span data-stu-id="4333b-108">This process turns the propagation of extended error information on for all processes on the machine.</span></span>

<span data-ttu-id="4333b-109">Per abilitare le informazioni estese sugli errori solo per determinati processi in un computer o per disabilitarlo solo per determinati processi nel computer, utilizzare le opzioni **disattivata con eccezioni** o **con eccezioni** .</span><span class="sxs-lookup"><span data-stu-id="4333b-109">To enable extended error information for only certain processes on a computer, or to disable it for only certain processes on the computer, use the **Off with exceptions** or **On with exceptions** options.</span></span> <span data-ttu-id="4333b-110">Entrambe le opzioni utilizzano le **eccezioni delle informazioni sugli errori estesi** del campo per specificare i processi che hanno l'impostazione predefinita e i processi che hanno il contrario rispetto all'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4333b-110">Both options use the field **Extended Error Information Exceptions** to specify which processes have the default setting, and which processes have the opposite of the default setting.</span></span> <span data-ttu-id="4333b-111">**Le eccezioni delle informazioni sugli errori estesi** contengono un elenco di nomi di processo.</span><span class="sxs-lookup"><span data-stu-id="4333b-111">**Extended Error Information Exceptions** contains a list of process names.</span></span>

<span data-ttu-id="4333b-112">Se la riga di comando di un processo inizia con una stringa che si trova nelle **eccezioni delle informazioni di errore estese**, il processo riceverà il contrario rispetto all'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4333b-112">If the command line of a process starts with a string that is in the **Extended Error Information Exceptions**, the process will receive the opposite of the default setting.</span></span> <span data-ttu-id="4333b-113">Se, ad esempio, si desidera che tutti i processi nel computer propaghino informazioni estese sugli errori, ad eccezione di LSASS e del processo denominato **server protetto**, impostare la **propagazione delle informazioni sugli errori estesi** su **on con le eccezioni** e specificare nel campo eccezioni per le **informazioni sugli errori** estesi la stringa seguente: lsass "server protetto".</span><span class="sxs-lookup"><span data-stu-id="4333b-113">For example, if you want all the process on your computer to propagate extended error information, except for lsass and the process called **Secure Server**, set the **Propagation of extended error information** to **On with exceptions**, and specify in the **Extended Error Information Exceptions** field the following string: lsass "Secure Server".</span></span>

<span data-ttu-id="4333b-114">Le stringhe possono essere racchiuse tra virgolette doppie, ma questa operazione è facoltativa se non sono presenti spazi nella stringa.</span><span class="sxs-lookup"><span data-stu-id="4333b-114">Strings can be enclosed with double quotes, but doing so is optional if there are no spaces in the string.</span></span> <span data-ttu-id="4333b-115">Inoltre, è possibile specificare l'inizio della riga di comando del processo.</span><span class="sxs-lookup"><span data-stu-id="4333b-115">Also, the beginning of the process command line can be specified.</span></span> <span data-ttu-id="4333b-116">Se, ad esempio, si specifica **off con le eccezioni** nella **propagazione del campo informazioni sugli errori estesi** e nel campo eccezioni per le **informazioni sugli errori estesi** , viene specificato quanto segue: Win.</span><span class="sxs-lookup"><span data-stu-id="4333b-116">For example, if **Off with exceptions** is specified in the **Propagation of extended error information** field, and in the **Extended Error Information Exceptions** field the following is specified: win.</span></span>

<span data-ttu-id="4333b-117">Ogni processo che inizia con "Win" propaga le informazioni estese sull'errore.</span><span class="sxs-lookup"><span data-stu-id="4333b-117">Each process that begins with "win" propagates extended error information.</span></span> <span data-ttu-id="4333b-118">In molti computer, ad esempio, questi processi sarebbero winlogon.exe e WINWORD.EXE.</span><span class="sxs-lookup"><span data-stu-id="4333b-118">On many computers, for example, those processes would be winlogon.exe and WINWORD.EXE.</span></span>

 

 




