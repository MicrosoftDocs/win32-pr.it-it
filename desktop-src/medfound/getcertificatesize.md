---
description: Ottiene le dimensioni di un certificato per un driver di visualizzazione.
ms.assetid: fd52e939-127a-4493-8406-31f7767921cd
title: GetCertificateSize (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateSize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bcd1f49ce65978c6a89c89cee1fda38e41434065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342456"
---
# <a name="getcertificatesize-function"></a><span data-ttu-id="9086f-103">GetCertificateSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="9086f-103">GetCertificateSize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9086f-104">Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9086f-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="9086f-105">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="9086f-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="9086f-106">Ottiene le dimensioni di un certificato per un driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9086f-106">Gets the size of a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="9086f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9086f-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificateSize(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ ULONG                    *pulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="9086f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9086f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9086f-109">*pstrDeviceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9086f-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9086f-110">Puntatore a una struttura [**di \_ stringhe Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="9086f-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="9086f-111">*ctPVPCertificateType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9086f-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9086f-112">Tipo di certificato, specificato come membro dell'enumerazione del **tipo di \_ certificato \_ DXGKMDT** .</span><span class="sxs-lookup"><span data-stu-id="9086f-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="9086f-113">*pulCertificateLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9086f-113">*pulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9086f-114">Riceve le dimensioni in byte del certificato.</span><span class="sxs-lookup"><span data-stu-id="9086f-114">Receives the size of the certificate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9086f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9086f-115">Return value</span></span>

<span data-ttu-id="9086f-116">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="9086f-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="9086f-117">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="9086f-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9086f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="9086f-118">Remarks</span></span>

<span data-ttu-id="9086f-119">Le applicazioni devono chiamare il metodo [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) anziché questa funzione.</span><span class="sxs-lookup"><span data-stu-id="9086f-119">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="9086f-120">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="9086f-120">This function has no associated import library.</span></span> <span data-ttu-id="9086f-121">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="9086f-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="9086f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9086f-122">Requirements</span></span>



| <span data-ttu-id="9086f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9086f-123">Requirement</span></span> | <span data-ttu-id="9086f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9086f-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9086f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9086f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9086f-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9086f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9086f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9086f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9086f-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9086f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9086f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9086f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9086f-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9086f-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9086f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9086f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9086f-132">Funzioni di OPM</span><span class="sxs-lookup"><span data-stu-id="9086f-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="9086f-133">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="9086f-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
