---
title: Proprietà InitialProgram di ITsSbSession
description: Recupera o specifica il programma iniziale per questa sessione.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà InitialProgram
- Servizi Desktop remoto proprietà InitialProgram, interfaccia ITsSbSession
- Interfaccia ITsSbSession Servizi Desktop remoto, proprietà InitialProgram
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476727"
---
# <a name="itssbsessioninitialprogram-property"></a><span data-ttu-id="ce98b-106">Proprietà ITsSbSession:: InitialProgram</span><span class="sxs-lookup"><span data-stu-id="ce98b-106">ITsSbSession::InitialProgram property</span></span>

<span data-ttu-id="ce98b-107">Recupera o specifica il programma iniziale per questa sessione.</span><span class="sxs-lookup"><span data-stu-id="ce98b-107">Retrieves or specifies the initial program for this session.</span></span> <span data-ttu-id="ce98b-108">Il programma iniziale è il programma che viene avviato all'avvio della sessione utente.</span><span class="sxs-lookup"><span data-stu-id="ce98b-108">The initial program is the program that is launched when the user session starts.</span></span>

<span data-ttu-id="ce98b-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ce98b-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce98b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce98b-110">Syntax</span></span>


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a><span data-ttu-id="ce98b-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ce98b-111">Property value</span></span>

<span data-ttu-id="ce98b-112">Variabile **BSTR** che contiene il programma iniziale.</span><span class="sxs-lookup"><span data-stu-id="ce98b-112">A **BSTR** variable that contains the initial program.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce98b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce98b-113">Requirements</span></span>



| <span data-ttu-id="ce98b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce98b-114">Requirement</span></span> | <span data-ttu-id="ce98b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ce98b-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ce98b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce98b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce98b-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ce98b-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ce98b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce98b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce98b-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ce98b-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="ce98b-120">IDL</span><span class="sxs-lookup"><span data-stu-id="ce98b-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ce98b-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ce98b-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce98b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce98b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce98b-123">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="ce98b-123">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





