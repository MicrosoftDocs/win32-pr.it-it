---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (applicazioni isolate e assembly side-by-side)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401578"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="dfed5-103">P (applicazioni isolate e assembly side-by-side)</span><span class="sxs-lookup"><span data-stu-id="dfed5-103">P (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="dfed5-104">[A](a-sbscs-gly.md) B C [d](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="dfed5-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="dfed5-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**configurazione per applicazione**</span><span class="sxs-lookup"><span data-stu-id="dfed5-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**per-application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="dfed5-106">Configurazione che può eseguire l'override della configurazione dell'applicazione globale di un assembly specifico.</span><span class="sxs-lookup"><span data-stu-id="dfed5-106">Configuration that can override a specific assembly's global application configuration.</span></span> <span data-ttu-id="dfed5-107">Una configurazione per applicazione è specificata da un file manifesto di configurazione dell'applicazione installato nella stessa cartella del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="dfed5-107">A per-application configuration is specified by an application configuration manifest file installed in the same folder as the executable file.</span></span> <span data-ttu-id="dfed5-108">Il file manifesto descrive la versione o l'intervallo di versioni degli assembly affiancati che devono essere usati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dfed5-108">The manifest file describes the version, or range of versions, of side-by-side assemblies to be used by the application.</span></span> <span data-ttu-id="dfed5-109">La configurazione per applicazione può essere usata quando una nuova versione di un assembly non è compatibile con un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dfed5-109">Per-application configuration might be used when a new version of an assembly is incompatible with an application.</span></span> <span data-ttu-id="dfed5-110">In questo caso, è possibile eseguire l'override della configurazione predefinita o globale dell'applicazione per un assembly affiancato specifico.</span><span class="sxs-lookup"><span data-stu-id="dfed5-110">In this case, the application's default or global configuration can be overridden for a specific side-by-side assembly.</span></span>

</dd> <dt>

<span data-ttu-id="dfed5-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly side-by-side privato**</span><span class="sxs-lookup"><span data-stu-id="dfed5-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**private side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="dfed5-112">Un assembly side-by-side privato è visibile solo per un'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="dfed5-112">A private side-by-side assembly is only visible to a specified application.</span></span> <span data-ttu-id="dfed5-113">Viene installato localmente in un'applicazione isolata e il codice dell'assembly diventa privato per il contesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dfed5-113">It is installed locally to an isolated application and the assembly's code becomes private to the application context.</span></span> <span data-ttu-id="dfed5-114">Le dipendenze di un assembly side-by-side privato sono descritte nel file manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dfed5-114">The dependencies of a private side-by-side assembly are described in the application manifest file.</span></span> <span data-ttu-id="dfed5-115">Gli assembly side-by-side privati possono essere usati per compensare gli effetti negativi della condivisione degli assembly, ad esempio i conflitti tra DLL e per semplificare la distribuzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dfed5-115">Private side-by-side assemblies can be used to offset the negative effects of assembly sharing, such as DLL conflicts, and to facilitate application deployment.</span></span>

</dd> <dt>

<span data-ttu-id="dfed5-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**token di chiave pubblica**</span><span class="sxs-lookup"><span data-stu-id="dfed5-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**public key token**</span></span>
</dt> <dd>

<span data-ttu-id="dfed5-117">Stringa esadecimale a 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica in cui è firmato l'assembly.</span><span class="sxs-lookup"><span data-stu-id="dfed5-117">A 16-character hexadecimal string that represents the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="dfed5-118">La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore.</span><span class="sxs-lookup"><span data-stu-id="dfed5-118">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="dfed5-119">Obbligatorio per tutti gli assembly affiancati condivisi.</span><span class="sxs-lookup"><span data-stu-id="dfed5-119">Required for all shared side-by-side assemblies.</span></span>

</dd> </dl>

 

 



