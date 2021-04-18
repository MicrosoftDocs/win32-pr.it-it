---
description: La proprietà ProductCode è un identificatore univoco per la versione specifica del prodotto, rappresentata come GUID di stringa, ad esempio &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: Proprietà ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330620"
---
# <a name="productcode-property"></a><span data-ttu-id="db621-103">Proprietà ProductCode</span><span class="sxs-lookup"><span data-stu-id="db621-103">ProductCode property</span></span>

<span data-ttu-id="db621-104">La proprietà **ProductCode** è un identificatore univoco per la versione specifica del prodotto, rappresentata come [GUID](guid.md)di stringa, ad esempio " {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="db621-104">The **ProductCode** property is a unique identifier for the particular product release, represented as a string [GUID](guid.md), for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="db621-105">Le lettere usate in questo GUID devono essere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="db621-105">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="db621-106">Questo ID deve variare per versioni e linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="db621-106">This ID must vary for different versions and languages.</span></span>

<span data-ttu-id="db621-107">Un aggiornamento del prodotto che aggiorna un prodotto in un prodotto completamente nuovo deve modificare anche il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="db621-107">A product upgrade that updates a product into an entirely new product must also change the product code.</span></span> <span data-ttu-id="db621-108">Alle versioni a 32 bit e a 64 bit del pacchetto di un'applicazione devono essere assegnati codici di prodotto diversi.</span><span class="sxs-lookup"><span data-stu-id="db621-108">The 32-bit and 64-bit versions of an application's package must be assigned different product codes.</span></span>

<span data-ttu-id="db621-109">**ProductCode** viene annunciato come una proprietà del prodotto ed è il metodo principale per specificare il prodotto.</span><span class="sxs-lookup"><span data-stu-id="db621-109">The **ProductCode** is advertised as a product property, and is the primary method of specifying the product.</span></span> <span data-ttu-id="db621-110">Questa proprietà è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="db621-110">This property is REQUIRED.</span></span>

## <a name="requirements"></a><span data-ttu-id="db621-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db621-111">Requirements</span></span>



| <span data-ttu-id="db621-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="db621-112">Requirement</span></span> | <span data-ttu-id="db621-113">Valore</span><span class="sxs-lookup"><span data-stu-id="db621-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db621-114">Versione</span><span class="sxs-lookup"><span data-stu-id="db621-114">Version</span></span><br/> | <span data-ttu-id="db621-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="db621-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="db621-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="db621-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="db621-117">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="db621-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="db621-118">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="db621-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db621-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db621-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db621-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="db621-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




