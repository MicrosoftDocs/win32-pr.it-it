---
title: Linee guida hardware periferiche
description: Se il dispositivo hardware non è progettato per funzionare in una sessione remota, i fornitori devono garantire che il software dei driver di dispositivo forzi la disabilitazione del reindirizzamento del dispositivo usando criteri di sistema o criteri di gruppo.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396463"
---
# <a name="peripheral-hardware-guidelines"></a><span data-ttu-id="0fd3e-103">Linee guida hardware periferiche</span><span class="sxs-lookup"><span data-stu-id="0fd3e-103">Peripheral hardware guidelines</span></span>

<span data-ttu-id="0fd3e-104">Per un client Connessione Desktop remoto (RDC), il server di host sessione Desktop remoto (host sessione Desktop remoto) è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-104">To a Remote Desktop Connection (RDC) client, the Remote Desktop Session Host (RD Session Host) server is the local computer.</span></span> <span data-ttu-id="0fd3e-105">Di conseguenza, i dispositivi come le unità disco e le stampanti collegate al server vengono visualizzati come dispositivi locali per un client.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-105">Consequently, devices such as disk drives and printers attached to the server appear as local devices to a client.</span></span> <span data-ttu-id="0fd3e-106">Al contrario, le unità e le stampanti collegate a un terminale client possono sembrare dispositivi remoti, a seconda delle opzioni selezionate per la connessione, del server utilizzato e della versione del software client utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-106">In contrast, drives and printers attached to a client terminal can appear to be remote devices, depending on the options selected for the connection, the server used, and the version of the client software used.</span></span>

<span data-ttu-id="0fd3e-107">Sebbene la versione iniziale di Servizi Desktop remoto non supportasse le applicazioni che inviano l'output direttamente alle porte seriali, parallele e audio collegate al terminale client, le versioni correnti consentono a tali dispositivi di apparire come dispositivi locali per le applicazioni in esecuzione nella sessione di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-107">While the initial release of Remote Desktop Services did not support applications that send output directly to serial, parallel, and sound ports attached to the client terminal, the current versions do allow these devices to appear as local devices to applications running in the Remote Desktop Services session.</span></span>

<span data-ttu-id="0fd3e-108">Se il dispositivo hardware non è progettato per funzionare in una sessione remota, i fornitori devono garantire che il software dei driver di dispositivo forzi la disabilitazione del reindirizzamento del dispositivo usando criteri di sistema o criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-108">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

 

 




