---
description: È possibile applicare un aggiornamento importante installando il nuovo pacchetto di installazione per il prodotto aggiornato.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Applicazione degli aggiornamenti principali tramite l'installazione del prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311056"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a><span data-ttu-id="4fa1b-103">Applicazione degli aggiornamenti principali tramite l'installazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="4fa1b-103">Applying Major Upgrades by Installing the Product</span></span>

<span data-ttu-id="4fa1b-104">È possibile applicare un aggiornamento importante installando il nuovo pacchetto di installazione per il prodotto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="4fa1b-104">A major upgrade can be applied by installing the new installation package for the upgraded product.</span></span> <span data-ttu-id="4fa1b-105">Poiché gli aggiornamenti principali ottengono un codice prodotto diverso dal prodotto originale, l'installazione dell'aggiornamento deve essere considerata un'installazione di un nuovo prodotto.</span><span class="sxs-lookup"><span data-stu-id="4fa1b-105">Because major upgrades get a different product code than the original product, installing the upgrade must be treated as an installation of a new product.</span></span> <span data-ttu-id="4fa1b-106">L'aggiornamento può essere semplicemente installato come un altro prodotto.</span><span class="sxs-lookup"><span data-stu-id="4fa1b-106">The upgrade can simply be installed like another product.</span></span> <span data-ttu-id="4fa1b-107">È possibile fare in modo che il nuovo pacchetto di installazione gestisca la rimozione del prodotto precedente includendo la [tabella di aggiornamento](upgrade-table.md) e l'azione [FindRelatedProducts](findrelatedproducts-action.md) e [RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="4fa1b-107">You can have the new installation package handle the removal of the old product by including the [Upgrade table](upgrade-table.md) and the [FindRelatedProducts action](findrelatedproducts-action.md) and [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

<span data-ttu-id="4fa1b-108">**Per propagare un aggiornamento principale agli utenti correnti dalla riga di comando**</span><span class="sxs-lookup"><span data-stu-id="4fa1b-108">**To propagate a major upgrade to current users from the command line**</span></span>

-   <span data-ttu-id="4fa1b-109">Dalla riga di comando, usare: **msiexec/i \[** _percorso del file MSI aggiornato_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="4fa1b-109">From the command line, use: **msiexec /i \[**_path to updated msi file_*_\]_*</span></span>

<span data-ttu-id="4fa1b-110">**Per propagare un aggiornamento principale agli utenti correnti da un programma**</span><span class="sxs-lookup"><span data-stu-id="4fa1b-110">**To propagate a major upgrade to current users from a program**</span></span>

-   <span data-ttu-id="4fa1b-111">Da un programma, chiamare [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) e specificare il percorso del file MSI aggiornato.</span><span class="sxs-lookup"><span data-stu-id="4fa1b-111">From a program, call [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) and specify the path to the updated msi file.</span></span>

 

 



