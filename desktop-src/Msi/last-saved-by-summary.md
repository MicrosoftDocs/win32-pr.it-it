---
description: Il programma di installazione imposta l'ultima proprietà salvata da riepilogo su un valore che dipende dal fatto che si tratti di un pacchetto di installazione, una trasformazione o un pacchetto di patch. In un pacchetto di installazione, il programma di installazione imposta questa proprietà sul valore della proprietà LogonUser durante un'installazione amministrativa. Gli sviluppatori di strumenti di modifica del database possono utilizzare questa proprietà durante il processo di sviluppo per tenere traccia dell'ultima persona che ha modificato il database di installazione. Questa proprietà deve essere impostata su null in un database di spedizione finale. Il programma di installazione non usa mai questa proprietà e un utente non deve mai modificarla. In una trasformazione questa proprietà di riepilogo contiene gli ID della piattaforma e della lingua che un database deve avere dopo che è stato trasformato. La proprietà specifica l'elemento che deve essere impostato nel riepilogo del modello nel nuovo database. In un pacchetto di patch questa proprietà di riepilogo contiene un elenco delimitato da punti e virgola di nomi di sottoarchivi di trasformazione nell'ordine in cui sono applicati da questa patch.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Ultimo salvataggio da proprietà di riepilogo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330488"
---
# <a name="last-saved-by-summary-property"></a><span data-ttu-id="6a898-107">Ultimo salvataggio da proprietà di riepilogo</span><span class="sxs-lookup"><span data-stu-id="6a898-107">Last Saved By Summary property</span></span>

<span data-ttu-id="6a898-108">Il programma di installazione imposta l' **ultima proprietà salvata da riepilogo** su un valore che dipende dal fatto che si tratti di un pacchetto di installazione, una trasformazione o un pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="6a898-108">The installer sets the **Last Saved by Summary** Property to a value that depends on whether this is an installation package, transform, or patch package.</span></span>

<span data-ttu-id="6a898-109">In un pacchetto di installazione, il programma di installazione imposta questa proprietà sul valore della proprietà [**LogonUser**](logonuser.md) durante un' [installazione amministrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="6a898-109">In an installation package, the installer sets this property to the value of the [**LogonUser**](logonuser.md) property during an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="6a898-110">Gli sviluppatori di strumenti di modifica del database possono utilizzare questa proprietà durante il processo di sviluppo per tenere traccia dell'ultima persona che ha modificato il database di installazione.</span><span class="sxs-lookup"><span data-stu-id="6a898-110">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="6a898-111">Questa proprietà deve essere impostata su null in un database di spedizione finale.</span><span class="sxs-lookup"><span data-stu-id="6a898-111">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="6a898-112">Il programma di installazione non usa mai questa proprietà e un utente non deve mai modificarla.</span><span class="sxs-lookup"><span data-stu-id="6a898-112">The installer never uses this property and a user never needs to modify it.</span></span>

<span data-ttu-id="6a898-113">In una trasformazione questa proprietà di riepilogo contiene gli ID della piattaforma e della lingua che un database deve avere dopo che è stato trasformato.</span><span class="sxs-lookup"><span data-stu-id="6a898-113">In a transform, this summary property contains the platform and language ID(s) that a database should have after it has been transformed.</span></span> <span data-ttu-id="6a898-114">La proprietà specifica l'elemento che deve essere impostato nel [**Riepilogo del modello**](template-summary.md) nel nuovo database.</span><span class="sxs-lookup"><span data-stu-id="6a898-114">The property specifies to what the [**Template Summary**](template-summary.md) should be set in the new database.</span></span>

<span data-ttu-id="6a898-115">In un pacchetto di patch questa proprietà di riepilogo contiene un elenco delimitato da punti e virgola di nomi di sottoarchivi di trasformazione nell'ordine in cui sono applicati da questa patch.</span><span class="sxs-lookup"><span data-stu-id="6a898-115">In a patch package, this summary property contains a semicolon-delimited list of transform substorage names in the order they are applied by this patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a898-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a898-116">Requirements</span></span>



| <span data-ttu-id="6a898-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a898-117">Requirement</span></span> | <span data-ttu-id="6a898-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6a898-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a898-119">Versione</span><span class="sxs-lookup"><span data-stu-id="6a898-119">Version</span></span><br/> | <span data-ttu-id="6a898-120">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a898-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6a898-121">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a898-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6a898-122">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="6a898-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a898-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a898-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a898-124">Descrizioni delle proprietà di riepilogo</span><span class="sxs-lookup"><span data-stu-id="6a898-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




