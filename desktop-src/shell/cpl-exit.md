---
description: Inviato una sola volta alla funzione CPlApplet di un'applicazione del pannello di controllo prima che venga rilasciata la DLL contenente l'applicazione del pannello di controllo.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: Messaggio CPL_EXIT (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225929"
---
# <a name="cpl_exit-message"></a><span data-ttu-id="0e6e7-103">\_Messaggio di uscita cpl</span><span class="sxs-lookup"><span data-stu-id="0e6e7-103">CPL\_EXIT message</span></span>

<span data-ttu-id="0e6e7-104">Inviato una sola volta alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo prima che venga rilasciata la DLL contenente l'applicazione del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="0e6e7-104">Sent once to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application before the DLL containing the Control Panel application is released.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e6e7-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e6e7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e6e7-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e6e7-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0e6e7-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0e6e7-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0e6e7-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e6e7-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0e6e7-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0e6e7-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e6e7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e6e7-110">Return value</span></span>

<span data-ttu-id="0e6e7-111">Se la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora correttamente questo messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="0e6e7-111">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e6e7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e6e7-112">Remarks</span></span>

<span data-ttu-id="0e6e7-113">Questo messaggio viene inviato dopo l'invio dell'ultimo messaggio di [**\_ arresto cpl**](cpl-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="0e6e7-113">This message is sent after the last [**CPL\_STOP**](cpl-stop.md) message is sent.</span></span>

<span data-ttu-id="0e6e7-114">In risposta a questo messaggio, un'applicazione del pannello di controllo deve liberare la memoria allocata ed eseguire la pulizia a livello globale.</span><span class="sxs-lookup"><span data-stu-id="0e6e7-114">In response to this message, a Control Panel application must free any memory that it has allocated and perform global-level cleanup.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e6e7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e6e7-115">Requirements</span></span>



| <span data-ttu-id="0e6e7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e6e7-116">Requirement</span></span> | <span data-ttu-id="0e6e7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0e6e7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0e6e7-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e6e7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0e6e7-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0e6e7-119">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0e6e7-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e6e7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0e6e7-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e6e7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0e6e7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e6e7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e6e7-123"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e6e7-123"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e6e7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e6e7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e6e7-125">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="0e6e7-125">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
