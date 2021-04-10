---
title: Connessione al computer SDO
description: Con il puntatore di interfaccia restituito da CoCreateInstance, chiamare il metodo di associazione ISdoMachine.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963158"
---
# <a name="attaching-to-the-sdo-computer"></a><span data-ttu-id="2aa6c-103">Connessione al computer SDO</span><span class="sxs-lookup"><span data-stu-id="2aa6c-103">Attaching to the SDO Computer</span></span>

<span data-ttu-id="2aa6c-104">Con il puntatore di interfaccia restituito da [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), chiamare il metodo [**ISdoMachine:: alconnessione**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) .</span><span class="sxs-lookup"><span data-stu-id="2aa6c-104">With the interface pointer returned by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), call the [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) method.</span></span> <span data-ttu-id="2aa6c-105">Passare **null** come parametro al metodo di **connessione** .</span><span class="sxs-lookup"><span data-stu-id="2aa6c-105">Pass **NULL** as the parameter to the **Attach** method.</span></span> <span data-ttu-id="2aa6c-106">Il valore **null** **specifica che associa associare l'** oggetto computer al computer locale.</span><span class="sxs-lookup"><span data-stu-id="2aa6c-106">The value **NULL** specifies that **Attach** associate the machine object with the local computer.</span></span> <span data-ttu-id="2aa6c-107">La connessione a un computer remoto non è supportata.</span><span class="sxs-lookup"><span data-stu-id="2aa6c-107">Attaching to a remote computer is not supported.</span></span>

<span data-ttu-id="2aa6c-108">Per determinare se il computer locale è già collegato, chiamare il metodo [**ISdoMachine:: GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .</span><span class="sxs-lookup"><span data-stu-id="2aa6c-108">To determine if the local computer is already attached, call the [**ISdoMachine::GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) method.</span></span>

<span data-ttu-id="2aa6c-109">Vedere [connessione a un computer SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) per il codice di esempio che illustra come connettersi al computer locale.</span><span class="sxs-lookup"><span data-stu-id="2aa6c-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to attach to the local computer.</span></span>

 

 