---
description: È possibile utilizzare il Windows Installer per rilevare i componenti o i file mancanti, quindi reinstallare le funzionalità che contengono i componenti mancanti.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Installazione di un componente mancante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310972"
---
# <a name="installing-a-missing-component"></a><span data-ttu-id="98c2a-103">Installazione di un componente mancante</span><span class="sxs-lookup"><span data-stu-id="98c2a-103">Installing a Missing Component</span></span>

<span data-ttu-id="98c2a-104">È possibile utilizzare il Windows Installer per rilevare i componenti o i file mancanti, quindi reinstallare le funzionalità che contengono i componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="98c2a-104">You can use the Windows Installer to detect missing components or files, and then reinstall features that contain the missing components.</span></span> <span data-ttu-id="98c2a-105">Poiché il programma di installazione installa le funzionalità e non i componenti, è necessario innanzitutto risolvere il componente a cui appartiene un file mancante, quindi installare la funzionalità che contiene il componente.</span><span class="sxs-lookup"><span data-stu-id="98c2a-105">Because the Installer installs features and not components, it must first resolve to which component a missing file belongs, and then install the feature that contains the component.</span></span> <span data-ttu-id="98c2a-106">Se più di una funzionalità è collegata al componente, il programma di installazione installa la funzionalità che richiede lo spazio su disco minimo.</span><span class="sxs-lookup"><span data-stu-id="98c2a-106">If more than one feature is linked to the component, the Installer installs the feature that requires the least disk space.</span></span>

<span data-ttu-id="98c2a-107">Se si chiama [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), è possibile verificare che il file di chiave di un componente sia presente.</span><span class="sxs-lookup"><span data-stu-id="98c2a-107">If you call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), you can verify that the key file of a component is present.</span></span> <span data-ttu-id="98c2a-108">Tuttavia, è comunque possibile che altri file appartenenti al componente siano mancanti.</span><span class="sxs-lookup"><span data-stu-id="98c2a-108">However, it is still possible that other files belonging to the component are missing.</span></span> <span data-ttu-id="98c2a-109">In questo scenario, chiamare [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="98c2a-109">In that scenario, call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span> <span data-ttu-id="98c2a-110">Il programma di installazione risolve quindi il componente a cui appartiene il file e installa la funzionalità collegata al componente che richiede lo spazio minimo su disco.</span><span class="sxs-lookup"><span data-stu-id="98c2a-110">The Installer then resolves to which component the file belongs, and installs the feature that is linked to the component that requires the least disk space.</span></span>

<span data-ttu-id="98c2a-111">Se la funzione [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) non riesce in modo imprevisto, è necessario installare tutti i componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="98c2a-111">If the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function unexpectedly fails, you must install any missing components.</span></span>

<span data-ttu-id="98c2a-112">Nella procedura seguente viene illustrato come installare i componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="98c2a-112">The following procedure shows you how to install missing components.</span></span>

<span data-ttu-id="98c2a-113">**Per rilevare e installare un componente mancante**</span><span class="sxs-lookup"><span data-stu-id="98c2a-113">**To detect and install a missing component**</span></span>

1.  <span data-ttu-id="98c2a-114">Chiamare [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) per verificare che il file di chiave di un componente sia presente.</span><span class="sxs-lookup"><span data-stu-id="98c2a-114">Call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to verify that the key file of a component is present.</span></span> <span data-ttu-id="98c2a-115">Tuttavia, anche se il file di chiave del componente è presente, è comunque possibile che altri file appartenenti al componente siano mancanti.</span><span class="sxs-lookup"><span data-stu-id="98c2a-115">However, even if the key file of the component is present, it is still possible that other files belonging to the component are missing.</span></span>
2.  <span data-ttu-id="98c2a-116">Chiamare la funzione [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) se la funzionalità associata al componente è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="98c2a-116">Call the [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) function if the feature associated with the component is unknown.</span></span>
3.  <span data-ttu-id="98c2a-117">Chiamare la funzione [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) o [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) se la funzionalità associata al componente è nota.</span><span class="sxs-lookup"><span data-stu-id="98c2a-117">Call the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) or [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) function if the feature associated with the component is known.</span></span>
4.  <span data-ttu-id="98c2a-118">Chiamare [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) se un'applicazione non è in grado di aprire un file.</span><span class="sxs-lookup"><span data-stu-id="98c2a-118">Call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) if an application is unable to open a file.</span></span>

 

 



