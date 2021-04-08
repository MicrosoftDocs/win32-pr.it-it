---
title: TfEditCookie (msctf. h)
description: Il tipo di dati TfEditCookie identifica una sessione di modifica con un blocco.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047816"
---
# <a name="tfeditcookie"></a><span data-ttu-id="f3b3e-104">TfEditCookie</span><span class="sxs-lookup"><span data-stu-id="f3b3e-104">TfEditCookie</span></span>

<span data-ttu-id="f3b3e-105">Il tipo di dati **TfEditCookie** identifica una sessione di modifica con un blocco.</span><span class="sxs-lookup"><span data-stu-id="f3b3e-105">The **TfEditCookie** data type identifies an edit session that has a lock.</span></span>


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a><span data-ttu-id="f3b3e-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3b3e-106">Remarks</span></span>

<span data-ttu-id="f3b3e-107">Il tipo di dati **TfEditCookie** viene fornito dal gestore TSF e viene usato da un client (servizio applicazione o testo) per identificare una sessione di modifica con un blocco di sola lettura o di lettura/scrittura in diversi metodi.</span><span class="sxs-lookup"><span data-stu-id="f3b3e-107">The **TfEditCookie** data type is supplied by the TSF manager and is used by a client (application or text service) to identify an edit session with a read-only or read/write lock in various methods.</span></span>

<span data-ttu-id="f3b3e-108">Viene ottenuto un valore **TfEditCookie** in uno dei modi seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3b3e-108">A **TfEditCookie** value is obtained in one of the following ways.</span></span>

-   <span data-ttu-id="f3b3e-109">Il client chiama [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span><span class="sxs-lookup"><span data-stu-id="f3b3e-109">The client calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>
-   <span data-ttu-id="f3b3e-110">Il gestore TSF chiama il metodo client [ITfEditSession::D oeditsession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) .</span><span class="sxs-lookup"><span data-stu-id="f3b3e-110">The TSF manager calls the client [ITfEditSession::DoEditSession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) method.</span></span>
-   <span data-ttu-id="f3b3e-111">Il gestore TSF chiama il metodo client [ITfCompositionSink:: OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) .</span><span class="sxs-lookup"><span data-stu-id="f3b3e-111">The TSF manager calls the client [ITfCompositionSink::OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) method.</span></span>
-   <span data-ttu-id="f3b3e-112">Il gestore TSF chiama il metodo client [ITfCleanupContextSink:: OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) .</span><span class="sxs-lookup"><span data-stu-id="f3b3e-112">The TSF manager calls the client [ITfCleanupContextSink::OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) method.</span></span>
-   <span data-ttu-id="f3b3e-113">Il gestore TSF chiama il metodo client [ITfTextEditSink:: OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) .</span><span class="sxs-lookup"><span data-stu-id="f3b3e-113">The TSF manager calls the client [ITfTextEditSink::OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b3e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3b3e-114">Requirements</span></span>



| <span data-ttu-id="f3b3e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3b3e-115">Requirement</span></span> | <span data-ttu-id="f3b3e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f3b3e-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b3e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3b3e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b3e-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="f3b3e-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="f3b3e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3b3e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b3e-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f3b3e-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="f3b3e-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f3b3e-121">Redistributable</span></span><br/>          | <span data-ttu-id="f3b3e-122">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f3b3e-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="f3b3e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3b3e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3b3e-124"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b3e-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3b3e-125">IDL</span><span class="sxs-lookup"><span data-stu-id="f3b3e-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3b3e-126"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3b3e-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b3e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3b3e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b3e-128">**ITfCleanupContextSink::OnCleanupContext**</span><span class="sxs-lookup"><span data-stu-id="f3b3e-128">**ITfCleanupContextSink::OnCleanupContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[<span data-ttu-id="f3b3e-129">**ITfCompositionSink::OnCompositionTerminated**</span><span class="sxs-lookup"><span data-stu-id="f3b3e-129">**ITfCompositionSink::OnCompositionTerminated**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[<span data-ttu-id="f3b3e-130">**ITfDocumentMgr:: CreateContext**</span><span class="sxs-lookup"><span data-stu-id="f3b3e-130">**ITfDocumentMgr::CreateContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="f3b3e-131">**ITfEditSession::D oEditSession**</span><span class="sxs-lookup"><span data-stu-id="f3b3e-131">**ITfEditSession::DoEditSession**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[<span data-ttu-id="f3b3e-132">**ITfTextEditSink::OnEndEdit**</span><span class="sxs-lookup"><span data-stu-id="f3b3e-132">**ITfTextEditSink::OnEndEdit**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





