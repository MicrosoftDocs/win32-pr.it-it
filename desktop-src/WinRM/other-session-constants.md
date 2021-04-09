---
title: Altre costanti di sessione (WSManDisp. h)
description: Specificare la codifica, la crittografia e la porta nome entità servizio.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236e69d80db2ad30b8cc2934b6b2016d7eecbed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121071"
---
# <a name="other-session-constants"></a><span data-ttu-id="05b04-103">Altre costanti di sessione</span><span class="sxs-lookup"><span data-stu-id="05b04-103">Other Session Constants</span></span>

<span data-ttu-id="05b04-104">Costanti, elencate nell'elenco seguente, nell'enumerazione **\_ \_ WSManSessionFlags** che specificano la porta di codifica, crittografia e nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="05b04-104">Constants, listed in the following list, in the **\_\_WSManSessionFlags** enumeration that specify encoding, encryption, and service principal name port.</span></span>

<dl> <dt>

<span data-ttu-id="05b04-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span><span class="sxs-lookup"><span data-stu-id="05b04-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05b04-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="05b04-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="05b04-107">Invia la richiesta in UTF8 anziché UTF16.</span><span class="sxs-lookup"><span data-stu-id="05b04-107">Sends the request in UTF8 rather than UTF16.</span></span>

<span data-ttu-id="05b04-108">Il metodo di scripting associato è [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) e il metodo C++ è [**IWSManEx. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span><span class="sxs-lookup"><span data-stu-id="05b04-108">The associated scripting method is [**WSMan.SessionFlagUTF8**](wsman-sessionflagutf8.md) and the C++ method is [**IWSManEx.SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05b04-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="05b04-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05b04-110">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="05b04-110">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="05b04-111">Non crittografare i messaggi inviati in rete.</span><span class="sxs-lookup"><span data-stu-id="05b04-111">Do not encrypt the messages sent over the network.</span></span> <span data-ttu-id="05b04-112">Questa impostazione è consentita solo se il [*listener*](windows-remote-management-glossary.md) è configurato in modo che **AllowUnencrypted** sia impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="05b04-112">This setting is allowed only if the [*listener*](windows-remote-management-glossary.md) is configured so that **AllowUnencrypted** is set to **True**.</span></span>

<span data-ttu-id="05b04-113">Il metodo di scripting associato è [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) e il metodo C++ è [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span><span class="sxs-lookup"><span data-stu-id="05b04-113">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05b04-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span><span class="sxs-lookup"><span data-stu-id="05b04-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05b04-115">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="05b04-115">4194304 (0x400000)</span></span>
</dt> <dt>



<span data-ttu-id="05b04-116">Specificare la porta del nome dell'entità servizio (SPN) per la connessione diretta a hardware BMC remoto, nota anche come connessione [*fuori banda*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="05b04-116">Specify the Service Principal Name (SPN) port when connecting directly to remote BMC hardware, also known as an [*out-of-band*](windows-remote-management-glossary.md) connection.</span></span> <span data-ttu-id="05b04-117">Poiché sia il computer server WinRM che l'hardware BMC possono condividere lo stesso indirizzo IP, questo flag indica che il numero di porta SPN deve essere utilizzato per determinare se la connessione è al servizio o direttamente al BMC.</span><span class="sxs-lookup"><span data-stu-id="05b04-117">Because both the WinRM server computer and the BMC hardware can share the same IP address, this flag indicates that the SPN port number must be used to determine whether the connection is to the service or directly to the BMC.</span></span> <span data-ttu-id="05b04-118">Per ulteriori informazioni, vedere [formati dei nomi per nomi SPN univoci](/windows/desktop/AD/name-formats-for-unique-spns).</span><span class="sxs-lookup"><span data-stu-id="05b04-118">For more information, see [Name Formats for Unique SPNs](/windows/desktop/AD/name-formats-for-unique-spns).</span></span>

<span data-ttu-id="05b04-119">Il metodo di scripting associato è [**WSMan. SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) e il metodo C++ è [**IWSManEx. SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span><span class="sxs-lookup"><span data-stu-id="05b04-119">The associated scripting method is [**WSMan.SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) and the C++ method is [**IWSManEx.SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05b04-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span><span class="sxs-lookup"><span data-stu-id="05b04-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05b04-121">0x800000</span><span class="sxs-lookup"><span data-stu-id="05b04-121">0x800000</span></span>
</dt> <dt>



<span data-ttu-id="05b04-122">Invia la richiesta in UTF16.</span><span class="sxs-lookup"><span data-stu-id="05b04-122">Sends the request in UTF16.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05b04-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05b04-123">Requirements</span></span>



| <span data-ttu-id="05b04-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="05b04-124">Requirement</span></span> | <span data-ttu-id="05b04-125">Valore</span><span class="sxs-lookup"><span data-stu-id="05b04-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="05b04-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05b04-126">Minimum supported client</span></span><br/> | <span data-ttu-id="05b04-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05b04-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="05b04-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05b04-128">Minimum supported server</span></span><br/> | <span data-ttu-id="05b04-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05b04-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="05b04-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05b04-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="05b04-131"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="05b04-131"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="05b04-132">IDL</span><span class="sxs-lookup"><span data-stu-id="05b04-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05b04-133"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="05b04-133"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05b04-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05b04-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b04-135">Costanti di sessione</span><span class="sxs-lookup"><span data-stu-id="05b04-135">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

