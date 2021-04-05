---
title: Rilevamento della modalità operativa di un dominio
description: In Windows 2000, un dominio può essere eseguito in due modalità operative miste e native.
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- Rilevamento della modalità operativa di un dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872325"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a><span data-ttu-id="740f1-104">Rilevamento della modalità operativa di un dominio</span><span class="sxs-lookup"><span data-stu-id="740f1-104">Detecting the Operation Mode of a Domain</span></span>

<span data-ttu-id="740f1-105">In Windows 2000, un dominio può essere eseguito in due modalità operative: misto e nativo.</span><span class="sxs-lookup"><span data-stu-id="740f1-105">In Windows 2000, a domain can run in two operation modes: mixed and native.</span></span> <span data-ttu-id="740f1-106">Utilizzare la modalità mista per includere i controller di dominio che eseguono Windows NT 4,0 in un dominio Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="740f1-106">Mixed mode should be used to include domain controllers running Windows NT 4.0 in a Windows 2000 domain.</span></span> <span data-ttu-id="740f1-107">La modalità mista non supporta i gruppi universali o i gruppi annidati.</span><span class="sxs-lookup"><span data-stu-id="740f1-107">Mixed mode does not support universal groups or nested groups.</span></span> <span data-ttu-id="740f1-108">Se tutti i controller di dominio nel dominio eseguono Windows 2000, è possibile utilizzare la modalità nativa.</span><span class="sxs-lookup"><span data-stu-id="740f1-108">If all domain controllers in the domain are running Windows 2000, you can use native mode.</span></span>

<span data-ttu-id="740f1-109">Per rilevare a livello di codice la modalità operativa di un dominio di Windows 2000, leggere la proprietà [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) dell'oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) per quel dominio.</span><span class="sxs-lookup"><span data-stu-id="740f1-109">To programmatically detect the operation mode of a Windows 2000 domain, read the [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) property of the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object for that domain.</span></span> <span data-ttu-id="740f1-110">Il valore zero (0) indica che il dominio è in modalità nativa.</span><span class="sxs-lookup"><span data-stu-id="740f1-110">A value of zero (0) means that the domain is in native mode.</span></span> <span data-ttu-id="740f1-111">Un valore pari a uno (1) indica che il dominio è in modalità mista.</span><span class="sxs-lookup"><span data-stu-id="740f1-111">A value of one (1) indicates that the domain is in mixed mode.</span></span> <span data-ttu-id="740f1-112">È anche possibile usare la funzione [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) per ottenere la modalità operativa, nonché altri dati sul dominio e il relativo stato.</span><span class="sxs-lookup"><span data-stu-id="740f1-112">You can also use the [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) function to get the operation mode as well as other data about the domain and its state.</span></span>

<span data-ttu-id="740f1-113">Per eseguire il binding all'oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) del dominio dell'account utente con cui è in esecuzione l'applicazione, usare binding senza server e RootDSE per ottenere il nome distinto per il dominio e quindi usare tale nome distinto per l'associazione all'oggetto **domainDNS** che rappresenta tale dominio.</span><span class="sxs-lookup"><span data-stu-id="740f1-113">To bind to the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object of the domain of the user account under which your application is running, use serverless binding and rootDSE to get the distinguished name for the domain and then use that distinguished name to bind to the **domainDNS** object that represents that domain.</span></span> <span data-ttu-id="740f1-114">Per ulteriori informazioni sull'associazione senza server e rootDSE, vedere [binding senza server e RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="740f1-114">For more information about serverless binding and rootDSE, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="740f1-115">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come rilevare a livello di codice la modalità operativa di un dominio, vedere [il codice di esempio per determinare la modalità operativa](example-code-for-determining-the-operation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="740f1-115">For more information and a code example that shows how to programmatically detect the operation mode of a domain, see [Example Code for Determining the Operation Mode](example-code-for-determining-the-operation-mode.md).</span></span>

 

 