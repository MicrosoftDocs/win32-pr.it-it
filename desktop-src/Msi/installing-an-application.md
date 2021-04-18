---
description: È possibile installare interi prodotti con funzioni Windows Installer. Nei passaggi seguenti viene descritto come installare un prodotto.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Installazione di un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317129"
---
# <a name="installing-an-application"></a><span data-ttu-id="09bc1-104">Installazione di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="09bc1-104">Installing an Application</span></span>

<span data-ttu-id="09bc1-105">È possibile installare interi prodotti con funzioni Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="09bc1-105">You can install entire products with Windows Installer functions.</span></span> <span data-ttu-id="09bc1-106">Nei passaggi seguenti viene descritto come installare un prodotto.</span><span class="sxs-lookup"><span data-stu-id="09bc1-106">The following steps describe how to install a product.</span></span>

<span data-ttu-id="09bc1-107">**Per installare un prodotto**</span><span class="sxs-lookup"><span data-stu-id="09bc1-107">**To install a product**</span></span>

1.  <span data-ttu-id="09bc1-108">Eseguire un prodotto tramite la sequenza di installazione o disinstallazione chiamando la funzione [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) .</span><span class="sxs-lookup"><span data-stu-id="09bc1-108">Run a product through its installation or uninstallation sequence by calling the [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) function.</span></span>
2.  <span data-ttu-id="09bc1-109">Specificare il livello di installazione chiamando la funzione [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .</span><span class="sxs-lookup"><span data-stu-id="09bc1-109">Specify the installation level by calling the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function.</span></span>

    <span data-ttu-id="09bc1-110">Per impostare lo stato di installazione, è possibile usare i parametri della funzione [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .</span><span class="sxs-lookup"><span data-stu-id="09bc1-110">You can use the parameters of the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function to set the installation state.</span></span> <span data-ttu-id="09bc1-111">Ad esempio, è possibile impostare lo stato su Installa localmente o per eseguire l'installazione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="09bc1-111">For example, you can set the state to install locally or to install from the source.</span></span> <span data-ttu-id="09bc1-112">È possibile impostare l'intervallo di funzionalità del prodotto da includere impostando il livello.</span><span class="sxs-lookup"><span data-stu-id="09bc1-112">You can set the range of product features to be included by setting the level.</span></span>

<span data-ttu-id="09bc1-113">Per ulteriori informazioni sull'installazione di un'applicazione, vedere la pagina relativa al meccanismo di [resilienza](resiliency.md) e [installazione](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="09bc1-113">For more information about installing an application, see [Resiliency](resiliency.md) and [Installation Mechanism](installation-mechanism.md).</span></span>

 

 



