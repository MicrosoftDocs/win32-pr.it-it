---
title: Ottenere un'identità di codifica
description: Un'applicazione che decodifica i dati codificati può ottenere l'identità della routine utilizzata per codificare i dati, prima di chiamare una routine per decodificarla. La routine MesInqProcEncodingId fornisce questa identità.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- RPC (Remote Procedure Call), attività, acquisizione dell'identità di codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713072"
---
# <a name="obtaining-an-encoding-identity"></a><span data-ttu-id="19b78-105">Ottenere un'identità di codifica</span><span class="sxs-lookup"><span data-stu-id="19b78-105">Obtaining an Encoding Identity</span></span>

<span data-ttu-id="19b78-106">Un'applicazione che decodifica i dati codificati può ottenere l'identità della routine utilizzata per codificare i dati, prima di chiamare una routine per decodificarla.</span><span class="sxs-lookup"><span data-stu-id="19b78-106">An application that is decoding encoded data can obtain the identity of the routine used to encode the data, prior to calling a routine to decode it.</span></span> <span data-ttu-id="19b78-107">La routine [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) fornisce questa identità.</span><span class="sxs-lookup"><span data-stu-id="19b78-107">The [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) routine provides this identity.</span></span>

<span data-ttu-id="19b78-108">A ogni procedura di un'interfaccia viene assegnato un numero di identificazione intero, detto *identificatore di routine* o *ID proc*, dal compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="19b78-108">Each procedure in an interface is assigned an integer identification number, called a *procedure identifier* or a *proc ID*, by the MIDL compiler.</span></span> <span data-ttu-id="19b78-109">La numerazione inizia con zero.</span><span class="sxs-lookup"><span data-stu-id="19b78-109">Numbering begins with zero.</span></span> <span data-ttu-id="19b78-110">Le librerie di runtime RPC non sono necessarie per tradurre l'ID procedura in una chiamata di procedura effettiva.</span><span class="sxs-lookup"><span data-stu-id="19b78-110">The RPC run-time libraries are not involved in translating the procedure ID into an actual procedure call.</span></span> <span data-ttu-id="19b78-111">Dato un ID proc, l'applicazione deve fornire un metodo per chiamare la procedura corretta.</span><span class="sxs-lookup"><span data-stu-id="19b78-111">Given a proc ID, your application must provide a means of calling the correct procedure.</span></span> <span data-ttu-id="19b78-112">In genere, gli sviluppatori di applicazioni utilizzano una serie di istruzioni **if** oppure, quando si utilizza C/C++, un'istruzione **Switch** a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="19b78-112">Typically, application developers use a series of **if** statements, or (when using C/C++) a **switch** statement for this purpose.</span></span>

 

 




