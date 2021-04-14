---
description: Security Support Provider Interface (SSPI) consente a un'applicazione di usare diversi modelli di sicurezza disponibili in un computer o in una rete senza modificare l'interfaccia del sistema di sicurezza.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modello SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401575"
---
# <a name="sspi-model"></a><span data-ttu-id="bd0a7-103">Modello SSPI</span><span class="sxs-lookup"><span data-stu-id="bd0a7-103">SSPI Model</span></span>

<span data-ttu-id="bd0a7-104">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) consente a un'applicazione di usare diversi modelli di sicurezza disponibili in un computer o in una rete senza modificare l'interfaccia del sistema di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bd0a7-104">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) allows an application to use various security models available on a computer or network without changing the interface to the security system.</span></span> <span data-ttu-id="bd0a7-105">SSPI non stabilisce [*credenziali*](../secgloss/c-gly.md) di accesso perché si tratta in genere di un'operazione con privilegi gestita dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bd0a7-105">SSPI does not establish logon [*credentials*](../secgloss/c-gly.md) because that is generally a privileged operation handled by the operating system.</span></span>

<span data-ttu-id="bd0a7-106">Una [*Security Support Provider*](../secgloss/s-gly.md) (SSP) è contenuta in una [*libreria di collegamento dinamico*](../secgloss/d-gly.md) (dll) che implementa SSPI rendendo disponibili per le applicazioni uno o più [*pacchetti di sicurezza*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bd0a7-106">A [*security support provider*](../secgloss/s-gly.md) (SSP) is contained in a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements SSPI by making one or more [*security packages*](../secgloss/s-gly.md) available to applications.</span></span> <span data-ttu-id="bd0a7-107">Ogni pacchetto di sicurezza fornisce mapping tra le chiamate di funzione SSPI di un'applicazione e le funzioni di un modello di sicurezza effettivo.</span><span class="sxs-lookup"><span data-stu-id="bd0a7-107">Each security package provides mappings between the SSPI function calls of an application and the functions of an actual security model.</span></span> <span data-ttu-id="bd0a7-108">I pacchetti di sicurezza supportano i [*protocolli di sicurezza*](../secgloss/s-gly.md) , ad esempio l'autenticazione [*Kerberos*](../secgloss/k-gly.md) e la gestione LAN.</span><span class="sxs-lookup"><span data-stu-id="bd0a7-108">Security packages support [*security protocols*](../secgloss/s-gly.md) such as [*Kerberos*](../secgloss/k-gly.md) authentication and LAN Manager.</span></span>

<span data-ttu-id="bd0a7-109">L'interfaccia SSPI è disponibile in modalità kernel e in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="bd0a7-109">The SSPI interface is available in kernel mode as well as user mode.</span></span> <span data-ttu-id="bd0a7-110">Per utilizzare la funzionalità SSPI in modalità kernel, è necessario installare il file System di Windows installabile con estensione DDK.</span><span class="sxs-lookup"><span data-stu-id="bd0a7-110">To use SSPI functionality in kernel mode, you must install the Windows Installable File System DDK.</span></span> <span data-ttu-id="bd0a7-111">Il modello chiamante rimane invariato, ma le considerazioni sulla modalità kernel sono indicate nelle pagine di riferimento per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="bd0a7-111">The calling model remains the same, but kernel mode considerations are noted on function reference pages.</span></span> <span data-ttu-id="bd0a7-112">Per ulteriori informazioni, vedere [funzioni SSPI](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="bd0a7-112">For more information, see [SSPI Functions](authentication-functions.md).</span></span>

 

 
