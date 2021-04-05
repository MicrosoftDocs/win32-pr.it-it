---
title: Linee guida sulla sicurezza
description: È importante informare l'utente sui possibili problemi di sicurezza.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118219"
---
# <a name="security-guideline"></a><span data-ttu-id="3ac7e-103">Linee guida sulla sicurezza</span><span class="sxs-lookup"><span data-stu-id="3ac7e-103">Security Guideline</span></span>

<span data-ttu-id="3ac7e-104">È importante informare l'utente sui possibili problemi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="3ac7e-104">It is important to keep the user informed about possible security issues.</span></span>

## <a name="notify-the-user-of-security-related-events"></a><span data-ttu-id="3ac7e-105">Invia notifica all'utente di eventi Security-Related</span><span class="sxs-lookup"><span data-stu-id="3ac7e-105">Notify the User of Security-Related Events</span></span>

<span data-ttu-id="3ac7e-106">Informare sempre l'utente di eventuali modifiche apportate alla sicurezza, sia che si tratti di un errore correlato alla sicurezza, ad esempio un errore di certificato, o di una modifica della sicurezza del protocollo sottostante, ad esempio il passaggio da un sito HTTPS a un sito HTTP.</span><span class="sxs-lookup"><span data-stu-id="3ac7e-106">Always notify the user of any change in security, whether it is a security-related error such as a certificate failure, or a change in the security of the underlying protocol, such as change from an HTTPS site to an HTTP site.</span></span>

## <a name="notify-the-user-of-security-related-errors"></a><span data-ttu-id="3ac7e-107">Notifica all'utente Security-Related errori</span><span class="sxs-lookup"><span data-stu-id="3ac7e-107">Notify the User of Security-Related Errors</span></span>

<span data-ttu-id="3ac7e-108">Quando l'applicazione riceve un messaggio di errore che può indicare un problema di sicurezza, la funzione **InternetErrorDlg** fornisce un'interfaccia standard e familiare per inviare una notifica all'utente nella maggior parte dei casi.</span><span class="sxs-lookup"><span data-stu-id="3ac7e-108">When your application receives an error message that may indicate a security problem, the **InternetErrorDlg** function provides a standard, familiar interface for notifying the user in most cases.</span></span>

<span data-ttu-id="3ac7e-109">Tra gli errori che rientrano in questa categoria:</span><span class="sxs-lookup"><span data-stu-id="3ac7e-109">Among the errors that fall in this category are:</span></span>

<span data-ttu-id="3ac7e-110">**ERRORE \_ \_ da http \_ a HTTPS da Internet a \_ \_ \_ redir**</span><span class="sxs-lookup"><span data-stu-id="3ac7e-110">**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>

<span data-ttu-id="3ac7e-111">**ERRORE \_ Internet \_ CA non valida \_**</span><span class="sxs-lookup"><span data-stu-id="3ac7e-111">**ERROR\_INTERNET\_INVALID\_CA**</span></span>

<span data-ttu-id="3ac7e-112">**ERRORE \_ Internet \_ Post \_ \_ non \_ sicuro**</span><span class="sxs-lookup"><span data-stu-id="3ac7e-112">**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>

<span data-ttu-id="3ac7e-113">**\_errori del certificato di Internet \_ sec errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ac7e-113">**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>

<span data-ttu-id="3ac7e-114">**ERRORE per il \_ \_ certificato CN di Internet sec \_ \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="3ac7e-114">**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>

<span data-ttu-id="3ac7e-115">**ERRORE in \_ Internet \_ sec \_ CERT \_ data \_ non valida**</span><span class="sxs-lookup"><span data-stu-id="3ac7e-115">**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>

<span data-ttu-id="3ac7e-116">Un errore di notifica all'utente di errori come questi possono esporre l'utente a vari tipi di violazioni della sicurezza, inclusi gli attacchi di spoofing o la divulgazione di informazioni non volontarie.</span><span class="sxs-lookup"><span data-stu-id="3ac7e-116">A failure to notify the user of errors such as these can expose the user to various sorts of security breaches, including spoofing attacks or involuntary information disclosure.</span></span>

## <a name="notify-the-user-when-connection-security-changes"></a><span data-ttu-id="3ac7e-117">Notifica all'utente quando viene modificata la sicurezza della connessione</span><span class="sxs-lookup"><span data-stu-id="3ac7e-117">Notify the User When Connection Security Changes</span></span>

<span data-ttu-id="3ac7e-118">Inviare sempre notifiche all'utente quando viene modificata la sicurezza della connessione, ad esempio da HTTPS a HTTP.</span><span class="sxs-lookup"><span data-stu-id="3ac7e-118">Always notify the user when the security of the connection changes, for example from HTTPS to HTTP.</span></span> <span data-ttu-id="3ac7e-119">In caso contrario, a meno che l'utente non abbia scelto in modo esplicito di non ricevere notifiche di tali modifiche, si nascondono i rischi derivanti dalla divulgazione involontaria di informazioni.</span><span class="sxs-lookup"><span data-stu-id="3ac7e-119">Otherwise, unless the user has explicitly chosen not to be notified of such changes, you are concealing the risks of involuntary information disclosure.</span></span>

<span data-ttu-id="3ac7e-120">Tra le funzioni che segnalano una modifica di questo tipo nella sicurezza delle connessioni si trovano la funzione di callback **InternetStatusCallback** e la funzione **InternetConfirmZoneCrossing** .</span><span class="sxs-lookup"><span data-stu-id="3ac7e-120">Among the functions that report such a change in connection security are the **InternetStatusCallback** callback function and the **InternetConfirmZoneCrossing** function.</span></span>

> [!Note]  
> <span data-ttu-id="3ac7e-121">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="3ac7e-121">WinINet does not support server implementations.</span></span> <span data-ttu-id="3ac7e-122">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="3ac7e-122">In addition, it should not be used from a service.</span></span> <span data-ttu-id="3ac7e-123">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="3ac7e-123">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 