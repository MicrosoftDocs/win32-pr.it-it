---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e2673f845d85db88d55cbcd53838f7e682dbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752319"
---
# <a name="d-windows-installer"></a><span data-ttu-id="91cfe-103">D (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="91cfe-103">D (Windows Installer)</span></span>

<span data-ttu-id="91cfe-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) d [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="91cfe-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="91cfe-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**funzione di database**</span><span class="sxs-lookup"><span data-stu-id="91cfe-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**database function**</span></span>
</dt> <dd>

<span data-ttu-id="91cfe-106">Accede al database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="91cfe-106">Accesses the installer database.</span></span> <span data-ttu-id="91cfe-107">Queste funzioni vengono fornite principalmente dagli strumenti di [*creazione dei pacchetti del programma di installazione*](i-gly.md) e non sono progettate per essere usate per chiamare i servizi del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="91cfe-107">These functions are provided primarily for use by [*installer package authoring tools*](i-gly.md) and they are not intended to be used to call installer services.</span></span> <span data-ttu-id="91cfe-108">Per ulteriori informazioni, vedere [funzioni di database](database-functions.md) e [riferimento](installer-function-reference.md)alle funzioni del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="91cfe-108">For more information, see [Database Functions](database-functions.md) and the [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cfe-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**handle di database**</span><span class="sxs-lookup"><span data-stu-id="91cfe-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**database handle**</span></span>
</dt> <dd>

<span data-ttu-id="91cfe-110">Obbligatorio per l'utilizzo di un database.</span><span class="sxs-lookup"><span data-stu-id="91cfe-110">Required for working with a database.</span></span> <span data-ttu-id="91cfe-111">Per ulteriori informazioni, vedere [ottenere un handle di database](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="91cfe-111">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cfe-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**patch Delta**</span><span class="sxs-lookup"><span data-stu-id="91cfe-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**delta patch**</span></span>
</dt> <dd>

<span data-ttu-id="91cfe-113">Una patch Delta è una patch Windows Installer compressa Delta creata usando uno strumento, ad esempio Patchwiz.dll, che supporta la compressione delta.</span><span class="sxs-lookup"><span data-stu-id="91cfe-113">A delta patch is a delta-compressed Windows Installer patch created using a tool, such as Patchwiz.dll, that supports delta compression.</span></span> <span data-ttu-id="91cfe-114">Le patch che usano la compressione delta possono ridurre le dimensioni di un aggiornamento fornendo solo le differenze (Delta) tra i file esistenti in un computer di destinazione e i nuovi file desiderati.</span><span class="sxs-lookup"><span data-stu-id="91cfe-114">Patches that use delta compression can reduce the size of an update by providing only the differences (deltas) between existing files on a target computer and the desired new files.</span></span> <span data-ttu-id="91cfe-115">I nuovi file desiderati vengono quindi sintetizzati dai file esistenti e dai Delta scaricati.</span><span class="sxs-lookup"><span data-stu-id="91cfe-115">The desired new files are then synthesized from the existing files and the downloaded deltas.</span></span> <span data-ttu-id="91cfe-116">Per ulteriori informazioni sulla tecnologia di compressione Delta, vedere l' [interfaccia di programmazione dell'applicazione di compressione delta](https://msdn.microsoft.com/library/ms811406.aspx).</span><span class="sxs-lookup"><span data-stu-id="91cfe-116">For more information about delta compression technology, see the [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).</span></span>

</dd> </dl>

 

 



