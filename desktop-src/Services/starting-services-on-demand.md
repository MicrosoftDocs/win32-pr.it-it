---
description: L'utente può avviare un servizio con l'utilità pannello di controllo servizi. L'utente può specificare gli argomenti per il servizio nel campo parametri di avvio. Un programma di controllo del servizio può avviare un servizio e specificare i relativi argomenti con la funzione StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Avvio dei servizi su richiesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317668"
---
# <a name="starting-services-on-demand"></a><span data-ttu-id="30321-105">Avvio dei servizi su richiesta</span><span class="sxs-lookup"><span data-stu-id="30321-105">Starting Services on Demand</span></span>

<span data-ttu-id="30321-106">L'utente può avviare un servizio con l'utilità pannello di controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="30321-106">The user can start a service with the Services control panel utility.</span></span> <span data-ttu-id="30321-107">L'utente può specificare gli argomenti per il servizio nel campo **parametri di avvio** .</span><span class="sxs-lookup"><span data-stu-id="30321-107">The user can specify arguments for the service in the **Start parameters** field.</span></span> <span data-ttu-id="30321-108">Un programma di controllo del servizio può avviare un servizio e specificare i relativi argomenti con la funzione [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="30321-108">A service control program can start a service and specify its arguments with the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function.</span></span>

<span data-ttu-id="30321-109">Quando il servizio viene avviato, SCM esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="30321-109">When the service is started, the SCM performs the following steps:</span></span>

-   <span data-ttu-id="30321-110">Recuperare le informazioni sull'account archiviate nel database.</span><span class="sxs-lookup"><span data-stu-id="30321-110">Retrieve the account information stored in the database.</span></span>
-   <span data-ttu-id="30321-111">Accedere all'account del servizio.</span><span class="sxs-lookup"><span data-stu-id="30321-111">Log on the service account.</span></span>
-   <span data-ttu-id="30321-112">Caricare il profilo utente.</span><span class="sxs-lookup"><span data-stu-id="30321-112">Load the user profile.</span></span>
-   <span data-ttu-id="30321-113">Creare il servizio nello stato Suspended.</span><span class="sxs-lookup"><span data-stu-id="30321-113">Create the service in the suspended state.</span></span>
-   <span data-ttu-id="30321-114">Assegnare il token di accesso al processo.</span><span class="sxs-lookup"><span data-stu-id="30321-114">Assign the logon token to the process.</span></span>
-   <span data-ttu-id="30321-115">Consente l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="30321-115">Allow the process to execute.</span></span>

 

 



