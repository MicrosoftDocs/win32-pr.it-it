---
title: Proprietà Name di ITsSbEnvironment
description: Recupera un valore che indica il nome dell'ambiente che ospita il computer di destinazione.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà nome
- Nome Servizi Desktop remoto proprietà, interfaccia ITsSbEnvironment
- Interfaccia ITsSbEnvironment Servizi Desktop remoto, proprietà Name
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963962"
---
# <a name="itssbenvironmentname-property"></a><span data-ttu-id="04145-106">Proprietà ITsSbEnvironment:: Name</span><span class="sxs-lookup"><span data-stu-id="04145-106">ITsSbEnvironment::Name property</span></span>

<span data-ttu-id="04145-107">Recupera un valore che indica il nome dell'ambiente che ospita il computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="04145-107">Retrieves a value that indicates the name of the environment that hosts the target computer.</span></span>

<span data-ttu-id="04145-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="04145-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="04145-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04145-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="04145-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="04145-110">Property value</span></span>

<span data-ttu-id="04145-111">Puntatore a una variabile **BSTR** che contiene il nome dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="04145-111">A pointer to a **BSTR** variable that contains the name of the environment.</span></span>

## <a name="remarks"></a><span data-ttu-id="04145-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="04145-112">Remarks</span></span>

<span data-ttu-id="04145-113">Questo metodo restituisce una stringa non utilizzata direttamente da Connessione Desktop remoto broker (gestore connessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="04145-113">This method returns a string that is not directly used by Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="04145-114">Gestore connessione Desktop remoto passa questa stringa ai plug-in delle risorse.</span><span class="sxs-lookup"><span data-stu-id="04145-114">RD Connection Broker passes this string to resource plug-ins.</span></span>

## <a name="requirements"></a><span data-ttu-id="04145-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04145-115">Requirements</span></span>



| <span data-ttu-id="04145-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="04145-116">Requirement</span></span> | <span data-ttu-id="04145-117">Valore</span><span class="sxs-lookup"><span data-stu-id="04145-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04145-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04145-118">Minimum supported client</span></span><br/> | <span data-ttu-id="04145-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="04145-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="04145-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04145-120">Minimum supported server</span></span><br/> | <span data-ttu-id="04145-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04145-121">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="04145-122">IDL</span><span class="sxs-lookup"><span data-stu-id="04145-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04145-123"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04145-123"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04145-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04145-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04145-125">**ITsSbEnvironment**</span><span class="sxs-lookup"><span data-stu-id="04145-125">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





