---
description: La proprietà riepilogo sicurezza indica se il pacchetto deve essere aperto in sola lettura.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Proprietà Riepilogo sicurezza
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331785"
---
# <a name="security-summary-property"></a><span data-ttu-id="827ca-103">Proprietà Riepilogo sicurezza</span><span class="sxs-lookup"><span data-stu-id="827ca-103">Security Summary property</span></span>

<span data-ttu-id="827ca-104">La proprietà **Riepilogo sicurezza** indica se il pacchetto deve essere aperto in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="827ca-104">The **Security Summary** property conveys whether the package should be opened as read-only.</span></span> <span data-ttu-id="827ca-105">Lo strumento di modifica del database non deve modificare un database applicato di sola lettura e deve generare un avviso in caso di tentativi di modifica di un database consigliato di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="827ca-105">The database editing tool should not modify a read-only enforced database and should issue a warning at attempts to modify a read-only recommended database.</span></span> <span data-ttu-id="827ca-106">I seguenti valori di questa proprietà sono applicabili ai file di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="827ca-106">The following values of this property are applicable to Windows Installer files.</span></span>



| <span data-ttu-id="827ca-107">Valore</span><span class="sxs-lookup"><span data-stu-id="827ca-107">Value</span></span> | <span data-ttu-id="827ca-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="827ca-108">Description</span></span>           |
|-------|-----------------------|
| <span data-ttu-id="827ca-109">0</span><span class="sxs-lookup"><span data-stu-id="827ca-109">0</span></span>     | <span data-ttu-id="827ca-110">Nessuna restrizione</span><span class="sxs-lookup"><span data-stu-id="827ca-110">No restriction</span></span>        |
| <span data-ttu-id="827ca-111">2</span><span class="sxs-lookup"><span data-stu-id="827ca-111">2</span></span>     | <span data-ttu-id="827ca-112">Di sola lettura consigliata</span><span class="sxs-lookup"><span data-stu-id="827ca-112">Read-only recommended</span></span> |
| <span data-ttu-id="827ca-113">4</span><span class="sxs-lookup"><span data-stu-id="827ca-113">4</span></span>     | <span data-ttu-id="827ca-114">Applicazione di sola lettura</span><span class="sxs-lookup"><span data-stu-id="827ca-114">Read-only enforced</span></span>    |



 

<span data-ttu-id="827ca-115">Questa proprietà deve essere impostata su sola lettura consigliata (2) per un database di installazione e per l'applicazione di sola lettura (4) per una trasformazione o una patch.</span><span class="sxs-lookup"><span data-stu-id="827ca-115">This property should be set to read-only recommended (2) for an installation database and to read-only enforced (4) for a transform or patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="827ca-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="827ca-116">Requirements</span></span>



| <span data-ttu-id="827ca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="827ca-117">Requirement</span></span> | <span data-ttu-id="827ca-118">Valore</span><span class="sxs-lookup"><span data-stu-id="827ca-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="827ca-119">Versione</span><span class="sxs-lookup"><span data-stu-id="827ca-119">Version</span></span><br/> | <span data-ttu-id="827ca-120">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="827ca-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="827ca-121">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="827ca-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="827ca-122">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="827ca-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="827ca-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="827ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="827ca-124">Descrizioni delle proprietà di riepilogo</span><span class="sxs-lookup"><span data-stu-id="827ca-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




