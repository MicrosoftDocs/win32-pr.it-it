---
title: Linee guida per la scrittura di DLL EAP
description: È possibile scrivere dll EAP o plug-in per ottimizzare le prestazioni in scenari diversi.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2d437df61811e6fb24b3a9b4ff406ced4905
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299293"
---
# <a name="guidelines-for-writing-eap-dlls"></a><span data-ttu-id="945ef-103">Linee guida per la scrittura di DLL EAP</span><span class="sxs-lookup"><span data-stu-id="945ef-103">Guidelines for Writing EAP DLLs</span></span>

<span data-ttu-id="945ef-104">È possibile scrivere dll EAP o plug-in per ottimizzare le prestazioni in scenari diversi.</span><span class="sxs-lookup"><span data-stu-id="945ef-104">EAP DLLs or Plug-ins can be written to optimize their performance in different scenarios.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="945ef-105">Linee guida generali</span><span class="sxs-lookup"><span data-stu-id="945ef-105">General Guidelines</span></span>

-   <span data-ttu-id="945ef-106">Per creare una connessione crittografata, è necessario che i plug-in EAP generino le chiavi di crittografia e le restituiscano tramite gli attributi RADIUS specifici del fornitore Microsoft MS-MPPE-send-keys e MS-MPPE-ricezione-Keys.</span><span class="sxs-lookup"><span data-stu-id="945ef-106">In order to create an encrypted connection, EAP plug-ins must generate encryption keys and return them through the Microsoft vendor-specific RADIUS Attributes MS-MPPE-Send-Keys and MS-MPPE-Recv-Keys.</span></span> <span data-ttu-id="945ef-107">Per ulteriori informazioni, vedere la sezione osservazioni nell' [**\_ \_ output EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) .</span><span class="sxs-lookup"><span data-stu-id="945ef-107">See the Remarks section in [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) for more information.</span></span>

## <a name="wireless-guidelines"></a><span data-ttu-id="945ef-108">Linee guida wireless</span><span class="sxs-lookup"><span data-stu-id="945ef-108">Wireless Guidelines</span></span>

<span data-ttu-id="945ef-109">Di seguito sono riportate le linee guida e le indicazioni per la scrittura di un plug-in EAP che supporti l'autenticazione di computer in scenari wireless (802.1 X).</span><span class="sxs-lookup"><span data-stu-id="945ef-109">The following are guidelines and recommendations for writing an EAP Plug-in that supports authenticating machines in wireless (802.1X) scenarios.</span></span> <span data-ttu-id="945ef-110">Questa sezione non si applica a scenari VPN e remote.</span><span class="sxs-lookup"><span data-stu-id="945ef-110">This section does not apply to VPN and Dial-up scenarios.</span></span>

-   <span data-ttu-id="945ef-111">Per non bloccare l'esecuzione di sistemi automatici, i plug-in EAP non devono effettuare chiamate all'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="945ef-111">In order not to block unattended systems' execution, EAP plug-ins must not make any user interface calls.</span></span>
-   <span data-ttu-id="945ef-112">L'implementazione del plug-in EAP del passaggio di autenticazione del computer deve essere completata il più rapidamente possibile, in modo da non ostacolare l'avvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="945ef-112">The EAP Plug-in implementation of the machine authentication step must complete as quickly as possible so it does not hinder operating system startup.</span></span>
    > [!Note]  
    > <span data-ttu-id="945ef-113">Se il protocollo EAP non supporta l'autenticazione del computer, deve verificare il flag di autenticazione del computer, l'autenticazione del **computer del \_ \_ flag EAP \_ \_ RAS** usato nel campo **fFlags** nell' [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)e restituire un errore.</span><span class="sxs-lookup"><span data-stu-id="945ef-113">If your EAP protocol does not support machine authentication, it must check for the machine authentication flag, **RAS\_EAP\_FLAG\_MACHINE\_AUTH** used in the **fFlags** field in [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), and return an error.</span></span>

     

 

 




