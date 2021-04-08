---
description: Un'azione personalizzata in una tabella di sequenza dell'interfaccia utente o un file eseguibile esterno può richiedere il livello di interfaccia utente corrente dell'installazione.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Determinazione del livello dell'interfaccia utente da un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586cd03bfda2b22e721c0ae9c3393d4bbc525a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967812"
---
# <a name="determining-ui-level-from-a-custom-action"></a><span data-ttu-id="7ba9e-103">Determinazione del livello dell'interfaccia utente da un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="7ba9e-103">Determining UI Level from a Custom Action</span></span>

<span data-ttu-id="7ba9e-104">Un'azione personalizzata in una tabella di sequenza dell'interfaccia utente o un file eseguibile esterno può richiedere il livello di interfaccia utente corrente dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="7ba9e-104">A custom action in a UI sequence table or an external executable file may need the current user interface level of the installation.</span></span> <span data-ttu-id="7ba9e-105">Ad esempio, un'azione personalizzata che dispone di una finestra di dialogo dovrebbe visualizzare la finestra di dialogo solo quando il livello dell'interfaccia utente è un'interfaccia utente completa o un'interfaccia utente ridotta, non dovrebbe visualizzare la finestra di dialogo se il livello dell'interfaccia utente è interfaccia utente di base o nessuno.</span><span class="sxs-lookup"><span data-stu-id="7ba9e-105">For example, a custom action that has a dialog box should only display the dialog when the user interface level is Full UI or Reduced UI, it should not display the dialog if the user interface level is Basic UI or None.</span></span> <span data-ttu-id="7ba9e-106">È necessario utilizzare la proprietà [**UILevel**](uilevel.md) per determinare il livello di interfaccia utente corrente.</span><span class="sxs-lookup"><span data-stu-id="7ba9e-106">You should use the [**UILevel**](uilevel.md) property to determine the current user interface level.</span></span> <span data-ttu-id="7ba9e-107">Non è possibile chiamare [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) da un'azione personalizzata e non è possibile modificare la proprietà a livello di interfaccia utente dall'interno di un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="7ba9e-107">You cannot call [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) from a custom action and it is not possible to change the UI level property from within a custom action.</span></span>

<span data-ttu-id="7ba9e-108">È consigliabile che le azioni personalizzate non utilizzino il livello di interfaccia utente come condizione per l'invio di messaggi di errore al programma di installazione, in quanto ciò può interferire con la registrazione e i messaggi esterni.</span><span class="sxs-lookup"><span data-stu-id="7ba9e-108">It is recommended that custom actions not use the UI level as a condition for sending error messages to the installer because this can interfere with logging and external messages.</span></span>

 

 



