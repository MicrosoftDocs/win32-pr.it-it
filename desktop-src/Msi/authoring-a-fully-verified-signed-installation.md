---
description: Usare queste linee guida per coprire un'intera Windows Installer installazione mediante una firma digitale.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Creazione di un'installazione firmata completamente verificata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e76bbfb77eab8b020cb1591847d2a36d09c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311048"
---
# <a name="authoring-a-fully-verified-signed-installation"></a><span data-ttu-id="4d689-103">Creazione di un'installazione firmata completamente verificata</span><span class="sxs-lookup"><span data-stu-id="4d689-103">Authoring a Fully Verified Signed Installation</span></span>

<span data-ttu-id="4d689-104">È possibile usare queste linee guida per coprire un'intera Windows Installer installazione mediante una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="4d689-104">You can use these guidelines to cover an entire Windows Installer installation by a digital signature.</span></span>

<span data-ttu-id="4d689-105">Gli autori di Windows Installer installazioni devono rispettare quanto segue per garantire che tutte le parti dell'installazione siano coperte da una firma digitale:</span><span class="sxs-lookup"><span data-stu-id="4d689-105">Authors of Windows Installer installations must adhere to the following to ensure that all parts of the installation are covered by a digital signature:</span></span>

-   <span data-ttu-id="4d689-106">Utilizzare file CAB interni oppure utilizzare file CAB esterni firmati e creare correttamente la [tabella MsiDigitalSignature](msidigitalsignature-table.md) e la [tabella MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="4d689-106">Use internal cabinet files, or use signed external cabinet files and correctly author the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>
-   <span data-ttu-id="4d689-107">Utilizzare solo le azioni personalizzate archiviate nel pacchetto o installate con il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4d689-107">Use only custom actions stored within the package or installed with the package.</span></span>
-   <span data-ttu-id="4d689-108">Firmare il pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="4d689-108">Sign the installation package.</span></span>
-   <span data-ttu-id="4d689-109">Includere una [tabella MsiPatchCertificate](msipatchcertificate-table.md) nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4d689-109">Include an [MsiPatchCertificate table](msipatchcertificate-table.md) in the package.</span></span> <span data-ttu-id="4d689-110">Per abilitare l'applicazione di patch per il [controllo dell'account utente (UAC)](user-account-control--uac--patching.md), questa tabella deve contenere le informazioni utilizzate per identificare i certificati del firmatario utilizzati per la firma digitale delle patch.</span><span class="sxs-lookup"><span data-stu-id="4d689-110">To enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md), this table must contain information used to identify the signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="4d689-111">L'applicazione di patch del controllo dell'account utente consente all'autore del pacchetto di installazione di identificare patch firmate digitalmente che possono essere applicate in futuro da utenti non amministratori.</span><span class="sxs-lookup"><span data-stu-id="4d689-111">UAC patching enables the author of the installation package to identify digitally-signed patches that can be applied in the future by non-administrator users.</span></span>

<span data-ttu-id="4d689-112">Per un esempio che illustra come creare un'installazione firmata usando l'automazione, vedere [creazione di un'installazione firmata completamente verificata usando l'automazione](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="4d689-112">For an example showing how to author a signed installation using automation, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

 

 



