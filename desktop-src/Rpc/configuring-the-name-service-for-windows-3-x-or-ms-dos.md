---
title: Configurazione del servizio nome per Windows 3. x o MS-DOS
description: RPC (Remote Procedure Call) e configurazione del servizio nome per Windows 3. x o MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044870"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a><span data-ttu-id="c6ede-103">Configurazione del servizio nome per Windows 3. x o MS-DOS</span><span class="sxs-lookup"><span data-stu-id="c6ede-103">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>

<span data-ttu-id="c6ede-104">Quando si esegue Setup.exe per installare la libreria di runtime RPC a 16 bit, viene richiesto di selezionare un provider di servizi dei nomi:</span><span class="sxs-lookup"><span data-stu-id="c6ede-104">When you run Setup.exe to install the 16-bit RPC run-time library, it prompts you to select a name service provider:</span></span>

-   <span data-ttu-id="c6ede-105">Se si sceglie **install default name service provider**, viene installato il valore predefinito NSP, Microsoft Locator.</span><span class="sxs-lookup"><span data-stu-id="c6ede-105">If you choose **Install Default Name Service Provider**, the default NSP, Microsoft Locator, is installed.</span></span>
-   <span data-ttu-id="c6ede-106">Se si sceglie **Installa provider di servizi nome personalizzato**, completare la finestra di dialogo **Definisci indirizzo di rete** per installare il servizio directory di celle DCE come NSP.</span><span class="sxs-lookup"><span data-stu-id="c6ede-106">If you choose **Install Custom Name Service Provider**, complete the **Define Network Address** dialog box to install the DCE Cell Directory Service as your NSP.</span></span> <span data-ttu-id="c6ede-107">Il servizio directory di celle DCE è il NSP usato con i server DCE.</span><span class="sxs-lookup"><span data-stu-id="c6ede-107">The DCE Cell Directory Service is the NSP used with DCE servers.</span></span>

<span data-ttu-id="c6ede-108">L'indirizzo di rete è il nome del computer host che esegue il daemon NSI (NSID).</span><span class="sxs-lookup"><span data-stu-id="c6ede-108">The network address is the name of the host computer that runs the NSI daemon (nsid).</span></span> <span data-ttu-id="c6ede-109">Questo computer funge da gateway per il servizio directory celle DCE, passando le chiamate di funzione NSI tra computer che eseguono sistemi operativi Microsoft e computer DCE.</span><span class="sxs-lookup"><span data-stu-id="c6ede-109">This computer acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="c6ede-110">L'indirizzo di rete non può contenere più di 80 caratteri, ad esempio 11.1.9.169 è un indirizzo valido.</span><span class="sxs-lookup"><span data-stu-id="c6ede-110">The network address can be 80 characters or less—for example, 11.1.9.169 is a valid address.</span></span>

 

 




