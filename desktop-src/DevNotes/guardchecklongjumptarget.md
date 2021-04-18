---
UID: ''
title: GuardCheckLongJumpTarget (funzione)
description: Tenta di verificare se la destinazione di un longjmp è valida.
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "106299550"
---
# <a name="guardchecklongjumptarget-function"></a><span data-ttu-id="ccfb6-103">GuardCheckLongJumpTarget (funzione)</span><span class="sxs-lookup"><span data-stu-id="ccfb6-103">GuardCheckLongJumpTarget function</span></span>

## <a name="description"></a><span data-ttu-id="ccfb6-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccfb6-104">Description</span></span>

<span data-ttu-id="ccfb6-105">Tenta di verificare se la destinazione di un [longjmp](/cpp/c-runtime-library/reference/longjmp) è valida per un processo con [protezione del flusso di controllo (cfg)](../secbp/control-flow-guard.md) abilitata.</span><span class="sxs-lookup"><span data-stu-id="ccfb6-105">Attempts to verify whether the target of a [longjmp](/cpp/c-runtime-library/reference/longjmp) is valid for a process which has [Control Flow Guard (CFG)](../secbp/control-flow-guard.md) enabled.</span></span>

<span data-ttu-id="ccfb6-106">Se l'indirizzo di destinazione corrisponde a un mapping di immagini, vengono estratte le destinazioni valide per il file binario.</span><span class="sxs-lookup"><span data-stu-id="ccfb6-106">If the target address corresponds to an image mapping, the valid targets are extracted for the binary.</span></span>
<span data-ttu-id="ccfb6-107">La funzione utilizza tali destinazioni per convalidare la destinazione.</span><span class="sxs-lookup"><span data-stu-id="ccfb6-107">The function uses those targets to validate the target.</span></span>
<span data-ttu-id="ccfb6-108">Se il file binario non contiene metadati che descrivono il set di destinazioni *longjmp* valide, la funzione restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="ccfb6-108">If the binary does not have metadata that describes the set of valid *longjmp* targets, the function returns **TRUE**.</span></span>

<span data-ttu-id="ccfb6-109">Se l'indirizzo di destinazione corrisponde a un mapping non di immagine, come nel codice JIT, viene consultato un criterio globale di sola lettura per determinare se il salto è consentito.</span><span class="sxs-lookup"><span data-stu-id="ccfb6-109">If the target address corresponds to a non-image mapping, as in JIT code, a global read-only policy is consulted to determine whether the jump is allowed.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccfb6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccfb6-110">Parameters</span></span>

### <a name="targetaddress-in"></a><span data-ttu-id="ccfb6-111">TargetAddress [in]</span><span class="sxs-lookup"><span data-stu-id="ccfb6-111">TargetAddress [in]</span></span>

<span data-ttu-id="ccfb6-112">Indirizzo di destinazione per il salto.</span><span class="sxs-lookup"><span data-stu-id="ccfb6-112">The target address for the jump.</span></span>

### <a name="flags-in"></a><span data-ttu-id="ccfb6-113">Flags [in]</span><span class="sxs-lookup"><span data-stu-id="ccfb6-113">Flags [in]</span></span>

<span data-ttu-id="ccfb6-114">Flag che descrivono l'operazione da eseguire sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ccfb6-114">Flags describing the operation to be performed on the address.</span></span>
<span data-ttu-id="ccfb6-115">Se si specifica **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), questa funzione non termina il processo se la destinazione non è valida.</span><span class="sxs-lookup"><span data-stu-id="ccfb6-115">If you specify **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), this function does not terminate the process if the target is invalid.</span></span>

## <a name="returns"></a><span data-ttu-id="ccfb6-116">Restituisce</span><span class="sxs-lookup"><span data-stu-id="ccfb6-116">Returns</span></span>

<span data-ttu-id="ccfb6-117">**True** se la destinazione è valida; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="ccfb6-117">**TRUE** if the target is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccfb6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccfb6-118">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="ccfb6-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ccfb6-119">See also</span></span>
