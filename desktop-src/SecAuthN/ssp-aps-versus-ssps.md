---
description: Vengono illustrate le differenze tra SSP/APs e SSP.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APs e SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968137"
---
# <a name="sspaps-vs-ssps"></a><span data-ttu-id="1842c-103">SSP/APs e SSP</span><span class="sxs-lookup"><span data-stu-id="1842c-103">SSP/APs vs. SSPs</span></span>

<span data-ttu-id="1842c-104">I [*pacchetti di sicurezza*](../secgloss/s-gly.md) vengono distribuiti in uno dei seguenti tipi di librerie a collegamento dinamico (dll):</span><span class="sxs-lookup"><span data-stu-id="1842c-104">[*Security packages*](../secgloss/s-gly.md) are deployed in one of the following types of dynamic-link libraries (DLLs):</span></span>

-   [<span data-ttu-id="1842c-105">SSP/APs</span><span class="sxs-lookup"><span data-stu-id="1842c-105">SSP/APs</span></span>](#sspaps-vs-ssps)
-   [<span data-ttu-id="1842c-106">Provider</span><span class="sxs-lookup"><span data-stu-id="1842c-106">SSPs</span></span>](#sspaps-vs-ssps)

<span data-ttu-id="1842c-107">Il fatto che un pacchetto di sicurezza si trovi in un pacchetto di Security Support Provider/[*autenticazione*](../secgloss/a-gly.md) (SSP/AP) o in una DLL di [*Security Support Provider*](../secgloss/s-gly.md) (SSP) è determinato dai tipi di servizi di sicurezza forniti e dal livello di integrazione con l' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA).</span><span class="sxs-lookup"><span data-stu-id="1842c-107">Whether a security package is in a security support provider/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) or a [*security support provider*](../secgloss/s-gly.md) (SSP) DLL is determined by the types of security services it provides and the extent to which it requires integration with the [*Local Security Authority*](../secgloss/l-gly.md) (LSA).</span></span> <span data-ttu-id="1842c-108">Queste differenze determinano anche l'API implementata in un pacchetto di sicurezza personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1842c-108">These differences also determine the API implemented in a custom security package.</span></span>

## <a name="sspaps"></a><span data-ttu-id="1842c-109">SSP/APs</span><span class="sxs-lookup"><span data-stu-id="1842c-109">SSP/APs</span></span>

<span data-ttu-id="1842c-110">Un SSP/AP è una DLL che contiene uno o più [*pacchetti di sicurezza*](../secgloss/s-gly.md) e può fungere da SSP per le applicazioni client/server e come [pacchetto di autenticazione](authentication-packages.md) per le applicazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="1842c-110">An SSP/AP is a DLL that contains one or more [*Security packages*](../secgloss/s-gly.md) and can function as an SSP for client/server applications and as an [authentication package](authentication-packages.md) for logon applications.</span></span> <span data-ttu-id="1842c-111">Per funzionare in entrambi i ruoli, SSP/APs vengono caricati nello spazio di elaborazione LSA all'avvio del sistema e possono essere caricati anche nei processi dell'applicazione client/server.</span><span class="sxs-lookup"><span data-stu-id="1842c-111">To function in both of these roles, SSP/APs are loaded into the LSA process space at system startup and can be loaded into client/server application processes as well.</span></span>

<span data-ttu-id="1842c-112">I pacchetti di sicurezza SSP/AP personalizzati devono implementare sia le [funzioni implementate da SSP/APS in modalità utente](authentication-functions.md)che le [funzioni implementate da SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1842c-112">Custom SSP/AP security packages must implement both the [Functions Implemented by User-mode SSP/APs](authentication-functions.md), and [Functions Implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="1842c-113">Queste implementazioni di funzioni possono avvalersi delle funzioni di supporto LSA per offrire funzionalità di sicurezza avanzate, ad esempio la creazione di token, il supporto [*supplementare delle credenziali*](../secgloss/s-gly.md) e l'autenticazione pass-through.</span><span class="sxs-lookup"><span data-stu-id="1842c-113">These function implementations can make use of LSA support functions to offer advanced security features such as token creation, [*supplemental credentials*](../secgloss/s-gly.md) support, and pass-through authentication.</span></span>

<span data-ttu-id="1842c-114">Se un pacchetto di sicurezza SSP/AP personalizzato fornisce la gamma completa di funzioni di [*integrità*](../secgloss/i-gly.md) e privacy dei messaggi, implementa anche le [funzioni implementate da SSP/APS in modalità utente](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1842c-114">If a custom SSP/AP security package provides the full range of message [*integrity*](../secgloss/i-gly.md) and privacy functions, it will also implement the [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span>

## <a name="ssps"></a><span data-ttu-id="1842c-115">Provider</span><span class="sxs-lookup"><span data-stu-id="1842c-115">SSPs</span></span>

<span data-ttu-id="1842c-116">Un SSP è una DLL che contiene uno o più pacchetti di sicurezza che forniscono servizi autenticati di connessione, integrità dei messaggi e crittografia messaggi alle applicazioni client/server.</span><span class="sxs-lookup"><span data-stu-id="1842c-116">An SSP is a DLL that contains one or more security packages that provide authenticated connection, message integrity, and message encryption services to client/server applications.</span></span> <span data-ttu-id="1842c-117">Gli SSP implementano le funzioni SSPI ( [Security Support Provider Interface](sspi.md) ).</span><span class="sxs-lookup"><span data-stu-id="1842c-117">SSPs implement [Security Support Provider Interface](sspi.md) (SSPI) functions.</span></span> <span data-ttu-id="1842c-118">Le applicazioni possono accedere ai pacchetti di sicurezza in un SSP chiamando direttamente le funzioni SSPI.</span><span class="sxs-lookup"><span data-stu-id="1842c-118">Applications can access the security packages in an SSP by calling the SSPI functions directly.</span></span> <span data-ttu-id="1842c-119">I SSP vengono caricati nei processi client e server; non sono integrati con LSA.</span><span class="sxs-lookup"><span data-stu-id="1842c-119">SSPs are loaded into the client and server processes; they are not integrated with the LSA.</span></span>

 

 
