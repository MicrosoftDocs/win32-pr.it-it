---
description: Disabilita le funzionalità di.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: pSetupSetGlobalFlags (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332370"
---
# <a name="psetupsetglobalflags-function"></a><span data-ttu-id="b8081-103">pSetupSetGlobalFlags (funzione)</span><span class="sxs-lookup"><span data-stu-id="b8081-103">pSetupSetGlobalFlags function</span></span>

<span data-ttu-id="b8081-104">\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="b8081-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="b8081-105">Disabilita le funzionalità di.</span><span class="sxs-lookup"><span data-stu-id="b8081-105">Disables features.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8081-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8081-106">Syntax</span></span>


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="b8081-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8081-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8081-108">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b8081-108">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8081-109">Flag utilizzati per disabilitare l'interfaccia utente o il backup automatico.</span><span class="sxs-lookup"><span data-stu-id="b8081-109">The flags used to disable user interface or automatic backup.</span></span>



| <span data-ttu-id="b8081-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b8081-110">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="b8081-111">Significato</span><span class="sxs-lookup"><span data-stu-id="b8081-111">Meaning</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <span data-ttu-id="b8081-112"><dt>**PSPGF \_**</dt> <dt>0X004</dt> non interattivo</span><span class="sxs-lookup"><span data-stu-id="b8081-112"><dt>**PSPGF\_NONINTERACTIVE**</dt> <dt>0x004</dt></span></span> </dl> | <span data-ttu-id="b8081-113">Impostare questa impostazione su Disabilita interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b8081-113">Set to disable user interface.</span></span><br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <span data-ttu-id="b8081-114"><dt>**PSPGF \_ Nessun \_ backup**</dt> <dt>0x002</dt></span><span class="sxs-lookup"><span data-stu-id="b8081-114"><dt>**PSPGF\_NO\_BACKUP**</dt> <dt>0x002</dt></span></span> </dl>               | <span data-ttu-id="b8081-115">Impostare per disabilitare il backup automatico.</span><span class="sxs-lookup"><span data-stu-id="b8081-115">Set to disable automatic backup.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8081-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8081-116">Return value</span></span>

<span data-ttu-id="b8081-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b8081-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8081-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8081-118">Remarks</span></span>

<span data-ttu-id="b8081-119">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b8081-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8081-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8081-120">Requirements</span></span>



| <span data-ttu-id="b8081-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8081-121">Requirement</span></span> | <span data-ttu-id="b8081-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b8081-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8081-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b8081-123">DLL</span></span><br/> | <dl> <span data-ttu-id="b8081-124"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8081-124"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
