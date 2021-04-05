---
description: Per applicare un aggiornamento principale mediante Windows Installer, il pacchetto di installazione del prodotto originale deve specificare una proprietà UpgradeCode, descritta in preparazione di un'applicazione per aggiornamenti principali futuri, e il pacchetto di aggiornamento deve disporre di una tabella di aggiornamento.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Aggiornamento della tabella di aggiornamento per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131195"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a><span data-ttu-id="d8a26-103">Aggiornamento della tabella di aggiornamento per un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d8a26-103">Updating Upgrade Table for an Upgrade</span></span>

<span data-ttu-id="d8a26-104">Per applicare un aggiornamento principale mediante Windows Installer, il pacchetto di installazione del prodotto originale deve specificare una proprietà [**UpgradeCode**](upgradecode.md) , descritta in [preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md), e il pacchetto di aggiornamento deve disporre di una [tabella di aggiornamento](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="d8a26-104">To apply a major upgrade using Windows Installer, the original product installation package must specify an [**UpgradeCode**](upgradecode.md) Property, described in [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md), and the upgrade package must have an [Upgrade table](upgrade-table.md).</span></span>

<span data-ttu-id="d8a26-105">Per ulteriori informazioni sugli aggiornamenti principali, vedere [aggiornamenti principali](major-upgrades.md) per l'applicazione di [patch e aggiornamenti](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="d8a26-105">For more information about major upgrades, see [Major Upgrades](major-upgrades.md) in [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="d8a26-106">Al pacchetto di installazione di MNP2000.msi è stata assegnata una proprietà [**UpgradeCode**](upgradecode.md) , come descritto nella sezione [specifica delle proprietà](specifying-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d8a26-106">The installation package of MNP2000.msi was assigned an [**UpgradeCode**](upgradecode.md) property, as described in the section [Specifying Properties](specifying-properties.md).</span></span>

<span data-ttu-id="d8a26-107">Windows Installer applica l'aggiornamento se l'utente ha già installato le versioni da 1,0 a 1,4 (incluse) della lingua inglese MNP2000.</span><span class="sxs-lookup"><span data-stu-id="d8a26-107">Windows Installer applies the upgrade if the user has already installed the 1.0 to 1.4 versions (inclusive) of English language MNP2000.</span></span> <span data-ttu-id="d8a26-108">Windows Installer esegue la migrazione di tutte le impostazioni della funzionalità del prodotto originale al prodotto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d8a26-108">Windows Installer migrates all of the original product's feature settings to the upgraded product.</span></span> <span data-ttu-id="d8a26-109">Il programma di installazione rimuove i file appartenenti ai prodotti originali non usati dall'aggiornamento del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d8a26-109">The installer removes the files belonging to the original products not being used by the product's upgrade.</span></span>

<span data-ttu-id="d8a26-110">Se la copia di MNP2001.msi non include una [tabella di aggiornamento](upgrade-table.md), utilizzare Orca o un altro editor di tabella per importare una tabella di aggiornamento vuota nel database da Schema.msi.</span><span class="sxs-lookup"><span data-stu-id="d8a26-110">If your copy of MNP2001.msi does not include an [Upgrade table](upgrade-table.md), use Orca, or another table editor, to import an empty Upgrade table into the database from Schema.msi.</span></span> <span data-ttu-id="d8a26-111">L'SDK fornisce una copia di Schema.msi.</span><span class="sxs-lookup"><span data-stu-id="d8a26-111">The SDK provides a copy of Schema.msi.</span></span> <span data-ttu-id="d8a26-112">Utilizzare l'editor di database per aprire MNP2001.msi e immettere i dati seguenti nella tabella di aggiornamento vuota.</span><span class="sxs-lookup"><span data-stu-id="d8a26-112">Use your database editor to open MNP2001.msi and enter the following data into the empty Upgrade table.</span></span>



| <span data-ttu-id="d8a26-113">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="d8a26-113">UpgradeCode</span></span>                            | <span data-ttu-id="d8a26-114">VersionMin</span><span class="sxs-lookup"><span data-stu-id="d8a26-114">VersionMin</span></span> | <span data-ttu-id="d8a26-115">VersionMax</span><span class="sxs-lookup"><span data-stu-id="d8a26-115">VersionMax</span></span> | <span data-ttu-id="d8a26-116">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="d8a26-116">Language</span></span> | <span data-ttu-id="d8a26-117">Attributi</span><span class="sxs-lookup"><span data-stu-id="d8a26-117">Attributes</span></span> | <span data-ttu-id="d8a26-118">Rimuovi</span><span class="sxs-lookup"><span data-stu-id="d8a26-118">Remove</span></span> | <span data-ttu-id="d8a26-119">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="d8a26-119">ActionProperty</span></span> |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| <span data-ttu-id="d8a26-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="d8a26-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> | <span data-ttu-id="d8a26-121">01.00.0000</span><span class="sxs-lookup"><span data-stu-id="d8a26-121">01.00.0000</span></span> | <span data-ttu-id="d8a26-122">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="d8a26-122">01.40.0000</span></span> | <span data-ttu-id="d8a26-123">1033</span><span class="sxs-lookup"><span data-stu-id="d8a26-123">1033</span></span>     | <span data-ttu-id="d8a26-124">769</span><span class="sxs-lookup"><span data-stu-id="d8a26-124">769</span></span>        |        | <span data-ttu-id="d8a26-125">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="d8a26-125">OLDAPPFOUND</span></span>    |



 

[<span data-ttu-id="d8a26-126">Continua</span><span class="sxs-lookup"><span data-stu-id="d8a26-126">Continue</span></span>](updating-properties-for-an-upgrade.md)

 

 



