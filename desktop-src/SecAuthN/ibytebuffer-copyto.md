---
description: Il metodo CopyTo copia un numero specificato di byte dal puntatore di ricerca corrente nell'oggetto al puntatore di ricerca corrente in un altro oggetto.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'Metodo IByteBuffer:: CopyTo (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233283"
---
# <a name="ibytebuffercopyto-method"></a><span data-ttu-id="ef225-103">Metodo IByteBuffer:: CopyTo</span><span class="sxs-lookup"><span data-stu-id="ef225-103">IByteBuffer::CopyTo method</span></span>

<span data-ttu-id="ef225-104">\[Il metodo **CopyTo** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ef225-104">\[The **CopyTo** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ef225-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ef225-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ef225-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ef225-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="ef225-107">Il metodo **CopyTo** copia un numero specificato di byte dal puntatore di ricerca corrente nell'oggetto al puntatore di ricerca corrente in un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="ef225-107">The **CopyTo** method copies a specified number of bytes from the current seek pointer in the object to the current seek pointer in another object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef225-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef225-108">Syntax</span></span>


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="ef225-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef225-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef225-110">*pByteBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef225-110">*pByteBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef225-111">Punta al flusso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ef225-111">Points to the destination stream.</span></span> <span data-ttu-id="ef225-112">Il flusso a cui punta *pByteBuffer* può essere un nuovo flusso o un clone del flusso di origine.</span><span class="sxs-lookup"><span data-stu-id="ef225-112">The stream pointed to by *pByteBuffer* can be a new stream or a clone of the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="ef225-113">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef225-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef225-114">Numero di byte da copiare dal flusso di origine.</span><span class="sxs-lookup"><span data-stu-id="ef225-114">Number of bytes to copy from the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="ef225-115">*pcbRead* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ef225-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef225-116">Puntatore alla posizione in cui questo metodo scrive il numero effettivo di byte letti dall'origine.</span><span class="sxs-lookup"><span data-stu-id="ef225-116">Pointer to the location where this method writes the actual number of bytes read from the source.</span></span> <span data-ttu-id="ef225-117">È possibile impostare questo puntatore su **null** per indicare che non si è interessati a questo valore.</span><span class="sxs-lookup"><span data-stu-id="ef225-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="ef225-118">In questo caso, questo metodo non fornisce il numero effettivo di byte letti.</span><span class="sxs-lookup"><span data-stu-id="ef225-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="ef225-119">*pcbWritten* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ef225-119">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef225-120">Puntatore alla posizione in cui questo metodo scrive il numero effettivo di byte scritti nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="ef225-120">Pointer to the location where this method writes the actual number of bytes written to the destination.</span></span> <span data-ttu-id="ef225-121">È possibile impostare questo puntatore su **null** per indicare che non si è interessati a questo valore.</span><span class="sxs-lookup"><span data-stu-id="ef225-121">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="ef225-122">In questo caso, questo metodo non fornisce il numero effettivo di byte scritti.</span><span class="sxs-lookup"><span data-stu-id="ef225-122">In this case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef225-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef225-123">Return value</span></span>

<span data-ttu-id="ef225-124">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ef225-124">The return value is an **HRESULT**.</span></span> <span data-ttu-id="ef225-125">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="ef225-125">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef225-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef225-126">Remarks</span></span>

<span data-ttu-id="ef225-127">Questo metodo copia i byte specificati da un flusso a un altro.</span><span class="sxs-lookup"><span data-stu-id="ef225-127">This method copies the specified bytes from one stream to another.</span></span> <span data-ttu-id="ef225-128">Può anche essere usato per copiare un flusso in se stesso.</span><span class="sxs-lookup"><span data-stu-id="ef225-128">It can also be used to copy a stream to itself.</span></span> <span data-ttu-id="ef225-129">Il puntatore Seek in ogni istanza del flusso viene regolato per il numero di byte letti o scritti.</span><span class="sxs-lookup"><span data-stu-id="ef225-129">The seek pointer in each stream instance is adjusted for the number of bytes read or written.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef225-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef225-130">Requirements</span></span>



| <span data-ttu-id="ef225-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef225-131">Requirement</span></span> | <span data-ttu-id="ef225-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ef225-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef225-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef225-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ef225-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ef225-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ef225-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef225-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ef225-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef225-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef225-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ef225-137">End of client support</span></span><br/>    | <span data-ttu-id="ef225-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ef225-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ef225-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ef225-139">End of server support</span></span><br/>    | <span data-ttu-id="ef225-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef225-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ef225-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef225-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef225-142"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef225-142"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef225-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ef225-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="ef225-144"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ef225-144"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ef225-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ef225-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef225-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef225-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef225-147">IID</span><span class="sxs-lookup"><span data-stu-id="ef225-147">IID</span></span><br/>                      | <span data-ttu-id="ef225-148">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="ef225-148">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

