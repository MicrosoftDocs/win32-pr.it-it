---
description: Quando il Windows Installer elabora lo script di installazione per l'installazione di un prodotto o di un'applicazione, genera contemporaneamente uno script di rollback e salva una copia di ogni file eliminato durante l'installazione.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Rollback dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130666"
---
# <a name="rollback-installation"></a><span data-ttu-id="d5d18-103">Rollback dell'installazione</span><span class="sxs-lookup"><span data-stu-id="d5d18-103">Rollback Installation</span></span>

<span data-ttu-id="d5d18-104">Quando il Windows Installer elabora lo script di installazione per l'installazione di un prodotto o di un'applicazione, genera contemporaneamente uno script di rollback e salva una copia di ogni file eliminato durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="d5d18-104">When the Windows Installer processes the installation script for the installation of a product or application, it simultaneously generates a rollback script and saves a copy of every file deleted during the installation.</span></span> <span data-ttu-id="d5d18-105">Questi file vengono conservati in una directory di sistema nascosta e vengono eliminati automaticamente al termine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="d5d18-105">These files are kept in a hidden system directory and are automatically deleted once the installation is successfully completed.</span></span> <span data-ttu-id="d5d18-106">Se tuttavia l'installazione ha esito negativo, il programma di installazione esegue automaticamente un'installazione di rollback che restituisce lo stato originale del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5d18-106">If however the installation is unsuccessful, the installer automatically performs a rollback installation that returns the system to its original state.</span></span>

<span data-ttu-id="d5d18-107">Il rollback automatico di un'installazione non riuscita è il comportamento predefinito del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="d5d18-107">Automatic rollback of an unsuccessful installation is the default behavior of the installer.</span></span> <span data-ttu-id="d5d18-108">Per disabilitare il rollback durante un'installazione, usare uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="d5d18-108">To disable rollback during an installation use one of the following:</span></span>

-   [<span data-ttu-id="d5d18-109">**Proprietà DISABLEROLLBACK**</span><span class="sxs-lookup"><span data-stu-id="d5d18-109">**DISABLEROLLBACK Property**</span></span>](-disablerollback.md)
-   [<span data-ttu-id="d5d18-110">**Proprietà PROMPTROLLBACKCOST**</span><span class="sxs-lookup"><span data-stu-id="d5d18-110">**PROMPTROLLBACKCOST Property**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="d5d18-111">Azione DisableRollback</span><span class="sxs-lookup"><span data-stu-id="d5d18-111">DisableRollback Action</span></span>](disablerollback-action.md)
-   [<span data-ttu-id="d5d18-112">DisableRollback</span><span class="sxs-lookup"><span data-stu-id="d5d18-112">DisableRollback</span></span>](disablerollback.md)
-   [<span data-ttu-id="d5d18-113">ControlEvent EnableRollback</span><span class="sxs-lookup"><span data-stu-id="d5d18-113">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

<span data-ttu-id="d5d18-114">Ogni volta che il rollback è disabilitato, il programma di installazione imposta la proprietà [**RollbackDisabled**](rollbackdisabled.md) .</span><span class="sxs-lookup"><span data-stu-id="d5d18-114">Whenever rollback is disabled, the installer sets the [**RollbackDisabled**](rollbackdisabled.md) property.</span></span>

<span data-ttu-id="d5d18-115">Se un'installazione utilizza [azioni personalizzate](custom-actions.md), per utilizzare la funzionalità di rollback è necessaria la creazione aggiuntiva del pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="d5d18-115">If an installation uses [custom actions](custom-actions.md), additional authoring of the installation package is required to use rollback functionality.</span></span> <span data-ttu-id="d5d18-116">Per altre informazioni, vedere [rollback delle azioni personalizzate](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d5d18-116">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



