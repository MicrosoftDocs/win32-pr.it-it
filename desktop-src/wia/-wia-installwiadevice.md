---
description: La funzione InstallWiaDevice installa un dispositivo Windows Image Acquisition (WIA) come dispositivo con enumerazione radice. È possibile che venga visualizzato un avviso di sicurezza se un file di installazione o un coinstallatore non è firmato digitalmente e considerato attendibile.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Funzione InstallWiaDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752863"
---
# <a name="installwiadevice-function"></a><span data-ttu-id="93df7-104">InstallWiaDevice (funzione)</span><span class="sxs-lookup"><span data-stu-id="93df7-104">InstallWiaDevice function</span></span>

<span data-ttu-id="93df7-105">La funzione **InstallWiaDevice** installa un dispositivo Windows Image Acquisition (WIA) come dispositivo con enumerazione radice.</span><span class="sxs-lookup"><span data-stu-id="93df7-105">The **InstallWiaDevice** function installs a Windows Image Acquisition (WIA) device as root-enumerated device.</span></span> <span data-ttu-id="93df7-106">È possibile che venga visualizzato un avviso di sicurezza se un file di installazione o un coinstallatore non è firmato digitalmente e considerato attendibile.</span><span class="sxs-lookup"><span data-stu-id="93df7-106">It may popup a security warning if any installing file or coinstaller is not digitally signed and trusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="93df7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93df7-107">Syntax</span></span>


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a><span data-ttu-id="93df7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="93df7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93df7-109">*pWiaDeviceInstall* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93df7-109">*pWiaDeviceInstall* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93df7-110">Tipo: \**PWIADEVICEINSTALL \** _</span><span class="sxs-lookup"><span data-stu-id="93df7-110">Type: \**PWIADEVICEINSTALL\** _</span></span>

<span data-ttu-id="93df7-111">Puntatore a una struttura WIADEVICEINSTALL.</span><span class="sxs-lookup"><span data-stu-id="93df7-111">Pointer to a WIADEVICEINSTALL structure.</span></span> <span data-ttu-id="93df7-112">Il membro _szFriendlyName \* della struttura deve essere impostato sull'effettivo dispositivo FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="93df7-112">The _szFriendlyName\* member of the structure must be set to the actual device FriendlyName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93df7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93df7-113">Return value</span></span>

<span data-ttu-id="93df7-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="93df7-114">Type: **DWORD**</span></span>

<span data-ttu-id="93df7-115">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="93df7-115">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="93df7-116">Se la funzione ha esito negativo, restituisce un codice di errore Win32.</span><span class="sxs-lookup"><span data-stu-id="93df7-116">If the function fails, it returns a Win32 error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="93df7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93df7-117">Requirements</span></span>



| <span data-ttu-id="93df7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="93df7-118">Requirement</span></span> | <span data-ttu-id="93df7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="93df7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93df7-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93df7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="93df7-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93df7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="93df7-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93df7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="93df7-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93df7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="93df7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93df7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="93df7-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="93df7-125"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="93df7-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="93df7-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="93df7-127"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93df7-127"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




