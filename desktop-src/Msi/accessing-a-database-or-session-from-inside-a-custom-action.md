---
description: Non è possibile accedere a una sessione del programma di installazione da un'azione personalizzata che non è la sessione di installazione corrente.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Accesso a un database o a una sessione dall'interno di un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967309"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a><span data-ttu-id="cdf4e-103">Accesso a un database o a una sessione dall'interno di un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="cdf4e-103">Accessing a Database or Session from Inside a Custom Action</span></span>

<span data-ttu-id="cdf4e-104">Non è possibile accedere a una sessione del programma di installazione da un'azione personalizzata che non è la sessione di installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="cdf4e-104">You cannot access an installer session from a custom action that is not the current installation session.</span></span> <span data-ttu-id="cdf4e-105">Le azioni personalizzate sono limitate all'utilizzo solo del database attivo della sessione e di nessun altro database.</span><span class="sxs-lookup"><span data-stu-id="cdf4e-105">Custom actions are limited to working with only the active database of the session and no other databases.</span></span> <span data-ttu-id="cdf4e-106">Le funzioni di [database](database-functions.md) Windows Installer seguenti non devono essere chiamate da un'azione personalizzata, perché richiedono un handle per un database che non è il database della sessione di installazione corrente:</span><span class="sxs-lookup"><span data-stu-id="cdf4e-106">The following Windows Installer [Database Functions](database-functions.md) must not be called from a custom action, because they require a handle to a database that is not the database of the current installation session:</span></span>

[<span data-ttu-id="cdf4e-107">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="cdf4e-107">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[<span data-ttu-id="cdf4e-108">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="cdf4e-108">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[<span data-ttu-id="cdf4e-109">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="cdf4e-109">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[<span data-ttu-id="cdf4e-110">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="cdf4e-110">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[<span data-ttu-id="cdf4e-111">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="cdf4e-111">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[<span data-ttu-id="cdf4e-112">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="cdf4e-112">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[<span data-ttu-id="cdf4e-113">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="cdf4e-113">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[<span data-ttu-id="cdf4e-114">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="cdf4e-114">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[<span data-ttu-id="cdf4e-115">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="cdf4e-115">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a><span data-ttu-id="cdf4e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cdf4e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdf4e-117">Accesso alla sessione corrente del programma di installazione dall'interno di un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="cdf4e-117">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



