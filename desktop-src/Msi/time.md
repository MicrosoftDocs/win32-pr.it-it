---
description: "La proprietà Time è l'ora corrente in ore, minuti e secondi come una stringa di testo letterale nel formato HH: MM: SS usando un clock a 24 ore."
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Proprietà Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330139"
---
# <a name="time-property"></a><span data-ttu-id="e7b82-103">Proprietà Time</span><span class="sxs-lookup"><span data-stu-id="e7b82-103">Time property</span></span>

<span data-ttu-id="e7b82-104">La proprietà **Time** è l'ora corrente in ore, minuti e secondi come una stringa di testo letterale nel formato HH: mm: SS usando un clock a 24 ore.</span><span class="sxs-lookup"><span data-stu-id="e7b82-104">The **Time** property is the current time in hours, minutes, and seconds as a string of literal text in the format HH:MM:SS using a 24 hour clock.</span></span> <span data-ttu-id="e7b82-105">Ad esempio, l'ora 6:57</span><span class="sxs-lookup"><span data-stu-id="e7b82-105">For example, the time 6:57 p.m.</span></span> <span data-ttu-id="e7b82-106">è rappresentato da "18:57:00".</span><span class="sxs-lookup"><span data-stu-id="e7b82-106">is represented by "18:57:00".</span></span> <span data-ttu-id="e7b82-107">Il formato del valore dipende dalle impostazioni locali dell'utente e è il formato ottenuto usando la funzione [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) con l' \_ opzione Time FORCE24HOURFORMAT \| time \_ NOTIMEMARKER.</span><span class="sxs-lookup"><span data-stu-id="e7b82-107">The format of the value depends upon the user's locale, and is the format obtained using [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) function with the TIME\_FORCE24HOURFORMAT \| TIME\_NOTIMEMARKER option.</span></span> <span data-ttu-id="e7b82-108">Il valore di questa proprietà viene impostato dal Windows Installer e non dall'autore del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e7b82-108">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b82-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7b82-109">Remarks</span></span>

<span data-ttu-id="e7b82-110">Poiché si tratta di una stringa di testo, non può essere utilizzata nelle espressioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="e7b82-110">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b82-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7b82-111">Requirements</span></span>



| <span data-ttu-id="e7b82-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b82-112">Requirement</span></span> | <span data-ttu-id="e7b82-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e7b82-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b82-114">Versione</span><span class="sxs-lookup"><span data-stu-id="e7b82-114">Version</span></span><br/> | <span data-ttu-id="e7b82-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e7b82-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e7b82-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e7b82-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e7b82-117">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e7b82-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e7b82-118">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e7b82-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7b82-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7b82-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b82-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7b82-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 
