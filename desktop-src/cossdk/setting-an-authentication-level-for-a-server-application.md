---
description: Quando si imposta un livello di autenticazione per un'applicazione, è necessario determinare il grado di autenticazione eseguito quando i client eseguono chiamate nell'applicazione.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Impostazione di un livello di autenticazione per un'applicazione server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304937"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a><span data-ttu-id="b22ed-103">Impostazione di un livello di autenticazione per un'applicazione server</span><span class="sxs-lookup"><span data-stu-id="b22ed-103">Setting an Authentication Level for a Server Application</span></span>

<span data-ttu-id="b22ed-104">Quando si imposta un livello di autenticazione per un'applicazione, è necessario determinare il grado di autenticazione eseguito quando i client eseguono chiamate nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b22ed-104">When you set an authentication level for an application, you determine what degree of authentication is performed when clients call into the application.</span></span> <span data-ttu-id="b22ed-105">Livelli di autenticazione più elevati offrono maggiore sicurezza e integrità dei dati, anche se in genere si verifica un calo delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b22ed-105">Higher authentication levels provide greater security and data integrity, although usually with some performance degradation.</span></span> <span data-ttu-id="b22ed-106">Per ulteriori informazioni, vedere [autenticazione client](client-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="b22ed-106">For more information, see [Client Authentication](client-authentication.md).</span></span>

<span data-ttu-id="b22ed-107">**Per selezionare un livello di autenticazione per un'applicazione server**</span><span class="sxs-lookup"><span data-stu-id="b22ed-107">**To select an authentication level for a server application**</span></span>

1.  <span data-ttu-id="b22ed-108">Fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si sta impostando l'autenticazione, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="b22ed-108">Right-click the COM+ application for which you are setting authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="b22ed-109">Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="b22ed-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="b22ed-110">Nella casella **livello di autenticazione per le chiamate** selezionare il livello appropriato.</span><span class="sxs-lookup"><span data-stu-id="b22ed-110">In the **Authentication level for calls** box, select the appropriate level.</span></span> <span data-ttu-id="b22ed-111">I livelli sono i seguenti, ordinati dalla sicurezza più bassa alla più alta:</span><span class="sxs-lookup"><span data-stu-id="b22ed-111">The levels are as follows, ordered from lowest to highest security:</span></span>

    -   <span data-ttu-id="b22ed-112">**Nessuno**.</span><span class="sxs-lookup"><span data-stu-id="b22ed-112">**None**.</span></span> <span data-ttu-id="b22ed-113">Non viene eseguita alcuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b22ed-113">No authentication occurs.</span></span>
    -   <span data-ttu-id="b22ed-114">**Connettersi**.</span><span class="sxs-lookup"><span data-stu-id="b22ed-114">**Connect**.</span></span> <span data-ttu-id="b22ed-115">Autentica le credenziali solo quando viene eseguita la connessione.</span><span class="sxs-lookup"><span data-stu-id="b22ed-115">Authenticates credentials only when the connection is made.</span></span>
    -   <span data-ttu-id="b22ed-116">**Chiamare**.</span><span class="sxs-lookup"><span data-stu-id="b22ed-116">**Call**.</span></span> <span data-ttu-id="b22ed-117">Autentica le credenziali all'inizio di ciascuna chiamata.</span><span class="sxs-lookup"><span data-stu-id="b22ed-117">Authenticates credentials at the beginning of every call.</span></span>
    -   <span data-ttu-id="b22ed-118">**Pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="b22ed-118">**Packet**.</span></span> <span data-ttu-id="b22ed-119">Autentica le credenziali e verifica la ricezione di tutti i dati della chiamata.</span><span class="sxs-lookup"><span data-stu-id="b22ed-119">Authenticates credentials and verifies that all call data is received.</span></span> <span data-ttu-id="b22ed-120">Si tratta dell'impostazione predefinita per le applicazioni server COM+.</span><span class="sxs-lookup"><span data-stu-id="b22ed-120">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="b22ed-121">**Integrità dei pacchetti**.</span><span class="sxs-lookup"><span data-stu-id="b22ed-121">**Packet Integrity**.</span></span> <span data-ttu-id="b22ed-122">Autentica le credenziali e verifica che nessuna chiamata di dati sia stata modificata durante il passaggio.</span><span class="sxs-lookup"><span data-stu-id="b22ed-122">Authenticates credentials and verifies that no call data has been modified in transit.</span></span>
    -   <span data-ttu-id="b22ed-123">**Privacy del pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="b22ed-123">**Packet Privacy**.</span></span> <span data-ttu-id="b22ed-124">Autentica le credenziali e codifica il pacchetto, includendo i dati e l'identità e la firma del mittente.</span><span class="sxs-lookup"><span data-stu-id="b22ed-124">Authenticates credentials and encrypts the packet, including the data and the sender's identity and signature.</span></span>

4.  <span data-ttu-id="b22ed-125">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="b22ed-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b22ed-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b22ed-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b22ed-127">Abilitazione dell'autenticazione per un'applicazione di libreria</span><span class="sxs-lookup"><span data-stu-id="b22ed-127">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



