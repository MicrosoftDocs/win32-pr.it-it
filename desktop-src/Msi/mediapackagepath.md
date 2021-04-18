---
description: "Se il pacchetto di installazione distribuito con un'applicazione non è alla radice del CD-ROM che i clienti ricevono, è necessario impostare la proprietà MEDIAPACKAGEPATH nella riga di comando sul percorso relativo dell'applicazione sul CD-ROM. Se, ad esempio, il percorso del pacchetto nel supporto è E: \\\\ percorso \\\\My.msi, utilizzare MEDIAPACKAGEPATH =&\\# 0034; \\\\ Percorso \\\\ & \\# 0034;. Gli amministratori possono creare CD-ROMs da un punto di installazione amministrativa. Se il percorso della radice dell'installazione viene modificato nei nuovi CD-ROM, la proprietà MEDIAPACKAGEPATH deve essere impostata sul nuovo percorso da installare da questo supporto. Un'origine con un percorso su CD-ROM diverso da quello specificato nel pacchetto è inutilizzabile. Tuttavia, non è necessario utilizzare questa proprietà quando si crea un punto di installazione amministrativa da supporti di spedizione."
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Proprietà MEDIAPACKAGEPATH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329618"
---
# <a name="mediapackagepath-property"></a><span data-ttu-id="3d263-106">Proprietà MEDIAPACKAGEPATH</span><span class="sxs-lookup"><span data-stu-id="3d263-106">MEDIAPACKAGEPATH property</span></span>

<span data-ttu-id="3d263-107">Se il pacchetto di installazione distribuito con un'applicazione non è alla radice del CD-ROM che i clienti ricevono, è necessario impostare la proprietà **MEDIAPACKAGEPATH** nella riga di comando sul percorso relativo dell'applicazione sul CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3d263-107">If the installation package shipping with an application is not at the root of the CD-ROM that customers receive, the **MEDIAPACKAGEPATH** property must be set on the command line to the relative path of the application on the CD-ROM.</span></span>

<span data-ttu-id="3d263-108">Se, ad esempio, il percorso del pacchetto nel supporto è E: \\ percorso \\My.msi, utilizzare MEDIAPACKAGEPATH = " \\ percorso \\ ".</span><span class="sxs-lookup"><span data-stu-id="3d263-108">For example, if the path to the package on the media is E:\\MyPath\\My.msi, then use MEDIAPACKAGEPATH="\\MyPath\\".</span></span>

<span data-ttu-id="3d263-109">Gli amministratori possono creare CD-ROMs da un punto di installazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="3d263-109">Administrators may create CD-ROMs from an administrative installation point.</span></span> <span data-ttu-id="3d263-110">Se il percorso della radice dell'installazione viene modificato nei nuovi CD-ROM, la proprietà **MEDIAPACKAGEPATH** deve essere impostata sul nuovo percorso da installare da questo supporto.</span><span class="sxs-lookup"><span data-stu-id="3d263-110">If the location of the root of the installation is changed on the new CD-ROMs, the **MEDIAPACKAGEPATH** property must be set to the new path to install from this media.</span></span> <span data-ttu-id="3d263-111">Un'origine con un percorso su CD-ROM diverso da quello specificato nel pacchetto è inutilizzabile.</span><span class="sxs-lookup"><span data-stu-id="3d263-111">A source with a location on the CD-ROM different than what is specified in the package is unusable.</span></span> <span data-ttu-id="3d263-112">Tuttavia, non è necessario utilizzare questa proprietà quando si crea un punto di installazione amministrativa da supporti di spedizione.</span><span class="sxs-lookup"><span data-stu-id="3d263-112">It is not necessary, however, to use this property when creating an administrative installation point from shipping media.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d263-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d263-113">Requirements</span></span>



| <span data-ttu-id="3d263-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d263-114">Requirement</span></span> | <span data-ttu-id="3d263-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3d263-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d263-116">Versione</span><span class="sxs-lookup"><span data-stu-id="3d263-116">Version</span></span><br/> | <span data-ttu-id="3d263-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3d263-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3d263-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3d263-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3d263-119">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3d263-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3d263-120">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3d263-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d263-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d263-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d263-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3d263-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




