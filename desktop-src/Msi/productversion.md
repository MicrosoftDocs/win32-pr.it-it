---
description: Il valore della proprietà ProductVersion è la versione del prodotto in formato stringa.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Proprietà ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330381"
---
# <a name="productversion-property"></a><span data-ttu-id="8dbc1-103">Proprietà ProductVersion</span><span class="sxs-lookup"><span data-stu-id="8dbc1-103">ProductVersion property</span></span>

<span data-ttu-id="8dbc1-104">Il valore della proprietà **ProductVersion** è la versione del prodotto in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-104">The value of the **ProductVersion** property is the version of the product in string format.</span></span> <span data-ttu-id="8dbc1-105">Questa proprietà è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-105">This property is REQUIRED.</span></span>

<span data-ttu-id="8dbc1-106">Il formato della stringa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="8dbc1-106">The format of the string is as follows:</span></span>

<dl> <span data-ttu-id="8dbc1-107">principale.secondario.build</span><span class="sxs-lookup"><span data-stu-id="8dbc1-107">major.minor.build</span></span>  
</dl>

<span data-ttu-id="8dbc1-108">Il primo campo è la versione principale e ha un valore massimo di 255.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-108">The first field is the major version and has a maximum value of 255.</span></span> <span data-ttu-id="8dbc1-109">Il secondo campo è la versione secondaria e ha un valore massimo di 255.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-109">The second field is the minor version and has a maximum value of 255.</span></span> <span data-ttu-id="8dbc1-110">Il terzo campo è denominato versione build o versione di aggiornamento e ha un valore massimo di 65.535.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-110">The third field is called the build version or the update version and has a maximum value of 65,535.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dbc1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8dbc1-111">Remarks</span></span>

<span data-ttu-id="8dbc1-112">Almeno uno dei tre campi di **ProductVersion** deve cambiare per un aggiornamento mediante la tabella di [aggiornamento](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="8dbc1-112">At least one of the three fields of **ProductVersion** must change for an upgrade using the [Upgrade table](upgrade-table.md).</span></span> <span data-ttu-id="8dbc1-113">Qualsiasi aggiornamento che modifica solo il codice del pacchetto, ma lascia invariato **ProductVersion** e [**ProductCode**](productcode.md) è chiamato un [piccolo aggiornamento](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="8dbc1-113">Any update that changes only the package code, but leaves **ProductVersion** and [**ProductCode**](productcode.md) unchanged is called a [small update](small-updates.md).</span></span> <span data-ttu-id="8dbc1-114">I campi di tre versioni vengono forniti principalmente per praticità.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-114">The three versions fields are provided primarily for convenience.</span></span> <span data-ttu-id="8dbc1-115">Se, ad esempio, si desidera modificare **ProductVersion**, ma non si desidera modificare le versioni principale o secondaria, è possibile modificare la versione di compilazione.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-115">For example, if you want to change **ProductVersion**, but do not want to change either the major or minor versions, you can change the build version.</span></span>

<span data-ttu-id="8dbc1-116">Si noti che Windows Installer utilizza solo i primi tre campi della versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-116">Note that Windows Installer uses only the first three fields of the product version.</span></span> <span data-ttu-id="8dbc1-117">Se si include un quarto campo nella versione del prodotto, il programma di installazione ignorerà il quarto campo.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-117">If you include a fourth field in your product version, the installer ignores the fourth field.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dbc1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8dbc1-118">Requirements</span></span>



| <span data-ttu-id="8dbc1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dbc1-119">Requirement</span></span> | <span data-ttu-id="8dbc1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8dbc1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dbc1-121">Versione</span><span class="sxs-lookup"><span data-stu-id="8dbc1-121">Version</span></span><br/> | <span data-ttu-id="8dbc1-122">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8dbc1-123">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8dbc1-124">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8dbc1-125">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8dbc1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8dbc1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dbc1-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8dbc1-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="8dbc1-128">Applicazione di patch e aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="8dbc1-128">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="8dbc1-129">aggiornamento ridotto</span><span class="sxs-lookup"><span data-stu-id="8dbc1-129">small update</span></span>](small-updates.md)
</dt> </dl>

 

 




