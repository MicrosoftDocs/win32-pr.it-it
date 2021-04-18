---
description: Crea un gestore del flusso di byte per l'origine dei supporti MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: MFCreateMP3ByteStreamPlugin (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308413"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a><span data-ttu-id="61194-103">MFCreateMP3ByteStreamPlugin (funzione)</span><span class="sxs-lookup"><span data-stu-id="61194-103">MFCreateMP3ByteStreamPlugin function</span></span>

<span data-ttu-id="61194-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="61194-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="61194-105">Al contrario, le applicazioni devono usare il [resolver di origine](source-resolver.md) per creare l'origine multimediale MP3.\]</span><span class="sxs-lookup"><span data-stu-id="61194-105">Instead, applications should use the [Source Resolver](source-resolver.md) to create the MP3 media source.\]</span></span>

<span data-ttu-id="61194-106">Crea un gestore del flusso di byte per l'origine dei supporti MP3.</span><span class="sxs-lookup"><span data-stu-id="61194-106">Creates a byte-stream handler for the MP3 media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="61194-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61194-107">Syntax</span></span>


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a><span data-ttu-id="61194-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="61194-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61194-109">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61194-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61194-110">Identificatore di interfaccia (IID) dell'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="61194-110">The interface identifier (IID) of the requested interface.</span></span> <span data-ttu-id="61194-111">Impostare questo parametro su **IID \_ IMFByteStreamHandler** per ricevere un puntatore all'interfaccia [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="61194-111">Set this parameter to **IID\_IMFByteStreamHandler** to receive a pointer to the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span>

</dd> <dt>

<span data-ttu-id="61194-112">*ppvHandler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="61194-112">*ppvHandler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61194-113">Riceve un puntatore all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="61194-113">Receives a pointer to the interface.</span></span> <span data-ttu-id="61194-114">Il chiamante deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="61194-114">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61194-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61194-115">Return value</span></span>

<span data-ttu-id="61194-116">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="61194-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="61194-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61194-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="61194-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="61194-118">Remarks</span></span>

<span data-ttu-id="61194-119">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="61194-119">This function has no associated import library.</span></span> <span data-ttu-id="61194-120">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a mf.dll.</span><span class="sxs-lookup"><span data-stu-id="61194-120">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to mf.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="61194-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61194-121">Requirements</span></span>



| <span data-ttu-id="61194-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="61194-122">Requirement</span></span> | <span data-ttu-id="61194-123">Valore</span><span class="sxs-lookup"><span data-stu-id="61194-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61194-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61194-124">Minimum supported client</span></span><br/> | <span data-ttu-id="61194-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61194-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="61194-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61194-126">Minimum supported server</span></span><br/> | <span data-ttu-id="61194-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61194-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="61194-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="61194-128">End of client support</span></span><br/>    | <span data-ttu-id="61194-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61194-129">Windows Vista</span></span><br/>                             |
| <span data-ttu-id="61194-130">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="61194-130">End of server support</span></span><br/>    | <span data-ttu-id="61194-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61194-131">Windows Server 2008</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="61194-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61194-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61194-133">Funzioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="61194-133">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> <dt>

[<span data-ttu-id="61194-134">Gestori di schemi e gestori di Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="61194-134">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="61194-135">Resolver di origine</span><span class="sxs-lookup"><span data-stu-id="61194-135">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
