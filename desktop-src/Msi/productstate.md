---
description: Il programma di installazione imposta la proprietà ProductState sullo stato di installazione del prodotto in fase di inizializzazione.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Proprietà ProductState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333975"
---
# <a name="productstate-property"></a><span data-ttu-id="bb658-103">Proprietà ProductState</span><span class="sxs-lookup"><span data-stu-id="bb658-103">ProductState property</span></span>

<span data-ttu-id="bb658-104">Il programma di installazione imposta la proprietà **ProductState** sullo stato di installazione del prodotto in fase di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="bb658-104">The installer sets the **ProductState** property to the installation state for the product at initialization.</span></span> <span data-ttu-id="bb658-105">Questa proprietà è impostata su uno dei seguenti tipi di dati INSTALLSTATE restituiti da [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span><span class="sxs-lookup"><span data-stu-id="bb658-105">This property is set to one of the following INSTALLSTATE data types returned by [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span></span>



| <span data-ttu-id="bb658-106">INSTALLSTATE</span><span class="sxs-lookup"><span data-stu-id="bb658-106">INSTALLSTATE</span></span>             | <span data-ttu-id="bb658-107">Valore numerico</span><span class="sxs-lookup"><span data-stu-id="bb658-107">Numeric value</span></span> | <span data-ttu-id="bb658-108">Stato di installazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="bb658-108">Installation state of product</span></span>                   |
|--------------------------|---------------|-------------------------------------------------|
| <span data-ttu-id="bb658-109">INSTALLSTATE \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="bb658-109">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="bb658-110">-1</span><span class="sxs-lookup"><span data-stu-id="bb658-110">-1</span></span>            | <span data-ttu-id="bb658-111">Il prodotto non è né annunciato né installato.</span><span class="sxs-lookup"><span data-stu-id="bb658-111">The product is neither advertised or installed.</span></span> |
| <span data-ttu-id="bb658-112">INSTALLSTATE \_ annunciata</span><span class="sxs-lookup"><span data-stu-id="bb658-112">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="bb658-113">1</span><span class="sxs-lookup"><span data-stu-id="bb658-113">1</span></span>             | <span data-ttu-id="bb658-114">Il prodotto è annunciato ma non è installato.</span><span class="sxs-lookup"><span data-stu-id="bb658-114">The product is advertised but not installed.</span></span>    |
| <span data-ttu-id="bb658-115">INSTALLSTATE \_ assente</span><span class="sxs-lookup"><span data-stu-id="bb658-115">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="bb658-116">2</span><span class="sxs-lookup"><span data-stu-id="bb658-116">2</span></span>             | <span data-ttu-id="bb658-117">Il prodotto viene installato per un utente diverso.</span><span class="sxs-lookup"><span data-stu-id="bb658-117">The product is installed for a different user.</span></span>  |
| <span data-ttu-id="bb658-118">\_impostazione predefinita InstallState</span><span class="sxs-lookup"><span data-stu-id="bb658-118">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="bb658-119">5</span><span class="sxs-lookup"><span data-stu-id="bb658-119">5</span></span>             | <span data-ttu-id="bb658-120">Il prodotto è installato per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="bb658-120">The product is installed for the current user.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="bb658-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb658-121">Requirements</span></span>



| <span data-ttu-id="bb658-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb658-122">Requirement</span></span> | <span data-ttu-id="bb658-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bb658-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb658-124">Versione</span><span class="sxs-lookup"><span data-stu-id="bb658-124">Version</span></span><br/> | <span data-ttu-id="bb658-125">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bb658-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bb658-126">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bb658-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bb658-127">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb658-127">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bb658-128">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bb658-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb658-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb658-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb658-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb658-130">Properties</span></span>](properties.md)
</dt> </dl>

 

 




