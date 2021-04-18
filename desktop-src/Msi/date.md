---
description: La proprietà date è il mese, il giorno e l'anno correnti come una stringa di testo letterale nel formato MM/gg/aaaa.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: proprietà Date
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330382"
---
# <a name="date-property"></a><span data-ttu-id="c1dfb-103">proprietà Date</span><span class="sxs-lookup"><span data-stu-id="c1dfb-103">Date property</span></span>

<span data-ttu-id="c1dfb-104">La proprietà **date** è il mese, il giorno e l'anno correnti come una stringa di testo letterale nel formato mm/gg/aaaa.</span><span class="sxs-lookup"><span data-stu-id="c1dfb-104">The **Date** property is the current month, day, and year as a string of literal text in the format MM/DD/YYYY.</span></span> <span data-ttu-id="c1dfb-105">Ad esempio, la data 22 giugno 2005 può essere rappresentata come "06/22/2005".</span><span class="sxs-lookup"><span data-stu-id="c1dfb-105">For example, the date June 22, 2005 can represented as "06/22/2005".</span></span> <span data-ttu-id="c1dfb-106">Il formato del valore dipende dalle impostazioni locali dell'utente e è il formato ottenuto usando [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) con l' \_ opzione date shortdate.</span><span class="sxs-lookup"><span data-stu-id="c1dfb-106">The format of the value depends upon the user's locale, and is the format obtained using [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) with the DATE\_SHORTDATE option.</span></span> <span data-ttu-id="c1dfb-107">Il valore di questa proprietà viene impostato dal Windows Installer e non dall'autore del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c1dfb-107">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1dfb-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1dfb-108">Remarks</span></span>

<span data-ttu-id="c1dfb-109">Poiché si tratta di una stringa di testo, non può essere utilizzata nelle espressioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="c1dfb-109">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1dfb-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1dfb-110">Requirements</span></span>



| <span data-ttu-id="c1dfb-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1dfb-111">Requirement</span></span> | <span data-ttu-id="c1dfb-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c1dfb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dfb-113">Versione</span><span class="sxs-lookup"><span data-stu-id="c1dfb-113">Version</span></span><br/> | <span data-ttu-id="c1dfb-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c1dfb-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c1dfb-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c1dfb-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c1dfb-116">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c1dfb-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c1dfb-117">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c1dfb-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1dfb-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1dfb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1dfb-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1dfb-119">Properties</span></span>](properties.md)
</dt> </dl>

 

