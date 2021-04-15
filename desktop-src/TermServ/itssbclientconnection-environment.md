---
title: Proprietà dell'ambiente ITsSbClientConnection
description: Recupera un oggetto che contiene informazioni sull'ambiente che ospita il computer di destinazione.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà ambiente
- Servizi Desktop remoto Proprietà ambiente, interfaccia ITsSbClientConnection
- Interfaccia ITsSbClientConnection Servizi Desktop remoto, proprietà Environment
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477723"
---
# <a name="itssbclientconnectionenvironment-property"></a><span data-ttu-id="4ccc5-106">Proprietà ITsSbClientConnection:: Environment</span><span class="sxs-lookup"><span data-stu-id="4ccc5-106">ITsSbClientConnection::Environment property</span></span>

<span data-ttu-id="4ccc5-107">Recupera un oggetto che contiene informazioni sull'ambiente che ospita il computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4ccc5-107">Retrieves an object that contains information about the environment that hosts the target computer.</span></span> <span data-ttu-id="4ccc5-108">Ad esempio, in uno scenario di desktop virtuale, questo oggetto contiene informazioni sul computer che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4ccc5-108">For example, in a virtual desktop scenario, this object would contain information about the computer that hosts the virtual machine.</span></span>

<span data-ttu-id="4ccc5-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4ccc5-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccc5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ccc5-110">Syntax</span></span>


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a><span data-ttu-id="4ccc5-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4ccc5-111">Property value</span></span>

<span data-ttu-id="4ccc5-112">Puntatore a un puntatore a un oggetto di ambiente [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) .</span><span class="sxs-lookup"><span data-stu-id="4ccc5-112">A pointer to a pointer to an [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) environment object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4ccc5-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4ccc5-113">Error codes</span></span>

<span data-ttu-id="4ccc5-114">Se il metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4ccc5-114">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4ccc5-115">In caso contrario, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="4ccc5-115">Otherwise, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="4ccc5-116">I valori possibili includono, ma non sono limitati a, quelli nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="4ccc5-116">Possible values include, but are not limited to, those in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4ccc5-117">\_puntatore E</span><span class="sxs-lookup"><span data-stu-id="4ccc5-117">E\_POINTER</span></span>
</dt> <dd>

<span data-ttu-id="4ccc5-118">L'ambiente non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="4ccc5-118">The environment was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ccc5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ccc5-119">Remarks</span></span>

<span data-ttu-id="4ccc5-120">Un plug-in di orchestrazione può chiamare questo metodo per recuperare le informazioni sull'ambiente di una macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4ccc5-120">An orchestration plug-in can call this method to retrieve environment information about a target virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ccc5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ccc5-121">Requirements</span></span>



| <span data-ttu-id="4ccc5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ccc5-122">Requirement</span></span> | <span data-ttu-id="4ccc5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4ccc5-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4ccc5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ccc5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4ccc5-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4ccc5-125">None supported</span></span><br/>                                                            |
| <span data-ttu-id="4ccc5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ccc5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4ccc5-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ccc5-127">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="4ccc5-128">IDL</span><span class="sxs-lookup"><span data-stu-id="4ccc5-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ccc5-129"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ccc5-129"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ccc5-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ccc5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ccc5-131">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="4ccc5-131">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





