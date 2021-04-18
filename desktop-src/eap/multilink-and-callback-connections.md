---
title: Connessioni a collegamento multiplo e callback
description: Per il primo collegamento in una connessione a più collegamenti, il servizio di autenticazione imposta il flag del \_ \_ primo collegamento del flag EAP RAS \_ \_ nel membro fFlags \_ della \_ struttura di input EAP PPP.
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af39ebfa54469e2f44c44c800cebbfb176b33cad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299311"
---
# <a name="multilink-and-callback-connections"></a><span data-ttu-id="ba7de-103">Connessioni a collegamento multiplo e callback</span><span class="sxs-lookup"><span data-stu-id="ba7de-103">Multilink and Callback Connections</span></span>

<span data-ttu-id="ba7de-104">Per il primo collegamento in una connessione a più collegamenti, il servizio di autenticazione imposta il flag del \_ \_ primo collegamento del flag EAP RAS \_ \_ nel membro **fFlags** della struttura di [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) .</span><span class="sxs-lookup"><span data-stu-id="ba7de-104">For the first link in a multilink connection, the authentication service sets the RAS\_EAP\_FLAG\_FIRST\_LINK flag in the **fFlags** member of the [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) structure.</span></span> <span data-ttu-id="ba7de-105">Il protocollo di autenticazione può utilizzare la presenza di questo flag per determinare se presentare un'interfaccia utente specificatamente per il primo collegamento di una connessione a più collegamenti.</span><span class="sxs-lookup"><span data-stu-id="ba7de-105">The authentication protocol can use the presence of this flag to determine whether to present a user interface specifically for the first link of a multilink connection.</span></span>

<span data-ttu-id="ba7de-106">Se la connessione è configurata in modo che il server richiami il computer client, il flag del \_ \_ primo collegamento del flag EAP RAS \_ \_ non verrà impostato nel callback.</span><span class="sxs-lookup"><span data-stu-id="ba7de-106">If the connection is configured so that the server calls back the client computer, the RAS\_EAP\_FLAG\_FIRST\_LINK flag will not be set on the callback.</span></span>

<span data-ttu-id="ba7de-107">Se il protocollo di autenticazione imposta il membro **fSaveConnectionData** dell' [**\_ \_ output EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) su **true**, i collegamenti successivi nella connessione a collegamento multiplo ricevono i nuovi dati specifici della connessione.</span><span class="sxs-lookup"><span data-stu-id="ba7de-107">If the authentication protocol sets the **fSaveConnectionData** member of [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) to **TRUE**, subsequent links in the multilink connection receive the new connection-specific data.</span></span> <span data-ttu-id="ba7de-108">Nel caso di dati specifici dell'utente, tuttavia, il protocollo di autenticazione continua a ottenere i dati originali specifici dell'utente anche se imposta il membro **fSaveUserData** dell' **\_ \_ output EAP PPP** su **true**.</span><span class="sxs-lookup"><span data-stu-id="ba7de-108">In the case of user-specific data, however, the authentication protocol continues to get the original user-specific data even if it sets the **fSaveUserData** member of **PPP\_EAP\_OUTPUT** to **TRUE**.</span></span>

<span data-ttu-id="ba7de-109">Il protocollo di autenticazione può utilizzare un' [interfaccia utente interattiva](interactive-user-interface.md) per raccogliere dati per un particolare collegamento di una connessione a più collegamenti.</span><span class="sxs-lookup"><span data-stu-id="ba7de-109">The authentication protocol may use an [interactive user interface](interactive-user-interface.md) to collect data for a particular link of a multilink connection.</span></span> <span data-ttu-id="ba7de-110">In questo caso, il servizio di autenticazione rende disponibili i dati risultanti per il protocollo di autenticazione durante i collegamenti successivi.</span><span class="sxs-lookup"><span data-stu-id="ba7de-110">In this case, the authentication service makes the resulting data available to the authentication protocol during subsequent links.</span></span> <span data-ttu-id="ba7de-111">Tuttavia, questi dati non vengono mai salvati nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="ba7de-111">However, this data is never saved to persistent storage.</span></span>

 

 




