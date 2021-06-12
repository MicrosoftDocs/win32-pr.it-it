---
description: Informazioni sui Windows Installer concetti che iniziano con la lettera D, ad esempio la funzione di database e la patch differenziale.
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d76378d636c8ae14acdc9cb882c31840e3f1550f
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010934"
---
# <a name="d-windows-installer"></a><span data-ttu-id="55375-103">D (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="55375-103">D (Windows Installer)</span></span>

<span data-ttu-id="55375-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P Q](p-gly.md) [](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="55375-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="55375-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**funzione di database**</span><span class="sxs-lookup"><span data-stu-id="55375-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**database function**</span></span>
</dt> <dd>

<span data-ttu-id="55375-106">Accede al database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="55375-106">Accesses the installer database.</span></span> <span data-ttu-id="55375-107">Queste funzioni vengono fornite principalmente [](i-gly.md) per l'uso da parte degli strumenti di creazione di pacchetti del programma di installazione e non devono essere usate per chiamare i servizi del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="55375-107">These functions are provided primarily for use by [*installer package authoring tools*](i-gly.md) and they are not intended to be used to call installer services.</span></span> <span data-ttu-id="55375-108">Per altre informazioni, vedere [Funzioni di database e](database-functions.md) Informazioni di riferimento sulle funzioni del programma di [installazione](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="55375-108">For more information, see [Database Functions](database-functions.md) and the [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="55375-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**handle di database**</span><span class="sxs-lookup"><span data-stu-id="55375-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**database handle**</span></span>
</dt> <dd>

<span data-ttu-id="55375-110">Obbligatorio per l'uso di un database.</span><span class="sxs-lookup"><span data-stu-id="55375-110">Required for working with a database.</span></span> <span data-ttu-id="55375-111">Per altre informazioni, vedere [Recupero di un handle di database](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="55375-111">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="55375-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**patch differenziale**</span><span class="sxs-lookup"><span data-stu-id="55375-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**delta patch**</span></span>
</dt> <dd>

<span data-ttu-id="55375-113">Una patch differenziale è una patch Windows Installer compressa differenziale creata usando uno strumento, ad esempio Patchwiz.dll, che supporta la compressione differenziale.</span><span class="sxs-lookup"><span data-stu-id="55375-113">A delta patch is a delta-compressed Windows Installer patch created using a tool, such as Patchwiz.dll, that supports delta compression.</span></span> <span data-ttu-id="55375-114">Le patch che usano la compressione differenziale possono ridurre le dimensioni di un aggiornamento fornendo solo le differenze (differenziali) tra i file esistenti in un computer di destinazione e i nuovi file desiderati.</span><span class="sxs-lookup"><span data-stu-id="55375-114">Patches that use delta compression can reduce the size of an update by providing only the differences (deltas) between existing files on a target computer and the desired new files.</span></span> <span data-ttu-id="55375-115">I nuovi file desiderati vengono quindi sintetizzati dai file esistenti e dai delta scaricati.</span><span class="sxs-lookup"><span data-stu-id="55375-115">The desired new files are then synthesized from the existing files and the downloaded deltas.</span></span> <span data-ttu-id="55375-116">Per altre informazioni sulla tecnologia di compressione differenziale, vedere [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).</span><span class="sxs-lookup"><span data-stu-id="55375-116">For more information about delta compression technology, see the [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).</span></span>

</dd> </dl>

 

 



