---
description: La proprietà di riepilogo del numero di caratteri viene utilizzata solo nelle trasformazioni.
ms.assetid: d26d24a5-558e-4333-ae39-ffba1bbc5247
title: Proprietà riepilogo Conteggio caratteri
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afc99c065721f0f0b94691a12e00204305940efd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328450"
---
# <a name="character-count-summary-property"></a><span data-ttu-id="50ea2-103">Proprietà riepilogo Conteggio caratteri</span><span class="sxs-lookup"><span data-stu-id="50ea2-103">Character Count Summary property</span></span>

<span data-ttu-id="50ea2-104">La proprietà di **Riepilogo del numero di caratteri** viene utilizzata solo nelle trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="50ea2-104">The **Character Count Summary** property is only used in transforms.</span></span> <span data-ttu-id="50ea2-105">Questa parte del flusso di informazioni di riepilogo è divisa in parole a 2 16 bit.</span><span class="sxs-lookup"><span data-stu-id="50ea2-105">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="50ea2-106">La parola superiore contiene i [*flag di convalida della trasformazione*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50ea2-106">The upper word contains the [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="50ea2-107">La parola inferiore contiene i [*flag di condizione di errore di trasformazione*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50ea2-107">The lower word contains the [*transform error condition flags*](t-gly.md).</span></span>

<span data-ttu-id="50ea2-108">Questa proprietà deve essere null in un pacchetto di installazione o in un pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="50ea2-108">This property should be Null in an installation package or patch package.</span></span>

## <a name="requirements"></a><span data-ttu-id="50ea2-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50ea2-109">Requirements</span></span>



| <span data-ttu-id="50ea2-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="50ea2-110">Requirement</span></span> | <span data-ttu-id="50ea2-111">Valore</span><span class="sxs-lookup"><span data-stu-id="50ea2-111">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ea2-112">Versione</span><span class="sxs-lookup"><span data-stu-id="50ea2-112">Version</span></span><br/> | <span data-ttu-id="50ea2-113">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="50ea2-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="50ea2-114">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="50ea2-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="50ea2-115">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="50ea2-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50ea2-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50ea2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ea2-117">Descrizioni delle proprietà di riepilogo</span><span class="sxs-lookup"><span data-stu-id="50ea2-117">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




