---
title: TfClientId (msctf. h)
description: Il tipo di dati TfClientId viene utilizzato per identificare il client.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740874"
---
# <a name="tfclientid"></a><span data-ttu-id="90663-104">TfClientId</span><span class="sxs-lookup"><span data-stu-id="90663-104">TfClientId</span></span>

<span data-ttu-id="90663-105">Il tipo di dati **TfClientId** viene utilizzato per identificare il client.</span><span class="sxs-lookup"><span data-stu-id="90663-105">The **TfClientId** data type is used to identify the client.</span></span>


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a><span data-ttu-id="90663-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="90663-106">Remarks</span></span>

<span data-ttu-id="90663-107">In TSF, le applicazioni e i servizi di testo vengono in genere definiti client.</span><span class="sxs-lookup"><span data-stu-id="90663-107">Within TSF, applications and text services are generally referred to as clients.</span></span> <span data-ttu-id="90663-108">Ogni client riceve un identificatore univoco usato per identificare se stesso quando chiama diversi metodi di gestione TSF.</span><span class="sxs-lookup"><span data-stu-id="90663-108">Each client receives a unique identifier that it uses to identify itself when calling various TSF manager methods.</span></span> <span data-ttu-id="90663-109">Questo identificatore è del tipo **TfClientId** .</span><span class="sxs-lookup"><span data-stu-id="90663-109">This identifier is of the **TfClientId** type.</span></span>

<span data-ttu-id="90663-110">Il tipo di dati **TfClientId** viene fornito dal gestore TSF.</span><span class="sxs-lookup"><span data-stu-id="90663-110">The **TfClientId** data type is supplied by the TSF manager.</span></span> <span data-ttu-id="90663-111">Un'applicazione ottiene un valore **TfClientId** quando chiama [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span><span class="sxs-lookup"><span data-stu-id="90663-111">An application obtains a **TfClientId** value when it calls [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span> <span data-ttu-id="90663-112">Il valore TfClientId per un servizio di testo viene passato al metodo [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) .</span><span class="sxs-lookup"><span data-stu-id="90663-112">The TfClientId value for a text service is passed to the [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span> <span data-ttu-id="90663-113">Qualsiasi oggetto che non soddisfa le categorie precedenti può ottenere un identificatore client chiamando [ITfClientId:: getClientID](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span><span class="sxs-lookup"><span data-stu-id="90663-113">Any object that does not fit the above categories can obtain a client identifier by calling [ITfClientId::GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span></span>

## <a name="requirements"></a><span data-ttu-id="90663-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90663-114">Requirements</span></span>



| <span data-ttu-id="90663-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="90663-115">Requirement</span></span> | <span data-ttu-id="90663-116">Valore</span><span class="sxs-lookup"><span data-stu-id="90663-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="90663-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90663-117">Minimum supported client</span></span><br/> | <span data-ttu-id="90663-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="90663-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="90663-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90663-119">Minimum supported server</span></span><br/> | <span data-ttu-id="90663-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="90663-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="90663-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="90663-121">Redistributable</span></span><br/>          | <span data-ttu-id="90663-122">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="90663-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="90663-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90663-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="90663-124"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="90663-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="90663-125">IDL</span><span class="sxs-lookup"><span data-stu-id="90663-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90663-126"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90663-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90663-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90663-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90663-128">**ITfClientId:: getClientID**</span><span class="sxs-lookup"><span data-stu-id="90663-128">**ITfClientId::GetClientId**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[<span data-ttu-id="90663-129">**ITfTextInputProcessor:: Activate**</span><span class="sxs-lookup"><span data-stu-id="90663-129">**ITfTextInputProcessor::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="90663-130">**ITfThreadMgr:: Activate**</span><span class="sxs-lookup"><span data-stu-id="90663-130">**ITfThreadMgr::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





