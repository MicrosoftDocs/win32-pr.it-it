---
title: Struttura EapHostPeerNapInfo (Eaphostpeerapis. h)
description: Contiene le informazioni di protezione accesso alla rete (NAP) su un supplicant EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- Struttura EapHostPeerNapInfo EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048680"
---
# <a name="eaphostpeernapinfo-structure"></a><span data-ttu-id="e48d0-104">Struttura EapHostPeerNapInfo</span><span class="sxs-lookup"><span data-stu-id="e48d0-104">EapHostPeerNapInfo structure</span></span>

<span data-ttu-id="e48d0-105">La struttura **EapHostPeerNapInfo** contiene le informazioni di protezione accesso alla rete (NAP) su un supplicant EAP.</span><span class="sxs-lookup"><span data-stu-id="e48d0-105">The **EapHostPeerNapInfo** structure contains the Network Access Protection (NAP) information on an EAP supplicant.</span></span>

## <a name="syntax"></a><span data-ttu-id="e48d0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e48d0-106">Syntax</span></span>


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a><span data-ttu-id="e48d0-107">Members</span><span class="sxs-lookup"><span data-stu-id="e48d0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e48d0-108">**isolationState**</span><span class="sxs-lookup"><span data-stu-id="e48d0-108">**isolationState**</span></span>
</dt> <dd>

<span data-ttu-id="e48d0-109">Struttura [**di \_ stato di isolamento**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) che specifica lo stato di isolamento NAP di un computer.</span><span class="sxs-lookup"><span data-stu-id="e48d0-109">An [**ISOLATION\_STATE**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) structure that specifies the NAP isolation state of a computer.</span></span> <span data-ttu-id="e48d0-110">Lo stato di isolamento determina il livello di accesso alla rete concesso.</span><span class="sxs-lookup"><span data-stu-id="e48d0-110">The isolation state determines the level of network access granted.</span></span>

</dd> <dt>

<span data-ttu-id="e48d0-111">**probationTime**</span><span class="sxs-lookup"><span data-stu-id="e48d0-111">**probationTime**</span></span>
</dt> <dd>

<span data-ttu-id="e48d0-112">Struttura **ProbationTime** che specifica il tempo necessario affinché la connessione esca dalla quarantena dopo la quale viene eliminata la connessione.</span><span class="sxs-lookup"><span data-stu-id="e48d0-112">A **ProbationTime** structure that specifies the time required for the connection to come out of quarantine after which the connection will be dropped.</span></span> <span data-ttu-id="e48d0-113">Una struttura **ProbationTime** è identica a una struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="e48d0-113">A **ProbationTime** structure is identical to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e48d0-114">**stringCorrelationIdLength**</span><span class="sxs-lookup"><span data-stu-id="e48d0-114">**stringCorrelationIdLength**</span></span>
</dt> <dd>

<span data-ttu-id="e48d0-115">Lunghezza, in byte, del [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) di protezione accesso alla rete che segue la struttura.</span><span class="sxs-lookup"><span data-stu-id="e48d0-115">The length, in bytes, of the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) that follows this structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e48d0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e48d0-116">Remarks</span></span>

<span data-ttu-id="e48d0-117">La struttura **EapHostPeerNapInfo** precede il [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) di protezione accesso alla rete del tipo di dati **WCHAR** nel flusso di byte RPC.</span><span class="sxs-lookup"><span data-stu-id="e48d0-117">The **EapHostPeerNapInfo** structure precedes the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) of data type **WCHAR** in the RPC byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="e48d0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e48d0-118">Requirements</span></span>



| <span data-ttu-id="e48d0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e48d0-119">Requirement</span></span> | <span data-ttu-id="e48d0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e48d0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e48d0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e48d0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e48d0-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e48d0-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="e48d0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e48d0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e48d0-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e48d0-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e48d0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e48d0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e48d0-126"><dt>Eaphostpeerapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="e48d0-126"><dt>Eaphostpeerapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e48d0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e48d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48d0-128">Strutture supplicant EAPHost</span><span class="sxs-lookup"><span data-stu-id="e48d0-128">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="e48d0-129">**EapHostPeerGetAuthStatus**</span><span class="sxs-lookup"><span data-stu-id="e48d0-129">**EapHostPeerGetAuthStatus**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[<span data-ttu-id="e48d0-130">**EapHostPeerMethodAuthParams**</span><span class="sxs-lookup"><span data-stu-id="e48d0-130">**EapHostPeerMethodAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

