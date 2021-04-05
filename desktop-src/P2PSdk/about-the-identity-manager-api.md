---
description: L'API peer Identity Manager consente di creare, enumerare e modificare le identità dei peer in un'applicazione peer.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Informazioni su Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881818"
---
# <a name="about-identity-manager"></a><span data-ttu-id="40b3a-103">Informazioni su Identity Manager</span><span class="sxs-lookup"><span data-stu-id="40b3a-103">About Identity Manager</span></span>

<span data-ttu-id="40b3a-104">L'API peer Identity Manager consente di creare, enumerare e modificare le identità dei peer in un'applicazione peer.</span><span class="sxs-lookup"><span data-stu-id="40b3a-104">The Peer Identity Manager API allows you to create, enumerate, and manipulate peer identities in a peer application.</span></span> <span data-ttu-id="40b3a-105">È possibile utilizzare le identità peer create utilizzando questa API come input per il raggruppamento peer e le API del provider dello spazio dei nomi PNRP (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="40b3a-105">You can use the peer identities created using this API as input for the Peer Grouping and Peer Name Resolution Protocol (PNRP) Namespace Provider APIs.</span></span>

## <a name="peer-identity-manager-best-practices"></a><span data-ttu-id="40b3a-106">Procedure consigliate per peer Identity Manager</span><span class="sxs-lookup"><span data-stu-id="40b3a-106">Peer Identity Manager Best Practices</span></span>

<span data-ttu-id="40b3a-107">Ogni utente deve avere alcune identità peer che possono usare per le attività peer.</span><span class="sxs-lookup"><span data-stu-id="40b3a-107">Each user should have a few peer identities that they can use for the peer activities.</span></span> <span data-ttu-id="40b3a-108">Ad esempio, un utente potrebbe avere due identità peer per lavoro e svago.</span><span class="sxs-lookup"><span data-stu-id="40b3a-108">For example, a user might have two peer identities for work and leisure.</span></span>

<span data-ttu-id="40b3a-109">Un'applicazione peer ben progettata consente a un utente di selezionare un'identità peer da usare.</span><span class="sxs-lookup"><span data-stu-id="40b3a-109">A well-designed peer application allows a user to select a peer identity to use.</span></span> <span data-ttu-id="40b3a-110">Un utente può creare una nuova identità peer se nessuna delle identità peer esistenti è appropriata per l'uso con un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40b3a-110">A user can create a new peer identity if none of the existing peer identities are appropriate to use with an application.</span></span>

<span data-ttu-id="40b3a-111">Un'applicazione peer ben progettata controlla anche il numero di identità create.</span><span class="sxs-lookup"><span data-stu-id="40b3a-111">A well-designed peer application also controls the number of identities that it creates.</span></span> <span data-ttu-id="40b3a-112">Se un'applicazione crea un'identità peer temporanea, l'applicazione deve eliminare l'identità peer quando l'identità non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="40b3a-112">If an application creates a temporary peer identity, the application must delete the peer identity when the identity is not needed.</span></span> <span data-ttu-id="40b3a-113">Se un'applicazione non esegue questa manutenzione, il gestore di identità peer potrebbe non essere in grado di creare identità peer finché alcune identità peer non vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="40b3a-113">If an application does not perform this maintenance, the Peer Identity Manager may not be able to create peer identities until some peer identities are removed.</span></span>

 

 



