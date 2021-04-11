---
description: "Il metodo Revert Elimina tutte le modifiche apportate a un flusso sottoposto a transazione dall'ultima chiamata a IByteBuffer:: commit."
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'Metodo IByteBuffer:: Revert (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226024"
---
# <a name="ibytebufferrevert-method"></a><span data-ttu-id="1a13c-103">Metodo IByteBuffer:: Revert</span><span class="sxs-lookup"><span data-stu-id="1a13c-103">IByteBuffer::Revert method</span></span>

<span data-ttu-id="1a13c-104">\[Il metodo **Revert** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="1a13c-104">\[The **Revert** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1a13c-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1a13c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1a13c-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="1a13c-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="1a13c-107">Il metodo **Revert** Elimina tutte le modifiche apportate a un flusso sottoposto a transazione dall'ultima chiamata a [**IByteBuffer:: commit**](ibytebuffer-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="1a13c-107">The **Revert** method discards all changes that have been made to a transacted stream since the last [**IByteBuffer::Commit**](ibytebuffer-commit.md) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a13c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a13c-108">Syntax</span></span>


```C++
HRESULT Revert();
```



## <a name="parameters"></a><span data-ttu-id="1a13c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a13c-109">Parameters</span></span>

<span data-ttu-id="1a13c-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1a13c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a13c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a13c-111">Return value</span></span>

<span data-ttu-id="1a13c-112">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1a13c-112">The return value is an **HRESULT**.</span></span> <span data-ttu-id="1a13c-113">Un valore di S \_ OK indica che la chiamata è stata completata e che il flusso è stato ripristinato alla versione precedente.</span><span class="sxs-lookup"><span data-stu-id="1a13c-113">A value of S\_OK indicates the call was successful and the stream was reverted to its previous version.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a13c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a13c-114">Remarks</span></span>

<span data-ttu-id="1a13c-115">Questo metodo ignora le modifiche apportate a un flusso sottoposto a transazione dall'ultima operazione di commit.</span><span class="sxs-lookup"><span data-stu-id="1a13c-115">This method discards changes made to a transacted stream since the last commit operation.</span></span>

## <a name="examples"></a><span data-ttu-id="1a13c-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="1a13c-116">Examples</span></span>

<span data-ttu-id="1a13c-117">Nell'esempio seguente viene illustrato il ripristino di un flusso transazionale all'ultima operazione di cui è stato eseguito il commit.</span><span class="sxs-lookup"><span data-stu-id="1a13c-117">The following example shows reverting a transacted stream to the last-committed operation.</span></span>


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a><span data-ttu-id="1a13c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a13c-118">Requirements</span></span>



| <span data-ttu-id="1a13c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a13c-119">Requirement</span></span> | <span data-ttu-id="1a13c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1a13c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a13c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a13c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1a13c-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1a13c-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1a13c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a13c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1a13c-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a13c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a13c-125">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1a13c-125">End of client support</span></span><br/>    | <span data-ttu-id="1a13c-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1a13c-126">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1a13c-127">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="1a13c-127">End of server support</span></span><br/>    | <span data-ttu-id="1a13c-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1a13c-128">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1a13c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a13c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a13c-130"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a13c-130"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a13c-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1a13c-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="1a13c-132"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1a13c-132"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1a13c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1a13c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a13c-134"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a13c-134"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1a13c-135">IID</span><span class="sxs-lookup"><span data-stu-id="1a13c-135">IID</span></span><br/>                      | <span data-ttu-id="1a13c-136">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="1a13c-136">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

