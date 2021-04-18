---
title: Proprietà nome utente ITsSbSession
description: Recupera il nome utente per la sessione.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Proprietà UserName Servizi Desktop remoto
- Servizi Desktop remoto proprietà UserName, interfaccia ITsSbSession
- Interfaccia ITsSbSession Servizi Desktop remoto, proprietà UserName
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302603"
---
# <a name="itssbsessionusername-property"></a><span data-ttu-id="ff0b1-106">Proprietà ITsSbSession:: username</span><span class="sxs-lookup"><span data-stu-id="ff0b1-106">ITsSbSession::Username property</span></span>

<span data-ttu-id="ff0b1-107">Recupera il nome utente per la sessione.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-107">Retrieves the user name for this session.</span></span>

<span data-ttu-id="ff0b1-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff0b1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff0b1-109">Syntax</span></span>


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a><span data-ttu-id="ff0b1-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ff0b1-110">Property value</span></span>

<span data-ttu-id="ff0b1-111">Puntatore a una variabile **BSTR** che riceve il nome utente per la sessione.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-111">A pointer to a **BSTR** variable that receives the user name for this session.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff0b1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff0b1-112">Requirements</span></span>



| <span data-ttu-id="ff0b1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff0b1-113">Requirement</span></span> | <span data-ttu-id="ff0b1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ff0b1-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0b1-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff0b1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ff0b1-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ff0b1-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ff0b1-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff0b1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ff0b1-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff0b1-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="ff0b1-119">IDL</span><span class="sxs-lookup"><span data-stu-id="ff0b1-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff0b1-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff0b1-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff0b1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff0b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0b1-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="ff0b1-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





