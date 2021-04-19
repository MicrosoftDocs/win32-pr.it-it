---
description: Gli autori di pacchetti possono monitorare i messaggi di Windows Installer interni tramite la creazione di un'applicazione eseguibile che contiene un gestore di callback per ricevere i messaggi e le funzionalità per avviare un'installazione.
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: Monitoraggio di un'installazione mediante MsiSetExternalUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06cc461845a6db1fab4ede22581093c46c0e76e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317754"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a><span data-ttu-id="2935d-103">Monitoraggio di un'installazione mediante MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="2935d-103">Monitoring an Installation Using MsiSetExternalUI</span></span>

<span data-ttu-id="2935d-104">Gli autori di pacchetti possono monitorare i messaggi di Windows Installer interni tramite la creazione di un'applicazione eseguibile che contiene un gestore di callback per ricevere i messaggi e le funzionalità per avviare un'installazione.</span><span class="sxs-lookup"><span data-stu-id="2935d-104">Package authors can monitor internal Windows Installer messages through the creation of an executable application that contains both a callback handler to receive the messages and functionality to initiate an installation.</span></span>

<span data-ttu-id="2935d-105">Il gestore di callback è conforme al \_ prototipo del gestore INSTALLUI e un puntatore a questo gestore di callback viene passato a [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia).</span><span class="sxs-lookup"><span data-stu-id="2935d-105">The callback handler conforms to the INSTALLUI\_HANDLER prototype, and a pointer to this callback handler is passed to [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia).</span></span> <span data-ttu-id="2935d-106">Una volta che l'installazione è stata avviata da una chiamata a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), i messaggi di installazione vengono intercettati dal gestore di callback e l'autore del pacchetto può visualizzare o ignorare in modo selettivo uno o tutti i messaggi.</span><span class="sxs-lookup"><span data-stu-id="2935d-106">Once the installation has been initiated by a call to [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), installation messages are trapped by the callback handler and the package author can selectively display or ignore any or all of these messages.</span></span>

<span data-ttu-id="2935d-107">Per altre informazioni, vedere [gestione dei messaggi di stato usando MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [restituzione di valori da un gestore di interfaccia utente esterno](returning-values-from-an-external-user-interface-handler.md)e [analisi dei messaggi Windows Installer](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="2935d-107">For more information, see [Handling Progress Messages Using MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [Returning Values from an External User Interface Handler](returning-values-from-an-external-user-interface-handler.md), and [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="2935d-108">Per ulteriori informazioni sull'utilizzo di un gestore esterno basato su record, vedere [monitoraggio di un'installazione mediante MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).</span><span class="sxs-lookup"><span data-stu-id="2935d-108">For more information about using a record-based external handler, see [Monitoring an Installation Using MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).</span></span>

 

 



