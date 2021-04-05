---
title: Informazioni di autenticazione utente
description: Il servizio gestione connessione di accesso remoto nel computer client invia un nome utente e una password al server RAS nel computer remoto.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cb95d0e941c47deb398c03277013e0e0a35f9d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872594"
---
# <a name="user-authentication-information"></a><span data-ttu-id="b0504-103">Informazioni di autenticazione utente</span><span class="sxs-lookup"><span data-stu-id="b0504-103">User Authentication Information</span></span>

<span data-ttu-id="b0504-104">Il servizio gestione connessione di accesso remoto nel computer client invia un nome utente e una password al server RAS nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="b0504-104">The Remote Access Connection Manager service on the client computer sends a user name and password to the RAS server on the remote computer.</span></span> <span data-ttu-id="b0504-105">Prima di stabilire una connessione, il server remoto utilizza queste informazioni per autenticare l'utente.</span><span class="sxs-lookup"><span data-stu-id="b0504-105">Before it establishes a connection, the remote server uses this information to authenticate the user.</span></span> <span data-ttu-id="b0504-106">Per impostazione predefinita, la gestione connessione di accesso remoto invia il nome utente e la password dell'utente attualmente connesso.</span><span class="sxs-lookup"><span data-stu-id="b0504-106">By default, the Remote Access Connection Manager sends the user name and password of the currently logged-on user.</span></span> <span data-ttu-id="b0504-107">Il client RAS può utilizzare la struttura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) specificata nella chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per specificare un nome utente e una password diversi.</span><span class="sxs-lookup"><span data-stu-id="b0504-107">The RAS client can use the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure specified in the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call to specify a different user name and password.</span></span>

<span data-ttu-id="b0504-108">Se il server remoto non è in grado di autenticare l'utente con le informazioni specificate, può consentire all'operazione di connessione di entrare in uno [stato di sospensione](paused-states.md) per consentire al client RAS di raccogliere dati di autenticazione diversi dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b0504-108">If the remote server cannot authenticate the user with the specified information, it can allow the connection operation to enter a [paused state](paused-states.md) to enable the RAS client to collect different authentication data from the user.</span></span>

 

 