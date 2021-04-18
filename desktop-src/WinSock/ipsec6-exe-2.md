---
description: La configurazione dei criteri IPSec e delle associazioni di sicurezza per IPv6 viene eseguita con Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306945"
---
# <a name="ipsec6exe"></a><span data-ttu-id="20f38-103">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="20f38-103">Ipsec6.exe</span></span>

<span data-ttu-id="20f38-104">La configurazione dei criteri IPSec e delle associazioni di sicurezza per IPv6 viene eseguita con Ipsec6.exe.</span><span class="sxs-lookup"><span data-stu-id="20f38-104">Configuration of IPSec policies and security associations for IPv6 is done with Ipsec6.exe.</span></span> <span data-ttu-id="20f38-105">Di seguito sono Ipsec6.exe sottocomandi:</span><span class="sxs-lookup"><span data-stu-id="20f38-105">The following are Ipsec6.exe subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="20f38-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**SP \[ ipsec6** _Interfaccia_ di *_\]_*</span><span class="sxs-lookup"><span data-stu-id="20f38-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 sp \[**_Interface_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="20f38-107">Visualizza i criteri di sicurezza attivi.</span><span class="sxs-lookup"><span data-stu-id="20f38-107">Displays active security policies.</span></span> <span data-ttu-id="20f38-108">In alternativa, Visualizza i criteri di sicurezza attivi per un'interfaccia specifica.</span><span class="sxs-lookup"><span data-stu-id="20f38-108">Alternately, displays active security policies for a specific interface.</span></span>

</dd> <dt>

<span data-ttu-id="20f38-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**sa ipsec6**</span><span class="sxs-lookup"><span data-stu-id="20f38-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 sa**</span></span>
</dt> <dd>

<span data-ttu-id="20f38-110">Visualizza le associazioni di sicurezza attive.</span><span class="sxs-lookup"><span data-stu-id="20f38-110">Displays active security associations.</span></span>

</dd> <dt>

<span data-ttu-id="20f38-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[** _FileName (senza estensione)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="20f38-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="20f38-112">Crea i file utilizzati per configurare i criteri di sicurezza e le associazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="20f38-112">Creates files used to configure security policy and security associations.</span></span> <span data-ttu-id="20f38-113">Crea *filename*. SPD per i criteri di sicurezza e *filename*. Sad per le associazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="20f38-113">Creates *FileName*.spd for security policies and *FileName*.sad for security associations.</span></span> <span data-ttu-id="20f38-114">Usare i file creati come modelli per configurare i criteri di sicurezza o le associazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="20f38-114">Use the created files as templates to configure security policies or security associations.</span></span> <span data-ttu-id="20f38-115">I file possono essere modificati con un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="20f38-115">The files can be modified with a text editor.</span></span> <span data-ttu-id="20f38-116">Per richiamare la configurazione contenuta nei file SPD e SAD, utilizzare il comando **ipsec6 a** .</span><span class="sxs-lookup"><span data-stu-id="20f38-116">To invoke the configuration contained in the SPD and SAD files, use the **ipsec6 a** command.</span></span>

</dd> <dt>

<span data-ttu-id="20f38-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 \[** _FileName (senza estensione)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="20f38-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 a \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="20f38-118">Aggiunge i criteri di sicurezza in *filename*. SPD e le associazioni di sicurezza in *filename*. Sad all'elenco dei criteri di sicurezza e delle associazioni di sicurezza attivi.</span><span class="sxs-lookup"><span data-stu-id="20f38-118">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations.</span></span>

</dd> <dt>

<span data-ttu-id="20f38-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 \[**  *_\] \[_* _Nome file criterio (senza estensione)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="20f38-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[**_Policy_*_\] \[_*_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="20f38-120">Aggiunge i criteri di sicurezza in *filename*. SPD e le associazioni di sicurezza in *filename*. Sad all'elenco dei criteri di sicurezza attivi e delle associazioni di sicurezza, come a cui fa riferimento il numero di criteri.</span><span class="sxs-lookup"><span data-stu-id="20f38-120">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations as referenced by policy number.</span></span>

</dd> <dt>

<span data-ttu-id="20f38-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[ Type = SP sa \] \[** _NumeroIndice_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="20f38-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[type = sp sa\] \[**_IndexNumber_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="20f38-122">Elimina i criteri di sicurezza o le associazioni di sicurezza dall'elenco dei criteri di sicurezza attivi e delle associazioni di sicurezza, come a cui fa riferimento il numero di indice (visualizzato con **ipsec6 sp** o **ipsec6 sa**).</span><span class="sxs-lookup"><span data-stu-id="20f38-122">Deletes security policies or security associations from the list of active security policies and security associations, as referenced by their index number (displayed with **ipsec6 sp** or **ipsec6 sa**).</span></span>

</dd> </dl>

 

 



