---
title: Flag di test
description: Flag di test
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- Flag di MCI_TEST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332527"
---
# <a name="the-test-flag"></a><span data-ttu-id="546be-104">Flag di test</span><span class="sxs-lookup"><span data-stu-id="546be-104">The Test Flag</span></span>

<span data-ttu-id="546be-105">Il flag "test" ( \_ test MCI) esegue una query sul dispositivo per determinare se può eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="546be-105">The "test" (MCI\_TEST) flag queries the device to determine if it can execute the command.</span></span> <span data-ttu-id="546be-106">Il dispositivo restituisce un errore se non è possibile eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="546be-106">The device returns an error if it cannot execute the command.</span></span> <span data-ttu-id="546be-107">Non restituisce alcun errore se può gestire il comando.</span><span class="sxs-lookup"><span data-stu-id="546be-107">It returns no error if it can handle the command.</span></span> <span data-ttu-id="546be-108">Quando si specifica questo flag, MCI restituisce il controllo all'applicazione senza eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="546be-108">When you specify this flag, MCI returns control to the application without executing the command.</span></span>

<span data-ttu-id="546be-109">Questo flag è supportato dai dispositivi Digital-video e VCR per tutti i comandi tranne [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) e [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)).</span><span class="sxs-lookup"><span data-stu-id="546be-109">This flag is supported by digital-video and VCR devices for all commands except [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)).</span></span>

 

 




