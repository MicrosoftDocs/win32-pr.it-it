---
description: La classe di dispositivo comm/DataModel/PortName è costituita dai nomi dei dispositivi a cui sono collegati i modem.
ms.assetid: 174519f6-3e73-4f05-9718-9e38680a0fb7
title: comm/DataModel/PortName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f926dc87a093f49d41256b003e47c048caa5ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883565"
---
# <a name="commdatamodemportname"></a><span data-ttu-id="72285-103">comm/DataModel/PortName</span><span class="sxs-lookup"><span data-stu-id="72285-103">comm/datamodem/portname</span></span>

<span data-ttu-id="72285-104">La classe di dispositivo comm/DataModel/PortName è costituita dai nomi dei dispositivi a cui sono collegati i modem.</span><span class="sxs-lookup"><span data-stu-id="72285-104">The comm/datamodem/portname device class consists of the device names to which modems are attached.</span></span> <span data-ttu-id="72285-105">Quando il nome del dispositivo viene specificato in una chiamata alla funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) , la funzione compila la struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) con una stringa ANSI (not Unicode) con terminazione null che specifica il nome della porta a cui è collegato il modem specificato, ad esempio "COM1 \\ 0".</span><span class="sxs-lookup"><span data-stu-id="72285-105">When this device name is specified in a call to the [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function, the function fills the [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure with a null-terminated ANSI (not Unicode) string specifying the name of the port to which the specified modem is attached, such as "COM1\\0".</span></span> <span data-ttu-id="72285-106">Questa operazione è destinata principalmente ai fini dell'identificazione nell'interfaccia utente, ma può essere usata in alcune circostanze per aprire direttamente il dispositivo, ignorando il provider di servizi (se il provider di servizi non dispone già del dispositivo aperto).</span><span class="sxs-lookup"><span data-stu-id="72285-106">This is intended primarily for identification purposes in the user interface, but could be used under some circumstances to open the device directly, bypassing the service provider (if the service provider does not already have the device open itself).</span></span> <span data-ttu-id="72285-107">Se al dispositivo non è associata alcuna porta, \\ nella struttura **VARSTRING** viene restituita una stringa null ("0") (con una lunghezza di stringa pari a 1).</span><span class="sxs-lookup"><span data-stu-id="72285-107">If there is no port associated with the device, a null string ("\\0") is returned in the **VARSTRING** structure (with a string length of 1).</span></span>

 

 



