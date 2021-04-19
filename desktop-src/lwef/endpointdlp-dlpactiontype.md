---
description: Specifica il tipo di azione di un'operazione dlp (Data Loss Prevention) dell'endpoint.
title: Enumerazione DlpActionType (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495775"
---
# <a name="dlpactiontype-enumeration"></a><span data-ttu-id="09e62-103">Enumerazione DlpActionType</span><span class="sxs-lookup"><span data-stu-id="09e62-103">DlpActionType enumeration</span></span>

<span data-ttu-id="09e62-104">Specifica il tipo di azione di un'operazione dlp (Data Loss Prevention) dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="09e62-104">Specifies the action type of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e62-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09e62-105">Syntax</span></span>


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a><span data-ttu-id="09e62-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="09e62-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="09e62-107">*DlpActionTypeCopyToRemovableMedia*</span><span class="sxs-lookup"><span data-stu-id="09e62-107">*DlpActionTypeCopyToRemovableMedia*</span></span>
</dt> <dd>

<span data-ttu-id="09e62-108">Operazione di copia su supporti rimovibili.</span><span class="sxs-lookup"><span data-stu-id="09e62-108">A copy operation to removable media.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="09e62-109">*DlpActionTypeCopyToNetworkShare*</span><span class="sxs-lookup"><span data-stu-id="09e62-109">*DlpActionTypeCopyToNetworkShare*</span></span>
</dt> <dd>

<span data-ttu-id="09e62-110">Operazione di copia in una cartella di rete condivisa.</span><span class="sxs-lookup"><span data-stu-id="09e62-110">A copy operation to a shared network folder.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="09e62-111">*DlpActionTypeCopyToClipboard*</span><span class="sxs-lookup"><span data-stu-id="09e62-111">*DlpActionTypeCopyToClipboard*</span></span>
</dt> <dd>

<span data-ttu-id="09e62-112">Operazione di copia negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="09e62-112">A copy operation to the clipboard.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="09e62-113">*DlpActionTypePrint*</span><span class="sxs-lookup"><span data-stu-id="09e62-113">*DlpActionTypePrint*</span></span>
</dt> <dd>

<span data-ttu-id="09e62-114">Operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="09e62-114">A print operation.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="09e62-115">*DlpActionTypeScreenClip*</span><span class="sxs-lookup"><span data-stu-id="09e62-115">*DlpActionTypeScreenClip*</span></span>
</dt> <dd>

<span data-ttu-id="09e62-116">Operazione di acquisizione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="09e62-116">A screen capture operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="09e62-117">*DlpActionTypeAccessByUnallowedApp*</span><span class="sxs-lookup"><span data-stu-id="09e62-117">*DlpActionTypeAccessByUnallowedApp*</span></span>
</dt> <dd>

<span data-ttu-id="09e62-118">Operazione eseguita da un'app non consentita.</span><span class="sxs-lookup"><span data-stu-id="09e62-118">An operation performed by an unallowed app.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="09e62-119">*DlpActionTypeCloudAppEgress*</span><span class="sxs-lookup"><span data-stu-id="09e62-119">*DlpActionTypeCloudAppEgress*</span></span>
</dt> <dd>

<span data-ttu-id="09e62-120">Operazione destinata a una posizione cloud.</span><span class="sxs-lookup"><span data-stu-id="09e62-120">An operation targeted to a cloud location.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="09e62-121">*DlpActionTypeAccessByBluetoothApp*</span><span class="sxs-lookup"><span data-stu-id="09e62-121">*DlpActionTypeAccessByBluetoothApp*</span></span>
</dt> <dd>

<span data-ttu-id="09e62-122">Operazione che include l'accesso da parte di un'app Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="09e62-122">An operation that includes access by a bluetooth app.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="09e62-123">*DlpActionTypeAccessByRDPApp*</span><span class="sxs-lookup"><span data-stu-id="09e62-123">*DlpActionTypeAccessByRDPApp*</span></span>
</dt> <dd>

<span data-ttu-id="09e62-124">Operazione che include l'accesso da parte di un desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="09e62-124">An operation that includes access by a remote desktop.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="09e62-125">*DlpActionTypeCount*</span><span class="sxs-lookup"><span data-stu-id="09e62-125">*DlpActionTypeCount*</span></span>
</dt> <dd>

<span data-ttu-id="09e62-126">Valore massimo dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="09e62-126">The maximum value of the enumeration.</span></span>

</dd> </dl>
 

## <a name="remarks"></a><span data-ttu-id="09e62-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="09e62-127">Remarks</span></span>

<span data-ttu-id="09e62-128">I valori di questa enumerazione vengono usati dalla [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) struttura .</span><span class="sxs-lookup"><span data-stu-id="09e62-128">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="09e62-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09e62-129">Requirements</span></span>



| <span data-ttu-id="09e62-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e62-130">Requirement</span></span>          |    <span data-ttu-id="09e62-131">Valore</span><span class="sxs-lookup"><span data-stu-id="09e62-131">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09e62-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09e62-132">Minimum supported client</span></span><br/> | <span data-ttu-id="09e62-133">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="09e62-133">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

