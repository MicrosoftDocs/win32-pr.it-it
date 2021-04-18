---
description: Il valore della proprietà riepilogo oggetto comunica il nome del prodotto, della trasformazione o della patch installata dal pacchetto.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Proprietà di riepilogo oggetto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327312"
---
# <a name="subject-summary-property"></a><span data-ttu-id="5104e-103">Proprietà di riepilogo oggetto</span><span class="sxs-lookup"><span data-stu-id="5104e-103">Subject Summary property</span></span>

<span data-ttu-id="5104e-104">Il valore della proprietà **Riepilogo oggetto** comunica il nome del prodotto, della trasformazione o della patch installata dal pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5104e-104">The value of the **Subject Summary** property conveys the name of the product, transform, or patch that is installed by the package.</span></span>

<span data-ttu-id="5104e-105">Per fornire il valore di questa proprietà nelle informazioni di riepilogo, spetta all'autore di un database di installazione, di una trasformazione o di un pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="5104e-105">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="5104e-106">Per determinare il valore corretto, gli autori devono eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="5104e-106">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="5104e-107">Impostare la proprietà **Summary del soggetto** in un pacchetto di installazione sullo stesso valore della proprietà [**ProductName**](productname.md) .</span><span class="sxs-lookup"><span data-stu-id="5104e-107">Set the **Subject Summary** property in an installation package to the same value as the [**ProductName**](productname.md) property.</span></span>
-   <span data-ttu-id="5104e-108">Impostare la proprietà **Riepilogo oggetto** in una trasformazione sullo stesso valore della proprietà **Riepilogo oggetto** nel pacchetto di installazione originale.</span><span class="sxs-lookup"><span data-stu-id="5104e-108">Set the **Subject Summary** property in a transform to the same value as the **Subject Summary** property in the original installation package.</span></span>
-   <span data-ttu-id="5104e-109">Impostare la proprietà **Riepilogo oggetto** nelle informazioni di riepilogo di un pacchetto di patch su una breve descrizione della patch che include il nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="5104e-109">Set the **Subject Summary** property in the summary information of a patch package to a short description of the patch that includes the name of the product.</span></span>

## <a name="requirements"></a><span data-ttu-id="5104e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5104e-110">Requirements</span></span>



| <span data-ttu-id="5104e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5104e-111">Requirement</span></span> | <span data-ttu-id="5104e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5104e-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5104e-113">Versione</span><span class="sxs-lookup"><span data-stu-id="5104e-113">Version</span></span><br/> | <span data-ttu-id="5104e-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5104e-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5104e-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5104e-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5104e-116">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="5104e-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5104e-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5104e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5104e-118">**PATCHNEWSUMMARYSUBJECT**</span><span class="sxs-lookup"><span data-stu-id="5104e-118">**PATCHNEWSUMMARYSUBJECT**</span></span>](patchnewsummarysubject.md)
</dt> <dt>

[<span data-ttu-id="5104e-119">Descrizioni delle proprietà di riepilogo</span><span class="sxs-lookup"><span data-stu-id="5104e-119">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




