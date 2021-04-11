---
description: Il programma di installazione archivia tutte le informazioni sull'interfaccia utente nelle tabelle del database di installazione.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Visualizzazione in anteprima dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231861"
---
# <a name="previewing-the-user-interface"></a><span data-ttu-id="f22a4-103">Visualizzazione in anteprima dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f22a4-103">Previewing the User Interface</span></span>

<span data-ttu-id="f22a4-104">Il programma di installazione archivia tutte le informazioni sull' [interfaccia utente](user-interface.md) nelle tabelle del database di installazione.</span><span class="sxs-lookup"><span data-stu-id="f22a4-104">The installer stores all information about the [user interface](user-interface.md) in the tables of the installation database.</span></span> <span data-ttu-id="f22a4-105">Per semplificare la progettazione dell'interfaccia utente, il programma di installazione fornisce anche una modalità di anteprima per la visualizzazione di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="f22a4-105">To facilitate the design of the UI the installer also provides a preview mode for viewing this information.</span></span> <span data-ttu-id="f22a4-106">Nella procedura seguente viene descritto come abilitare la modalità di anteprima dell'interfaccia utente e visualizzare l'aspetto corrente delle finestre di dialogo e dei tabelloni.</span><span class="sxs-lookup"><span data-stu-id="f22a4-106">The following procedure describes how to enable the UI preview mode and display the current appearance of dialog boxes and billboards.</span></span>

<span data-ttu-id="f22a4-107">**Per visualizzare l'interfaccia utente in modalità di anteprima**</span><span class="sxs-lookup"><span data-stu-id="f22a4-107">**To view the user interface in the preview mode**</span></span>

1.  <span data-ttu-id="f22a4-108">Abilitare la modalità di anteprima chiamando la funzione [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) .</span><span class="sxs-lookup"><span data-stu-id="f22a4-108">Enable the preview mode by calling the [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) function.</span></span>
2.  <span data-ttu-id="f22a4-109">Visualizzare le finestre di dialogo specifiche chiamando la funzione [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) .</span><span class="sxs-lookup"><span data-stu-id="f22a4-109">Display the particular dialog boxes by calling the [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) function.</span></span>
3.  <span data-ttu-id="f22a4-110">Visualizzare manifesti specifici chiamando la funzione [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) .</span><span class="sxs-lookup"><span data-stu-id="f22a4-110">Display particular billboards by calling the [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) function.</span></span>

 

 



