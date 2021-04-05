---
description: Ogni assembly side-by-side deve avere una versione.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versioni degli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757316"
---
# <a name="assembly-versions"></a><span data-ttu-id="dbc2a-103">Versioni degli assembly</span><span class="sxs-lookup"><span data-stu-id="dbc2a-103">Assembly Versions</span></span>

<span data-ttu-id="dbc2a-104">Ogni assembly side-by-side deve avere una versione.</span><span class="sxs-lookup"><span data-stu-id="dbc2a-104">Every side-by-side assembly must have a version.</span></span> <span data-ttu-id="dbc2a-105">Ogni versione dell'assembly è associata a un numero di versione con quattro parti separate da punti: *Major. minor. Build. Revision*.</span><span class="sxs-lookup"><span data-stu-id="dbc2a-105">Each assembly version is associated with a version number having four parts separated by periods: *major.minor.build.revision*.</span></span> <span data-ttu-id="dbc2a-106">Se viene apportata una modifica a un assembly rendendola incompatibile con le versioni esistenti, è necessario modificare le parti *principali* o *secondarie* del numero di versione.</span><span class="sxs-lookup"><span data-stu-id="dbc2a-106">If a change is made to an assembly making it incompatible with existing versions, the *major* or *minor* parts of the version number must be changed.</span></span> <span data-ttu-id="dbc2a-107">Un numero di versione che viene modificato solo nelle parti di *compilazione* o *Revisione* indica che l'assembly è compatibile con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="dbc2a-107">A version number that changes only in the *build* or *revision* parts indicates that the assembly is backward compatible with prior versions.</span></span>

<span data-ttu-id="dbc2a-108">La versione deve essere specificata negli elementi **assemblyIdentity** dei [manifesti](manifests.md).</span><span class="sxs-lookup"><span data-stu-id="dbc2a-108">The version must be specified in **assemblyIdentity** elements of [manifests](manifests.md).</span></span> <span data-ttu-id="dbc2a-109">Usare il formato di versione in quattro parti: mmmm. NNNNN. ooooo. ppppp.</span><span class="sxs-lookup"><span data-stu-id="dbc2a-109">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="dbc2a-110">Ognuna delle parti separate da punti può essere 0-65535 inclusi.</span><span class="sxs-lookup"><span data-stu-id="dbc2a-110">Each of the parts separated by periods can be 0-65535 inclusive.</span></span>

 

 



