---
title: Metodo WSMan. GetErrorMessage (WSManDisp. h)
description: Restituisce una stringa formattata che contiene il testo di un numero di errore.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del Metodo GetErrorMessage
- Metodo GetErrorMessage Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, Metodo GetErrorMessage
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340693"
---
# <a name="wsmangeterrormessage-method"></a><span data-ttu-id="8eb8f-106">WSMan. GetErrorMessage, metodo</span><span class="sxs-lookup"><span data-stu-id="8eb8f-106">WSMan.GetErrorMessage method</span></span>

<span data-ttu-id="8eb8f-107">Restituisce una stringa formattata che contiene il testo di un numero di errore.</span><span class="sxs-lookup"><span data-stu-id="8eb8f-107">Returns a formatted string that contains the text of an error number.</span></span> <span data-ttu-id="8eb8f-108">Questo metodo esegue la stessa operazione del *numero di errore decimale o esadecimale* della riga **di comando WinRM** **helpmsg** .</span><span class="sxs-lookup"><span data-stu-id="8eb8f-108">This method performs the same operation as the **Winrm** command-line **winrm helpmsg** *decimal or hexadecimal error number*.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb8f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8eb8f-109">Syntax</span></span>


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="8eb8f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8eb8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eb8f-111">*numero errore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8eb8f-111">*errorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eb8f-112">Numero del messaggio di errore in formato decimale o esadecimale da WinRM, WinHTTP o altri componenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8eb8f-112">An error message number in decimal or hexadecimal from WinRM, WinHTTP, or other operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="8eb8f-113">*ErrorMessage* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8eb8f-113">*errorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8eb8f-114">Stringa del messaggio di errore formattata come i messaggi restituiti dal comando **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="8eb8f-114">An error message string formatted like messages returned from the **Winrm** command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8eb8f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8eb8f-115">Remarks</span></span>

<span data-ttu-id="8eb8f-116">Il metodo C++ corrispondente è [**IWSManEx:: GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span><span class="sxs-lookup"><span data-stu-id="8eb8f-116">The corresponding C++ method is [**IWSManEx::GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb8f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8eb8f-117">Requirements</span></span>



| <span data-ttu-id="8eb8f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb8f-118">Requirement</span></span> | <span data-ttu-id="8eb8f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8eb8f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb8f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8eb8f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb8f-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8eb8f-121">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="8eb8f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8eb8f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb8f-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8eb8f-123">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8eb8f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8eb8f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eb8f-125"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eb8f-125"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8eb8f-126">IDL</span><span class="sxs-lookup"><span data-stu-id="8eb8f-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8eb8f-127"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8eb8f-127"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="8eb8f-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="8eb8f-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="8eb8f-129"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8eb8f-129"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8eb8f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8eb8f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eb8f-131"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eb8f-131"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8eb8f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8eb8f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb8f-133">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="8eb8f-133">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





