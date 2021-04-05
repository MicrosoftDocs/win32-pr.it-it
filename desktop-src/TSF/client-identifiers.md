---
title: Identificatori client
description: Identificatori client
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- Framework servizi di testo (TSF), identificatori client
- TSF (Framework dei servizi di testo), identificatori client
- Servizi di testo, identificatori client
- Applicazioni abilitate per TSF, identificatori client
- identificatori client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de15b208d2fbc6c6ea5c2a1114eb5cb23ff12ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955287"
---
# <a name="client-identifiers"></a><span data-ttu-id="db1e9-108">Identificatori client</span><span class="sxs-lookup"><span data-stu-id="db1e9-108">Client Identifiers</span></span>

## <a name="applications"></a><span data-ttu-id="db1e9-109">Applicazioni</span><span class="sxs-lookup"><span data-stu-id="db1e9-109">Applications</span></span>

<span data-ttu-id="db1e9-110">Un'applicazione ottiene il relativo identificatore client chiamando [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span><span class="sxs-lookup"><span data-stu-id="db1e9-110">An application obtains its client identifier by calling [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span>

## <a name="text-services"></a><span data-ttu-id="db1e9-111">Servizi di testo</span><span class="sxs-lookup"><span data-stu-id="db1e9-111">Text Services</span></span>

<span data-ttu-id="db1e9-112">Un servizio di testo ottiene l'identificatore client quando viene chiamato il metodo [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) del servizio di testo.</span><span class="sxs-lookup"><span data-stu-id="db1e9-112">A text service obtains its client identifier when the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method is called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db1e9-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db1e9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db1e9-114">ITfThreadMgr:: Activate</span><span class="sxs-lookup"><span data-stu-id="db1e9-114">ITfThreadMgr::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[<span data-ttu-id="db1e9-115">ITfTextInputProcessor:: Activate</span><span class="sxs-lookup"><span data-stu-id="db1e9-115">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




