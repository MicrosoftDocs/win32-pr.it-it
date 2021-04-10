---
title: Altre informazioni di connessione
description: I membri della struttura RASDIALPARAMS possono inoltre specificare le informazioni di connessione seguenti.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963190"
---
# <a name="other-connection-information"></a><span data-ttu-id="cbf92-103">Altre informazioni di connessione</span><span class="sxs-lookup"><span data-stu-id="cbf92-103">Other Connection Information</span></span>

<span data-ttu-id="cbf92-104">I membri della struttura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) possono inoltre specificare le informazioni di connessione seguenti.</span><span class="sxs-lookup"><span data-stu-id="cbf92-104">The members of the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure can also specify the following connection information.</span></span>

-   <span data-ttu-id="cbf92-105">Numero di telefono per l'override del numero nella voce della rubrica telefonica.</span><span class="sxs-lookup"><span data-stu-id="cbf92-105">A phone number to override the number in the phone-book entry.</span></span>
-   <span data-ttu-id="cbf92-106">Numero di telefono di [callback](callback-connections.md) che il server remoto può richiamare per stabilire la connessione.</span><span class="sxs-lookup"><span data-stu-id="cbf92-106">A [callback](callback-connections.md) phone number that the remote server can call back to establish the connection.</span></span>
-   <span data-ttu-id="cbf92-107">Nome del dominio di rete remoto in cui deve essere eseguita l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="cbf92-107">The name of the remote network domain on which the authentication is to occur.</span></span>

<span data-ttu-id="cbf92-108">Per il numero di callback e il dominio, i membri di [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) possono indicare che RAS deve usare le informazioni nella voce della rubrica telefonica oppure può fornire informazioni che sostituiscono i dati della rubrica telefonica.</span><span class="sxs-lookup"><span data-stu-id="cbf92-108">For the callback number and the domain, the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) members can either indicate that RAS should use the information in the phone-book entry, or it can provide information that overrides the phone-book data.</span></span>

<span data-ttu-id="cbf92-109">Un client RAS può utilizzare il parametro *lpRasDialExtensions* della funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per controllare se RAS utilizza un prefisso o un suffisso di numero di telefono specificato in una voce della rubrica telefonica.</span><span class="sxs-lookup"><span data-stu-id="cbf92-109">A RAS client can use the *lpRasDialExtensions* parameter of the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function to control whether RAS uses a phone number prefix or suffix specified in a phone-book entry.</span></span>

 

 