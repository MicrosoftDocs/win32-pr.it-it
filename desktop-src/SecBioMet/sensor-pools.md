---
title: Pool di sensori
description: Descrive tre possibili pool di sensori di sistema, privati e non assegnati.
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399261"
---
# <a name="sensor-pools"></a><span data-ttu-id="c7dda-103">Pool di sensori</span><span class="sxs-lookup"><span data-stu-id="c7dda-103">Sensor Pools</span></span>

<span data-ttu-id="c7dda-104">Per supportare sia gli scenari di autenticazione di Windows che l'autenticazione definita dal fornitore, il servizio biometrico di Windows organizza le unità biometriche in tre possibili pool di sensori:</span><span class="sxs-lookup"><span data-stu-id="c7dda-104">To support both Windows authentication scenarios and vendor defined authentication, the Windows Biometric service organizes biometric units into three possible sensor pools:</span></span>

-   <span data-ttu-id="c7dda-105">**Pool privato** raccolta di unità biometriche allocate per l'utilizzo esclusivo da un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="c7dda-105">**Private pool** a collection of biometric units allocated for exclusive use by a client application.</span></span> <span data-ttu-id="c7dda-106">I pool privati possono supportare scenari di autenticazione che non sono basati su Windows e consentono a un'applicazione di accedere all'hardware di un'unità biometrica in modo definito dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="c7dda-106">Private pools can support authentication scenarios that are not Windows-based, and they make it possible for an application to access the hardware of a biometric unit in a vendor-defined fashion.</span></span> <span data-ttu-id="c7dda-107">Nel sistema possono essere presenti molti pool di sensori privati, perché sono presenti unità biometriche.</span><span class="sxs-lookup"><span data-stu-id="c7dda-107">There can be as many private sensor pools on the system as there are biometric units.</span></span>
-   <span data-ttu-id="c7dda-108">Il **pool di sensori di sistema** è una raccolta di unità biometriche condivisibili che consentono di accedere ai servizi di autenticazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="c7dda-108">**System sensor pool** a collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="c7dda-109">Questo pool viene usato da Winlogon, UAC e da qualsiasi altro client che associa un SID a un modello biometrico specifico.</span><span class="sxs-lookup"><span data-stu-id="c7dda-109">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span> <span data-ttu-id="c7dda-110">Ogni provider di servizi biometrico ha un pool di sensori di sistema.</span><span class="sxs-lookup"><span data-stu-id="c7dda-110">Each biometric service provider has one system sensor pool.</span></span>
-   <span data-ttu-id="c7dda-111">Il **pool non assegnato** contiene una raccolta (possibilmente vuota) di unità biometriche che non sono assegnate al pool di sistema o al pool privato.</span><span class="sxs-lookup"><span data-stu-id="c7dda-111">**Unassigned pool** contains a (possibly empty) collection of biometric units that are not assigned to either the system pool or the private pool.</span></span>

<span data-ttu-id="c7dda-112">Le applicazioni possono usare il pool di sistema condiviso oppure creare un pool privato costituito da unità biometriche rimosse dal sistema o da pool non assegnati.</span><span class="sxs-lookup"><span data-stu-id="c7dda-112">Applications can use the shared system pool or they can create a private pool made up of biometric units removed from the system or unassigned pools.</span></span> <span data-ttu-id="c7dda-113">Quando un'applicazione rilascia il proprio pool privato, le unità biometriche vengono riconfigurate e restituite ai pool originali.</span><span class="sxs-lookup"><span data-stu-id="c7dda-113">When an application releases its private pool, the biometric units are reconfigured and returned to their original pools.</span></span> <span data-ttu-id="c7dda-114">Per evitare attacchi di tipo Denial of Service, solo gli utenti con privilegi possono rimuovere l'ultimo sensore dal pool di sistema.</span><span class="sxs-lookup"><span data-stu-id="c7dda-114">To prevent denial of service attacks, only privileged users are permitted to remove the last sensor from the system pool.</span></span> <span data-ttu-id="c7dda-115">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="c7dda-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c7dda-116">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c7dda-116">In this section</span></span>



| <span data-ttu-id="c7dda-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="c7dda-117">Topic</span></span>                                                       | <span data-ttu-id="c7dda-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7dda-118">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7dda-119">Pool di sensori privati</span><span class="sxs-lookup"><span data-stu-id="c7dda-119">Private Sensor Pool</span></span>](private-sensor-pool.md)<br/>   | <span data-ttu-id="c7dda-120">Raccolta di unità biometriche riservate per l'utilizzo esclusivo da un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="c7dda-120">A collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="c7dda-121">I pool privati supportano i metodi di autenticazione proprietari e consentono a un'applicazione client di accedere a un'unità biometrica usando i comandi di controllo specificati dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="c7dda-121">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span><br/> |
| [<span data-ttu-id="c7dda-122">Pool di sensori di sistema</span><span class="sxs-lookup"><span data-stu-id="c7dda-122">System Sensor Pool</span></span>](system-sensor-pool.md)<br/>     | <span data-ttu-id="c7dda-123">Raccolta di unità biometriche condivisibili che consentono di accedere ai servizi di autenticazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="c7dda-123">A collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="c7dda-124">Questo pool viene usato da Winlogon, UAC e da qualsiasi altro client che associa un SID a un modello biometrico specifico.</span><span class="sxs-lookup"><span data-stu-id="c7dda-124">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span><br/>                                 |
| [<span data-ttu-id="c7dda-125">Comportamento del pool di sistema</span><span class="sxs-lookup"><span data-stu-id="c7dda-125">System Pool Behavior</span></span>](system-pool-behavior.md)<br/> | <span data-ttu-id="c7dda-126">Discussione sulle azioni eseguite dal pool di sistema quando si inviano notifiche degli eventi e quando non sono in sospeso operazioni biometriche.</span><span class="sxs-lookup"><span data-stu-id="c7dda-126">Discussion about the actions taken by the system pool when event notices are sent and when no biometric operations are pending.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="c7dda-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7dda-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7dda-128">Informazioni sull'API Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="c7dda-128">About the Windows Biometric Framework API</span></span>](./biometric-service-api-portal.md)
</dt> </dl>

 

