---
description: Questa finestra di dialogo modale Visualizza il contratto di licenza con l'utente.
ms.assetid: 367fe264-6e08-4b40-b61b-617bb92986b7
title: Finestra di dialogo LicenseAgreement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8876f315787671ee36de42e5b86167659611a77a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307250"
---
# <a name="licenseagreement-dialog"></a><span data-ttu-id="6c98a-103">Finestra di dialogo LicenseAgreement</span><span class="sxs-lookup"><span data-stu-id="6c98a-103">LicenseAgreement Dialog</span></span>

<span data-ttu-id="6c98a-104">Questa finestra di dialogo modale Visualizza il contratto di licenza con l'utente.</span><span class="sxs-lookup"><span data-stu-id="6c98a-104">This modal dialog box displays the license agreement to the user.</span></span> <span data-ttu-id="6c98a-105">In genere, nella finestra di dialogo viene visualizzato il testo dell'accordo utilizzando un [controllo ScrollableText](scrollabletext-control.md) e una coppia di pulsanti di opzione che consentono all'utente di accettare o rifiutare l'accordo.</span><span class="sxs-lookup"><span data-stu-id="6c98a-105">Typically the dialog box displays the text of the agreement using a [ScrollableText control](scrollabletext-control.md) and a pair of option buttons that let the user accept or reject the agreement.</span></span> <span data-ttu-id="6c98a-106">Per motivi legali è consigliabile che nessuno dei pulsanti venga presentato all'utente come già selezionato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6c98a-106">For legal reasons it is advisable that neither button be presented to the user as already selected by default.</span></span> <span data-ttu-id="6c98a-107">In questo modo l'utente deve effettuare una scelta attiva.</span><span class="sxs-lookup"><span data-stu-id="6c98a-107">This forces the user to make an active choice.</span></span> <span data-ttu-id="6c98a-108">Gli autori usano in genere un [controllo RadioButtonGroup](radiobuttongroup-control.md) a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="6c98a-108">Authors commonly use a [RadioButtonGroup control](radiobuttongroup-control.md) for this purpose.</span></span> <span data-ttu-id="6c98a-109">Si noti tuttavia che lo stato attivo su una finestra di dialogo non viene spostato in un controllo RadioButtonGroup fino a quando non viene selezionato uno dei pulsanti del gruppo.</span><span class="sxs-lookup"><span data-stu-id="6c98a-109">Note however that the focus on a dialog box does not move to a RadioButtonGroup control until one of the buttons in the group has been selected.</span></span>

 

 



