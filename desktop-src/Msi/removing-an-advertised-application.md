---
description: Per rimuovere un'applicazione installata nello stato pubblicizzato, è sufficiente disinstallarla usando MsiInstallProduct o MsiConfigureProduct. È anche possibile rimuovere un'applicazione annunciata dalla riga di comando. Vedere Opzioni della riga di comando.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Rimozione di un'applicazione annunciata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882721"
---
# <a name="removing-an-advertised-application"></a><span data-ttu-id="825b7-105">Rimozione di un'applicazione annunciata</span><span class="sxs-lookup"><span data-stu-id="825b7-105">Removing an Advertised Application</span></span>

<span data-ttu-id="825b7-106">Per rimuovere un'applicazione installata nello stato pubblicizzato, è sufficiente disinstallarla usando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span><span class="sxs-lookup"><span data-stu-id="825b7-106">To remove an application that has been installed in the advertised state, simply uninstall it using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span></span> <span data-ttu-id="825b7-107">È anche possibile rimuovere un'applicazione annunciata dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="825b7-107">You can also remove an advertised application from the command line.</span></span> <span data-ttu-id="825b7-108">Vedere [Opzioni della riga di comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="825b7-108">See [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="825b7-109">Si noti che potrebbe non essere possibile rimuovere un'applicazione annunciata se il pacchetto è stato creato in modo tale che l'esecuzione di un'installazione è condizionale quando l'istruzione **non è installata**.</span><span class="sxs-lookup"><span data-stu-id="825b7-109">Note that you may be unable to remove an advertised application if you have authored the package in such a way that running an installation is conditional upon the statement **NOT Installed**.</span></span> <span data-ttu-id="825b7-110">Un'applicazione annunciata non è installata nel computer dell'utente e il programma di installazione non imposta la proprietà [**installata**](installed.md) .</span><span class="sxs-lookup"><span data-stu-id="825b7-110">An advertised application is not installed on the user's computer and the installer does not set the [**Installed**](installed.md) Property.</span></span> <span data-ttu-id="825b7-111">Il pacchetto deve essere creato in modo che sia possibile disinstallare le applicazioni annunciate.</span><span class="sxs-lookup"><span data-stu-id="825b7-111">The package must be authored so that advertised applications can be uninstalled.</span></span>

 

 



