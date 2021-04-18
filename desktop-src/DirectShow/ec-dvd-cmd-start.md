---
description: Segnala che è stato avviato un comando per lo strumento di spostamento DVD.
ms.assetid: 230116b4-23f1-4c37-a781-da2c5aa20a1f
title: EC_DVD_CMD_START (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0fb723b220bf8aa12baa7133c9985225d6051921
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325043"
---
# <a name="ec_dvd_cmd_start"></a><span data-ttu-id="a5f68-103">\_ \_ avvio cmd DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="a5f68-103">EC\_DVD\_CMD\_START</span></span>

<span data-ttu-id="a5f68-104">Segnala che è stato avviato un comando per lo [strumento di spostamento DVD](dvd-navigator-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f68-104">Signals that a [DVD Navigator](dvd-navigator-filter.md) command has begun.</span></span>

## <a name="parameters"></a><span data-ttu-id="a5f68-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5f68-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f68-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a5f68-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a5f68-107">Identificatore del comando.</span><span class="sxs-lookup"><span data-stu-id="a5f68-107">Command identifier.</span></span> <span data-ttu-id="a5f68-108">Passare questo parametro al metodo [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) per recuperare un puntatore a interfaccia [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .</span><span class="sxs-lookup"><span data-stu-id="a5f68-108">Pass this parameter to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method to retrieve an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) interface pointer.</span></span>

</dd> <dt>

<span data-ttu-id="a5f68-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a5f68-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a5f68-110">Valore **HRESULT** che indica lo stato del comando.</span><span class="sxs-lookup"><span data-stu-id="a5f68-110">**HRESULT** value indicating the status of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5f68-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5f68-111">Remarks</span></span>

<span data-ttu-id="a5f68-112">Questo evento viene generato solo se l'applicazione imposta il flag **SendEvents del DVD del \_ \_ flag \_ cmd** in un metodo [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) che accetta un flag di [**\_ \_ flag CMD di DVD**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .</span><span class="sxs-lookup"><span data-stu-id="a5f68-112">This event is only fired if your application sets the **DVD\_CMD\_FLAG\_SendEvents** flag in an [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method that takes a [**DVD\_CMD\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) flag.</span></span>

<span data-ttu-id="a5f68-113">Questo evento viene generato nel dominio del titolo.</span><span class="sxs-lookup"><span data-stu-id="a5f68-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f68-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5f68-114">Requirements</span></span>



| <span data-ttu-id="a5f68-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5f68-115">Requirement</span></span> | <span data-ttu-id="a5f68-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a5f68-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f68-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5f68-117">Header</span></span><br/> | <dl> <span data-ttu-id="a5f68-118"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5f68-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5f68-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5f68-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f68-120">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="a5f68-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="a5f68-121">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="a5f68-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a5f68-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a5f68-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="a5f68-123">Sincronizzazione dei comandi DVD</span><span class="sxs-lookup"><span data-stu-id="a5f68-123">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




