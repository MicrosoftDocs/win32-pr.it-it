---
title: Costanti di sessione
description: Le costanti di sessione nell' \_ \_ enumerazione WSManSessionFlags specificano l'autenticazione e altre informazioni per le chiamate a WSMan. CreateSession o IWSMan CreateSession che si connettono a un computer remoto.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297817"
---
# <a name="session-constants"></a><span data-ttu-id="ef384-103">Costanti di sessione</span><span class="sxs-lookup"><span data-stu-id="ef384-103">Session Constants</span></span>

<span data-ttu-id="ef384-104">Le costanti di sessione nell'enumerazione **\_ \_ WSManSessionFlags** specificano l'autenticazione e altre informazioni per le chiamate [**WSMan. CreateSession**](wsman-createsession.md) o [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) che si connettono a un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="ef384-104">The session constants in the **\_\_WSManSessionFlags** enumeration specify authentication and other information for [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span> <span data-ttu-id="ef384-105">Queste costanti sono anche strettamente correlate alle opzioni dello strumento da riga di comando **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="ef384-105">These constants are also closely related to **Winrm** command-line tool switches.</span></span>

## <a name="using-session-constants"></a><span data-ttu-id="ef384-106">Utilizzo delle costanti di sessione</span><span class="sxs-lookup"><span data-stu-id="ef384-106">Using Session Constants</span></span>

<span data-ttu-id="ef384-107">È possibile impostare i flag di sessione per la chiamata a [**WSMan. CreateSession**](wsman-createsession.md) in due modi diversi.</span><span class="sxs-lookup"><span data-stu-id="ef384-107">You can set the Session flags for the call to [**WSMan.CreateSession**](wsman-createsession.md) in two different ways.</span></span> <span data-ttu-id="ef384-108">Uno è più breve e più semplice.</span><span class="sxs-lookup"><span data-stu-id="ef384-108">One is shorter and simpler.</span></span> <span data-ttu-id="ef384-109">Il modo più lungo, come illustrato nell'esempio seguente, consiste nell'individuare il valore del flag che si vuole usare e creare una costante nello script con tale valore.</span><span class="sxs-lookup"><span data-stu-id="ef384-109">The longer way, as is shown in the following example, is to locate the value of the flag you want to use and create a constant in your script with that value.</span></span> <span data-ttu-id="ef384-110">La costante viene quindi utilizzata per impostare il valore del parametro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="ef384-110">Then the constant is used to set the value of the *iFlags* parameter.</span></span>

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

<span data-ttu-id="ef384-111">La modalità consigliata, come illustrato nell'esempio seguente, consiste nell'usare il metodo dell'oggetto [**WSMan**](wsman.md) associato al flag.</span><span class="sxs-lookup"><span data-stu-id="ef384-111">The recommended way, as shown in the following example, is to use the [**WSMan**](wsman.md) object method associated with the flag.</span></span>

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span data-ttu-id="ef384-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Costanti di autenticazione**](authentication-constants.md)</span><span class="sxs-lookup"><span data-stu-id="ef384-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Authentication Constants**](authentication-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="ef384-113">Specificare il metodo di autenticazione e la modalità di gestione dei server di certificati.</span><span class="sxs-lookup"><span data-stu-id="ef384-113">Specify the authentication method and how to handle certificate servers.</span></span>

</dd> <dt>

<span data-ttu-id="ef384-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Altre costanti di sessione**](other-session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="ef384-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Other Session Constants**](other-session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="ef384-115">Specificare la porta di codifica, crittografia e nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="ef384-115">Specify the encoding, encryption, and service principal name port.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ef384-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ef384-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef384-117">Costanti ed enumerazioni WinRM</span><span class="sxs-lookup"><span data-stu-id="ef384-117">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="ef384-118">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="ef384-118">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="ef384-119">Autenticazione per le connessioni remote</span><span class="sxs-lookup"><span data-stu-id="ef384-119">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> </dl>

 

 




