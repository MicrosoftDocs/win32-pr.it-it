---
description: Segnala che è stato completato un particolare comando del navigatore DVD.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 550a3969ba431127b05234a0c9fe38eb5938ebf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325044"
---
# <a name="ec_dvd_cmd_end"></a><span data-ttu-id="71661-103">\_ \_ fine cmd DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="71661-103">EC\_DVD\_CMD\_END</span></span>

<span data-ttu-id="71661-104">Segnala che è stato completato un particolare comando del [navigatore DVD](dvd-navigator-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="71661-104">Signals that a particular [DVD Navigator](dvd-navigator-filter.md) command has completed.</span></span>

## <a name="parameters"></a><span data-ttu-id="71661-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="71661-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71661-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="71661-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="71661-107">Identificatore del comando.</span><span class="sxs-lookup"><span data-stu-id="71661-107">Command identifier.</span></span> <span data-ttu-id="71661-108">Passare questo parametro al metodo [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) per recuperare un puntatore a interfaccia [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .</span><span class="sxs-lookup"><span data-stu-id="71661-108">Pass this parameter to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method to retrieve an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) interface pointer.</span></span>

</dd> <dt>

<span data-ttu-id="71661-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="71661-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="71661-110">Valore **HRESULT** che indica lo stato del comando.</span><span class="sxs-lookup"><span data-stu-id="71661-110">**HRESULT** value indicating the status of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71661-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="71661-111">Remarks</span></span>

<span data-ttu-id="71661-112">Questo evento viene generato solo se l'applicazione imposta il flag SendEvents del DVD del \_ \_ flag CMD \_ in un metodo [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) che accetta un flag di [**\_ \_ flag CMD di DVD**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .</span><span class="sxs-lookup"><span data-stu-id="71661-112">This event is only fired if your application sets the DVD\_CMD\_FLAG\_SendEvents flag in an [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method that takes a [**DVD\_CMD\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) flag.</span></span>

<span data-ttu-id="71661-113">Questo evento viene generato nel dominio del titolo.</span><span class="sxs-lookup"><span data-stu-id="71661-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="71661-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71661-114">Requirements</span></span>



| <span data-ttu-id="71661-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="71661-115">Requirement</span></span> | <span data-ttu-id="71661-116">Valore</span><span class="sxs-lookup"><span data-stu-id="71661-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71661-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71661-117">Header</span></span><br/> | <dl> <span data-ttu-id="71661-118"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71661-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71661-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71661-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71661-120">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="71661-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="71661-121">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="71661-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="71661-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="71661-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="71661-123">Sincronizzazione dei comandi DVD</span><span class="sxs-lookup"><span data-stu-id="71661-123">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




