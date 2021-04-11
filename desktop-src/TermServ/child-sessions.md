---
title: Sessioni figlio
description: A partire da Windows Server 2012 e Windows 8, Desktop remoto supporta il concetto di sessione figlio, ovvero una sessione speciale di Desktop remoto loopback collegata alla sessione esistente di un utente.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220966"
---
# <a name="child-sessions"></a><span data-ttu-id="79ffd-103">Sessioni figlio</span><span class="sxs-lookup"><span data-stu-id="79ffd-103">Child Sessions</span></span>

<span data-ttu-id="79ffd-104">A partire da Windows Server 2012 e Windows 8, Desktop remoto supporta il concetto di *sessione figlio*, ovvero una sessione speciale di desktop remoto loopback collegata alla sessione esistente di un utente.</span><span class="sxs-lookup"><span data-stu-id="79ffd-104">Beginning with Windows Server 2012 and Windows 8, Remote Desktop supports the concept of a *child session*, which is a special loopback Remote Desktop session that is tied to a user's existing session.</span></span>

<span data-ttu-id="79ffd-105">Le sessioni figlio non sono supportate nei sistemi operativi seguenti:</span><span class="sxs-lookup"><span data-stu-id="79ffd-105">Child sessions are not supported on the following operating systems:</span></span>

<dl> <span data-ttu-id="79ffd-106">Windows RT</span><span class="sxs-lookup"><span data-stu-id="79ffd-106">Windows RT</span></span>  
<span data-ttu-id="79ffd-107">Opzione di installazione Server Core di Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79ffd-107">Windows Server 2012 Server Core installation option</span></span>  
<span data-ttu-id="79ffd-108">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="79ffd-108">Microsoft Hyper-V Server 2012</span></span>  
</dl>

<span data-ttu-id="79ffd-109">Un sistema può avere una sola sessione figlio attiva e connessa in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="79ffd-109">A system can only have one active and connected child session at any given time.</span></span>

<span data-ttu-id="79ffd-110">La sessione figlio può essere terminata disconnettendosi direttamente da tale sessione o verrà terminata al termine della sessione padre.</span><span class="sxs-lookup"><span data-stu-id="79ffd-110">The child session can be terminated by logging off directly from it, or it will be terminated when its parent session terminates.</span></span>

<span data-ttu-id="79ffd-111">Prima di poter utilizzare le sessioni figlio in un sistema, è necessario abilitare la funzionalità della sessione figlio chiamando la funzione [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) .</span><span class="sxs-lookup"><span data-stu-id="79ffd-111">Before child sessions can be used on a system, you must enable the child session functionality by calling the [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) function.</span></span> <span data-ttu-id="79ffd-112">È inoltre possibile determinare se le sessioni figlio sono state abilitate tramite la funzione [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) .</span><span class="sxs-lookup"><span data-stu-id="79ffd-112">You can also determine if child sessions have been enabled by using the [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) function.</span></span>

<span data-ttu-id="79ffd-113">Una sessione figlio può essere creata solo dall'interno di una sessione utente esistente usando il [controllo ActiveX Desktop remoto](remote-desktop-activex-control.md) e impostando la proprietà "ConnectToChildSession" con [**IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md) prima della connessione.</span><span class="sxs-lookup"><span data-stu-id="79ffd-113">A child session can only be created from within an existing user's session by using the [Remote Desktop ActiveX control](remote-desktop-activex-control.md) and setting the "ConnectToChildSession" property with [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) prior to connecting.</span></span> <span data-ttu-id="79ffd-114">Quando viene chiamato il metodo [**IMsTscAx. Connect**](imstscax-connect.md) , il controllo ActiveX Desktop remoto effettuerà automaticamente l'accesso alla sessione figlio senza richiedere le credenziali, tranne quando l'utente è connesso alla sessione padre tramite una smart card.</span><span class="sxs-lookup"><span data-stu-id="79ffd-114">When the [**IMsTscAx.Connect**](imstscax-connect.md) method is called, the Remote Desktop ActiveX control will automatically log on to the child session without prompting for credentials, except when the user is logged into the parent session using a smart card.</span></span> <span data-ttu-id="79ffd-115">A differenza di una normale sessione di Desktop remoto, un utente non necessita del diritto interattivo remoto per accedere alla sessione figlio perché si tratta di una sessione di loopback.</span><span class="sxs-lookup"><span data-stu-id="79ffd-115">Unlike a regular Remote Desktop session, a user does not need the Remote Interactive right to log on to the child session because this is a loopback session.</span></span>

<span data-ttu-id="79ffd-116">Una sessione figlio non può essere bloccata.</span><span class="sxs-lookup"><span data-stu-id="79ffd-116">A child session cannot be locked.</span></span> <span data-ttu-id="79ffd-117">Non avrà screen saver e nessuna schermata di accesso.</span><span class="sxs-lookup"><span data-stu-id="79ffd-117">It will have no screen saver and no logon screen.</span></span> <span data-ttu-id="79ffd-118">Inoltre, a differenza di una sessione normale, se è impostato il criterio del testo di accesso WinLogon, il testo di accesso non verrà visualizzato in questa sessione figlio.</span><span class="sxs-lookup"><span data-stu-id="79ffd-118">Also, unlike a regular session, if the WinLogon logon text policy is set, the logon text will not be displayed in this child session.</span></span> <span data-ttu-id="79ffd-119">Se questi criteri sono impostati, inoltre, non si verifica alcun effetto dei criteri di gruppo di timeout Connessione Desktop remoto nella sessione figlio.</span><span class="sxs-lookup"><span data-stu-id="79ffd-119">Also, there will be no effect of Remote Desktop Connection Timeout Group policies on the child session if these policies are set.</span></span>

<span data-ttu-id="79ffd-120">Le API seguenti vengono usate insieme alle sessioni figlio:</span><span class="sxs-lookup"><span data-stu-id="79ffd-120">The following APIs are used in conjunction with child sessions:</span></span>

-   [<span data-ttu-id="79ffd-121">**WTSEnableChildSessions**</span><span class="sxs-lookup"><span data-stu-id="79ffd-121">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [<span data-ttu-id="79ffd-122">**WTSIsChildSessionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="79ffd-122">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [<span data-ttu-id="79ffd-123">**WTSGetChildSessionId**</span><span class="sxs-lookup"><span data-stu-id="79ffd-123">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   <span data-ttu-id="79ffd-124">Proprietà "ConnectToChildSession" in [ **IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md)</span><span class="sxs-lookup"><span data-stu-id="79ffd-124">"ConnectToChildSession" property in [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)</span></span>

 

 




