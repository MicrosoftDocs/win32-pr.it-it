---
title: Installazione EAP
description: I fornitori implementano EAPs, noti anche come protocolli di autenticazione, nelle librerie a collegamento dinamico (dll).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398338"
---
# <a name="eap-installation"></a><span data-ttu-id="146e1-103">Installazione EAP</span><span class="sxs-lookup"><span data-stu-id="146e1-103">EAP Installation</span></span>

<span data-ttu-id="146e1-104">I fornitori implementano EAPs, noti anche come protocolli di autenticazione, nelle librerie a collegamento dinamico (dll).</span><span class="sxs-lookup"><span data-stu-id="146e1-104">Vendors implement EAPs, also known as authentication protocols, in dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="146e1-105">Una DLL per il protocollo di autenticazione deve risiedere sia nei computer client che nei computer server.</span><span class="sxs-lookup"><span data-stu-id="146e1-105">A DLL for the authentication protocol must reside on both the client and server computers.</span></span> <span data-ttu-id="146e1-106">Per semplicità, le dll del client e del server possono essere identiche. Tuttavia, questo non è un requisito.</span><span class="sxs-lookup"><span data-stu-id="146e1-106">For simplicity, the client and server DLLs may be identical; however, this is not a requirement.</span></span> <span data-ttu-id="146e1-107">Tenere inoltre presente che la stessa DLL può supportare più di un protocollo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="146e1-107">Also, be aware that the same DLL may support more than one authentication protocol.</span></span>

<span data-ttu-id="146e1-108">Il fornitore deve fornire il software di installazione per installare e rimuovere la DLL.</span><span class="sxs-lookup"><span data-stu-id="146e1-108">The vendor should provide setup software to install and remove the DLL.</span></span> <span data-ttu-id="146e1-109">Il software di installazione deve inoltre creare le chiavi e i valori appropriati per il protocollo di autenticazione nel registro di sistema e rimuoverli al momento della disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="146e1-109">The setup software should also create the appropriate keys and values for the authentication protocol in the system registry and remove them upon uninstall.</span></span>

<span data-ttu-id="146e1-110">L'installazione di ogni DLL EAP deve creare la seguente chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="146e1-110">The installation of each EAP DLL should create the following registry key.</span></span>

<span data-ttu-id="146e1-111">**HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** \\ **RASMAN** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**</span><span class="sxs-lookup"><span data-stu-id="146e1-111">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Rasman**\\**PPP**\\**EAP**\\**&lt;eaptypeid&gt;**</span></span>

<span data-ttu-id="146e1-112">Nel percorso precedente **&lt; eaptypeid &gt;** è l'ID del protocollo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="146e1-112">In the preceding path, **&lt;eaptypeid&gt;** is the ID of the authentication protocol.</span></span> <span data-ttu-id="146e1-113">Il fornitore deve ottenere questo ID da IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="146e1-113">The vendor must obtain this ID from the Internet Assigned Numbers Authority (IANA).</span></span>

<span data-ttu-id="146e1-114">Per ulteriori informazioni e per una descrizione dei valori supportati per questa chiave, vedere [autenticazione del registro di sistema dei valori](authentication-protocol-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="146e1-114">For more information and a description of the supported values for this key, see [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).</span></span>

 

 




