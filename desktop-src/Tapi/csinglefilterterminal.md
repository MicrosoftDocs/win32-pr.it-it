---
description: CSingleFilterTerminal è una classe di base terminale aggiuntiva applicabile sia ai terminali statici che a quelli dinamici.
ms.assetid: d423438f-1324-4df3-beaa-fdef325fac2e
title: CSingleFilterTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111a20e59ab0c549e994695610364c451c07fd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314622"
---
# <a name="csinglefilterterminal"></a><span data-ttu-id="cd2b9-103">CSingleFilterTerminal</span><span class="sxs-lookup"><span data-stu-id="cd2b9-103">CSingleFilterTerminal</span></span>

<span data-ttu-id="cd2b9-104">**CSingleFilterTerminal** è una classe di base terminale aggiuntiva applicabile sia ai terminali statici che a quelli dinamici.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-104">**CSingleFilterTerminal** is an additional terminal base class applicable to both static and dynamic terminals.</span></span> <span data-ttu-id="cd2b9-105">Deriva da [**CBaseTerminal**](cbaseterminal.md) e rende l'implementazione più specifica, supponendo che il terminale disponga di un singolo filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-105">It is derived from [**CBaseTerminal**](cbaseterminal.md) and makes the implementation more specific by assuming that the terminal has a single DirectShow filter.</span></span> <span data-ttu-id="cd2b9-106">Quando questa condizione viene soddisfatta, la derivazione di un'implementazione del terminale da **CSingleFilterTerminal** è molto più semplice rispetto alla derivazione da **CBaseTerminal**.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-106">When this condition is met, deriving a terminal implementation from **CSingleFilterTerminal** is much easier than deriving from **CBaseTerminal**.</span></span>

<span data-ttu-id="cd2b9-107">Definito in MSPterm. h.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-107">Defined in MSPterm.h.</span></span>

 

 



