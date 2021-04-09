---
description: Msimerg.exe è un'utilità della riga di comando che utilizza MsiDatabaseMerge per unire un database di riferimento in un database di base.
ms.assetid: db0c9ae5-a8e8-4eff-ae14-67dcce352483
title: Msimerg.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0555aa7bd762b92ed67d0bac1487159fadb73a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968311"
---
# <a name="msimergexe"></a><span data-ttu-id="cc963-103">Msimerg.exe</span><span class="sxs-lookup"><span data-stu-id="cc963-103">Msimerg.exe</span></span>

<span data-ttu-id="cc963-104">Msimerg.exe è un'utilità della riga di comando che utilizza [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) per [unire](merges-and-transforms.md) un database di riferimento in un database di base.</span><span class="sxs-lookup"><span data-stu-id="cc963-104">Msimerg.exe is a command line utility that uses [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to [merge](merges-and-transforms.md) a reference database into a base database.</span></span>

<span data-ttu-id="cc963-105">Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="cc963-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc963-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc963-106">Syntax</span></span>

<span data-ttu-id="cc963-107">**MSIMerg** *{database di base} {database di riferimento}*</span><span class="sxs-lookup"><span data-stu-id="cc963-107">**Msimerg** *{base database}{reference database}*</span></span>

<span data-ttu-id="cc963-108">Se si verifica un conflitto di merge tra i due database, le informazioni sui conflitti vengono inserite nella \_ tabella MergeErrors.</span><span class="sxs-lookup"><span data-stu-id="cc963-108">If there is a merge conflict between the two databases, the conflict information is placed in the \_MergeErrors table.</span></span>

## <a name="command-line-options"></a><span data-ttu-id="cc963-109">Opzioni da riga di comando</span><span class="sxs-lookup"><span data-stu-id="cc963-109">Command Line Options</span></span>

<span data-ttu-id="cc963-110">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="cc963-110">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc963-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc963-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc963-112">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cc963-112">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="cc963-113">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="cc963-113">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



