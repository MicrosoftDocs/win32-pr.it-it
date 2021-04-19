---
description: La proprietà SourceDir è la directory radice che contiene il file CAB di origine o l'albero dei file di origine del pacchetto di installazione. Questo valore viene usato per la risoluzione della directory.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: Proprietà SourceDir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332605"
---
# <a name="sourcedir-property"></a><span data-ttu-id="a7f2c-104">Proprietà SourceDir</span><span class="sxs-lookup"><span data-stu-id="a7f2c-104">SourceDir property</span></span>

<span data-ttu-id="a7f2c-105">La proprietà **SourceDir** è la directory radice che contiene il file CAB di origine o l'albero dei file di origine del pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-105">The **SourceDir** property is the root directory that contains the source cabinet file or the source file tree of the installation package.</span></span> <span data-ttu-id="a7f2c-106">Questo valore viene usato per la risoluzione della directory.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-106">This value is used for directory resolution.</span></span>

## <a name="default-value"></a><span data-ttu-id="a7f2c-107">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="a7f2c-107">Default Value</span></span>

<span data-ttu-id="a7f2c-108">Directory che contiene il pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-108">The directory that contains the installation package.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7f2c-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7f2c-109">Remarks</span></span>

<span data-ttu-id="a7f2c-110">L' [azione ResolveSource](resolvesource-action.md) deve essere chiamata prima di usare la proprietà **SourceDir** in qualsiasi espressione o tentare di recuperare il valore di **SourceDir** con [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span><span class="sxs-lookup"><span data-stu-id="a7f2c-110">The [ResolveSource action](resolvesource-action.md) must be called before using the **SourceDir** property in any expression or attempting to retrieve the value of **SourceDir** with [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="a7f2c-111">L'azione ResolveSource non deve essere eseguita mentre l'origine non è disponibile, ad esempio quando si disinstalla un'applicazione, perché ciò può causare una richiesta non intenzionale per il supporto di origine.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-111">The ResolveSource action should not be run while the source is unavailable, such as when uninstalling an application, because this can cause an unintended prompt for the source media.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f2c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7f2c-112">Requirements</span></span>



| <span data-ttu-id="a7f2c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7f2c-113">Requirement</span></span> | <span data-ttu-id="a7f2c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a7f2c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f2c-115">Versione</span><span class="sxs-lookup"><span data-stu-id="a7f2c-115">Version</span></span><br/> | <span data-ttu-id="a7f2c-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a7f2c-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a7f2c-118">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a7f2c-119">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7f2c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7f2c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f2c-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a7f2c-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




