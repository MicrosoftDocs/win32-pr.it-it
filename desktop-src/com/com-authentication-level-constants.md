---
title: Costanti del livello di autenticazione (rpcdce. h)
description: Questi valori specificano un livello di autenticazione che indica la quantità di autenticazione fornita per aiutare a proteggere l'integrità dei dati. Ogni livello include la protezione fornita dai livelli precedenti.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519062"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="636a4-104">Costanti del livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="636a4-104">Authentication Level Constants</span></span>

<span data-ttu-id="636a4-105">Questi valori specificano un livello di autenticazione che indica la quantità di autenticazione fornita per aiutare a proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="636a4-105">These values specify an authentication level, which indicates the amount of authentication provided to help protect the integrity of the data.</span></span> <span data-ttu-id="636a4-106">Ogni livello include la protezione fornita dai livelli precedenti.</span><span class="sxs-lookup"><span data-stu-id="636a4-106">Each level includes the protection provided by the previous levels.</span></span>



| <span data-ttu-id="636a4-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="636a4-107">Constant/value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="636a4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="636a4-108">Description</span></span>                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="636a4-109"><dt>**RPC \_ \_ \_ Livello \_ predefinito di autenticazione C**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="636a4-109"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="636a4-110">Indica a DCOM di scegliere il livello di autenticazione utilizzando il normale algoritmo di negoziazione della copertura di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="636a4-110">Tells DCOM to choose the authentication level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="636a4-111">Per ulteriori informazioni, vedere la pagina relativa alla [negoziazione della copertura di sicurezza](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="636a4-111">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span> <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="636a4-112"><dt>**RPC \_ \_Livello autenticazione C \_ \_ None**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="636a4-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="636a4-113">Non esegue alcuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="636a4-113">Performs no authentication.</span></span><br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="636a4-114"><dt>**RPC \_ \_Livello di autenticazione \_ C \_ Connect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="636a4-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="636a4-115">Autentica le credenziali del client solo quando il client stabilisce una relazione con il server.</span><span class="sxs-lookup"><span data-stu-id="636a4-115">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span> <span data-ttu-id="636a4-116">I trasporti di datagramma utilizzano sempre \_ PKT a livello di autenticazione RPC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="636a4-116">Datagram transports always use RPC\_AUTHN\_LEVEL\_PKT instead.</span></span> <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="636a4-117"><dt>**RPC \_ \_ \_ \_ Chiamata a livello di autenticazione C**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="636a4-117"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt> <dt>3</dt></span></span> </dl>                             | <span data-ttu-id="636a4-118">Esegue l'autenticazione solo all'inizio di ogni chiamata di procedura remota quando il server riceve la richiesta.</span><span class="sxs-lookup"><span data-stu-id="636a4-118">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="636a4-119">I trasporti di datagramma usano \_ \_ invece PKT a livello auth C RPC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="636a4-119">Datagram transports use RPC\_C\_AUTHN\_LEVEL\_PKT instead.</span></span><br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="636a4-120"><dt>**RPC \_ \_Livello di autenticazione \_ C \_ PKT**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="636a4-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt> <dt>4</dt></span></span> </dl>                                | <span data-ttu-id="636a4-121">Autentica che tutti i dati ricevuti provengano dal client previsto.</span><span class="sxs-lookup"><span data-stu-id="636a4-121">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="636a4-122"><dt>**RPC \_ \_Livello di autenticazione \_ C \_ PKT \_ integrità**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="636a4-122"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="636a4-123">Autentica e verifica che nessuno dei dati trasferiti tra il client e il server sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="636a4-123">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="636a4-124"><dt>**RPC \_ \_Livello di autenticazione \_ C \_ PKT \_ privacy**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="636a4-124"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="636a4-125">Autentica tutti i livelli precedenti e crittografa il valore dell'argomento di ogni chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="636a4-125">Authenticates all previous levels and encrypts the argument value of each remote procedure call.</span></span><br/>                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="636a4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="636a4-126">Requirements</span></span>



| <span data-ttu-id="636a4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="636a4-127">Requirement</span></span> | <span data-ttu-id="636a4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="636a4-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="636a4-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="636a4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="636a4-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="636a4-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="636a4-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="636a4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="636a4-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="636a4-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="636a4-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="636a4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="636a4-134"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="636a4-134"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





