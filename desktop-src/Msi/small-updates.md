---
description: Un piccolo aggiornamento apporta modifiche a uno o più file di applicazione troppo piccoli per garantire la modifica del codice del prodotto.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Aggiornamenti di piccole dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128371"
---
# <a name="small-updates"></a><span data-ttu-id="170b3-103">Aggiornamenti di piccole dimensioni</span><span class="sxs-lookup"><span data-stu-id="170b3-103">Small Updates</span></span>

<span data-ttu-id="170b3-104">Un piccolo aggiornamento apporta modifiche a uno o più file di applicazione troppo piccoli per garantire la modifica del codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="170b3-104">A small update makes changes to one or more application files that are too minor to warrant changing the product code.</span></span> <span data-ttu-id="170b3-105">Un aggiornamento di piccole dimensioni è noto anche come aggiornamento QFE (Quick Fix Engineering).</span><span class="sxs-lookup"><span data-stu-id="170b3-105">A small update is also commonly referred to as a quick fix engineering (QFE) update.</span></span> <span data-ttu-id="170b3-106">Un piccolo aggiornamento non consente la riorganizzazione della struttura ad albero del componente della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="170b3-106">A small update does not permit reorganization of the feature-component tree.</span></span>

<span data-ttu-id="170b3-107">Un piccolo aggiornamento tipico modifica solo uno o due file o una chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="170b3-107">A typical small update changes only one or two files or a registry key.</span></span> <span data-ttu-id="170b3-108">Poiché un aggiornamento di piccole dimensioni modifica le informazioni nel file con estensione msi, è necessario modificare il codice del pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="170b3-108">Because a small update changes the information in the .msi file, the installation package code must be changed.</span></span> <span data-ttu-id="170b3-109">Il codice del pacchetto viene archiviato nella proprietà [**Riepilogo numero revisione**](revision-number-summary.md) del [flusso di informazioni di riepilogo](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="170b3-109">The package code is stored in the [**Revision Number Summary**](revision-number-summary.md) property of the [Summary Information Stream](summary-information-stream.md).</span></span>

<span data-ttu-id="170b3-110">Il codice prodotto non viene mai modificato con un piccolo aggiornamento, quindi tutte le modifiche introdotte da un piccolo aggiornamento devono essere coerenti con le linee guida descritte in [modifica del codice del prodotto](changing-the-product-code.md).</span><span class="sxs-lookup"><span data-stu-id="170b3-110">The product code is never changed with a small update, so all of the changes introduced by a small update have to be consistent with the guidelines described in [Changing the Product Code](changing-the-product-code.md).</span></span> <span data-ttu-id="170b3-111">Un aggiornamento richiede un [aggiornamento principale](major-upgrades.md) per modificare il [**ProductCode**](productcode.md).</span><span class="sxs-lookup"><span data-stu-id="170b3-111">An update requires a [major upgrade](major-upgrades.md) to change the [**ProductCode**](productcode.md).</span></span> <span data-ttu-id="170b3-112">Se è necessario distinguere tra i prodotti senza modificare il codice del prodotto, usare un [aggiornamento secondario](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="170b3-112">If it is necessary to differentiate between products without changing the product code, use a [minor upgrade](minor-upgrades.md).</span></span>

<span data-ttu-id="170b3-113">Per informazioni su come applicare un pacchetto di patch di aggiornamento di piccole dimensioni a un pacchetto di Windows Installer, vedere la pagina relativa alla [creazione di una patch di aggiornamento](creating-a-small-update-patch.md)di piccole dimensioni, [applicazione di piccoli aggiornamenti mediante l'applicazione di patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [applicazione di piccoli aggiornamenti con la reinstallazione del prodotto](applying-small-updates-by-reinstalling-the-product.md)e [applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md).</span><span class="sxs-lookup"><span data-stu-id="170b3-113">For information on how to apply a small update patch package to a Windows Installer package, see [Creating a Small Update Patch](creating-a-small-update-patch.md), [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md), and [Applying Small Updates by Patching an Administrative Image](applying-small-updates-by-patching-an-administrative-image.md).</span></span>

 

 



