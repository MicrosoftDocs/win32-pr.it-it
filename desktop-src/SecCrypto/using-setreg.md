---
description: Lo strumento SetReg imposta il valore delle chiavi del registro di sistema che controllano il comportamento del processo di verifica del certificato Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Uso di SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130238"
---
# <a name="using-setreg"></a><span data-ttu-id="d9e7b-103">Uso di SetReg</span><span class="sxs-lookup"><span data-stu-id="d9e7b-103">Using SetReg</span></span>

<span data-ttu-id="d9e7b-104">Lo strumento SetReg imposta il valore delle chiavi del registro di sistema che controllano il comportamento del processo di verifica del certificato Authenticode.</span><span class="sxs-lookup"><span data-stu-id="d9e7b-104">The SetReg tool sets the value of the registry keys controlling the behavior of the Authenticode certificate verification process.</span></span> <span data-ttu-id="d9e7b-105">Queste chiavi, denominate chiavi di stato di pubblicazione software, controllano se considerare attendibile una radice di test, consentire l'approvazione offline dei certificati, verificare le date di scadenza del certificato ed eseguire controlli di revoca.</span><span class="sxs-lookup"><span data-stu-id="d9e7b-105">These keys, called the Software Publishing State Keys, control whether to trust a test root, allow offline approval of certificates, test certificate expiration dates, and perform revocation checks.</span></span>

<span data-ttu-id="d9e7b-106">Il comando seguente elenca la sintassi e le opzioni per l'uso di SetReg.</span><span class="sxs-lookup"><span data-stu-id="d9e7b-106">The following command lists the syntax and options for using SetReg.</span></span>

<span data-ttu-id="d9e7b-107">**setreg-?**</span><span class="sxs-lookup"><span data-stu-id="d9e7b-107">**setreg -?**</span></span>

<span data-ttu-id="d9e7b-108">Il seguente comando rende attendibile la radice del test.</span><span class="sxs-lookup"><span data-stu-id="d9e7b-108">The following command makes a test root trusted.</span></span> <span data-ttu-id="d9e7b-109">Per impostazione predefinita, una radice di test non è attendibile.</span><span class="sxs-lookup"><span data-stu-id="d9e7b-109">By default, a test root is not trusted.</span></span> <span data-ttu-id="d9e7b-110">Dopo aver apportato le modifiche ai valori di chiave, viene visualizzato un elenco del valore corrente di tutti i valori di chiave.</span><span class="sxs-lookup"><span data-stu-id="d9e7b-110">After any changes in the key values are made, a list of the current value of all of the key values is displayed.</span></span> <span data-ttu-id="d9e7b-111">Se si usa l'opzione **-q** , i valori di chiave non vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="d9e7b-111">If the **-q** option is used, the key values are not displayed.</span></span>

<span data-ttu-id="d9e7b-112">**setreg 1 TRUE**</span><span class="sxs-lookup"><span data-stu-id="d9e7b-112">**setreg 1 TRUE**</span></span>

<span data-ttu-id="d9e7b-113">Il seguente comando rende una radice di test non attendibile e determina la revoca di tutti i controlli.</span><span class="sxs-lookup"><span data-stu-id="d9e7b-113">The following command makes a test root untrusted and causes all verification to check for revocation.</span></span> <span data-ttu-id="d9e7b-114">L'opzione **-q** viene usata in modo che l'elenco di valori di chiave non venga visualizzato</span><span class="sxs-lookup"><span data-stu-id="d9e7b-114">The **-q** option is used so that the list of key values is not displayed</span></span>

<span data-ttu-id="d9e7b-115">**setreg-q 1 FALSE 3 TRUE**</span><span class="sxs-lookup"><span data-stu-id="d9e7b-115">**setreg -q 1 FALSE 3 TRUE**</span></span>

> [!Note]  
> <span data-ttu-id="d9e7b-116">I comandi, le opzioni e gli argomenti non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d9e7b-116">Commands, options, and arguments are not case sensitive.</span></span>

 

 

 



