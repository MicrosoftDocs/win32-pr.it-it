---
description: Ottiene un certificato per un driver di visualizzazione.
ms.assetid: eceaf151-1dae-4ff0-9139-7f1789f6c682
title: Funzione GetCertificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificate
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 30cb17345177b552e51120afd00758a3f6886584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305374"
---
# <a name="getcertificate-function"></a><span data-ttu-id="fb87e-103">Funzione GetCertificate</span><span class="sxs-lookup"><span data-stu-id="fb87e-103">GetCertificate function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb87e-104">Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="fb87e-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="fb87e-105">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="fb87e-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="fb87e-106">Ottiene un certificato per un driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="fb87e-106">Gets a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb87e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb87e-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificate(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ BYTE                     *pbCertificate,
  _Out_ ULONG                    ulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="fb87e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb87e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb87e-109">*pstrDeviceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb87e-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb87e-110">Puntatore a una struttura [**di \_ stringhe Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="fb87e-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="fb87e-111">*ctPVPCertificateType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb87e-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb87e-112">Tipo di certificato, specificato come membro dell'enumerazione del **tipo di \_ certificato \_ DXGKMDT** .</span><span class="sxs-lookup"><span data-stu-id="fb87e-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="fb87e-113">*pbCertificate* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb87e-113">*pbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb87e-114">Puntatore a un buffer che riceve il certificato.</span><span class="sxs-lookup"><span data-stu-id="fb87e-114">A pointer to a buffer that receives the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="fb87e-115">*ulCertificateLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb87e-115">*ulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb87e-116">Dimensioni in byte del buffer *pbCertificate* .</span><span class="sxs-lookup"><span data-stu-id="fb87e-116">The size of the *pbCertificate* buffer, in bytes.</span></span> <span data-ttu-id="fb87e-117">Per ottenere le dimensioni del certificato, chiamare [**GetCertificateSize**](getcertificatesize.md).</span><span class="sxs-lookup"><span data-stu-id="fb87e-117">To get the size of the certificate, call [**GetCertificateSize**](getcertificatesize.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb87e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb87e-118">Return value</span></span>

<span data-ttu-id="fb87e-119">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="fb87e-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="fb87e-120">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="fb87e-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb87e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb87e-121">Remarks</span></span>

<span data-ttu-id="fb87e-122">Le applicazioni devono chiamare il metodo [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) anziché questa funzione.</span><span class="sxs-lookup"><span data-stu-id="fb87e-122">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="fb87e-123">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="fb87e-123">This function has no associated import library.</span></span> <span data-ttu-id="fb87e-124">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="fb87e-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb87e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb87e-125">Requirements</span></span>



| <span data-ttu-id="fb87e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb87e-126">Requirement</span></span> | <span data-ttu-id="fb87e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fb87e-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fb87e-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb87e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fb87e-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb87e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fb87e-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb87e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fb87e-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb87e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fb87e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fb87e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb87e-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb87e-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb87e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb87e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb87e-135">Funzioni di OPM</span><span class="sxs-lookup"><span data-stu-id="fb87e-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="fb87e-136">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="fb87e-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
