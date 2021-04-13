---
title: Classi di configurazione Servizi Desktop remoto
description: Il provider WMI per la configurazione di Servizi Desktop remoto fornisce le classi seguenti. Di seguito è riportata un'illustrazione.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc9c58be85b8b4efc35495f35902ab67b35ad153
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399070"
---
# <a name="remote-desktop-services-configuration-classes"></a><span data-ttu-id="cb88c-104">Classi di configurazione Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="cb88c-104">Remote Desktop Services Configuration classes</span></span>

<span data-ttu-id="cb88c-105">Il provider WMI per la configurazione di Servizi Desktop remoto fornisce le classi seguenti.</span><span class="sxs-lookup"><span data-stu-id="cb88c-105">The Remote Desktop Services Configuration WMI provider provides the following classes.</span></span> <span data-ttu-id="cb88c-106">Di seguito è riportata un'illustrazione.</span><span class="sxs-lookup"><span data-stu-id="cb88c-106">An illustration follows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cb88c-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cb88c-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="cb88c-108">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="cb88c-108">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-109">Rappresenta l'associazione tra gli elementi del sistema gestito e la classe di impostazione definita.</span><span class="sxs-lookup"><span data-stu-id="cb88c-109">Represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-110">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="cb88c-110">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="cb88c-111">Classe di base per tutti i componenti di sistema che rappresentano componenti di sistema astratti, ad esempio profili, processi o funzionalità di sistema, sotto forma di dispositivi logici.</span><span class="sxs-lookup"><span data-stu-id="cb88c-111">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-112">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="cb88c-112">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="cb88c-113">Classe base per la gerarchia degli elementi di sistema.</span><span class="sxs-lookup"><span data-stu-id="cb88c-113">The base class for the system element hierarchy.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-114">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="cb88c-114">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="cb88c-115">Rappresenta i parametri operativi e relativi alla configurazione per uno o più elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="cb88c-115">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-116">**\_Terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-116">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dd>

<span data-ttu-id="cb88c-117">rappresenta un terminale.</span><span class="sxs-lookup"><span data-stu-id="cb88c-117">represents a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-118">**\_TerminalError Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-118">**Win32\_TerminalError**</span></span>](win32-terminalerror.md)
</dt> <dd>

<span data-ttu-id="cb88c-119">Rappresenta un errore del terminale.</span><span class="sxs-lookup"><span data-stu-id="cb88c-119">Represents a terminal error.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-120">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-120">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dd>

<span data-ttu-id="cb88c-121">sottoclasse della classe [**del \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="cb88c-121">a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="cb88c-122">[**Win32 \_ TerminalService**](win32-terminalservice.md) rappresenta la proprietà dell' **elemento** dell' [**associazione \_ TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="cb88c-122">[**Win32\_TerminalService**](win32-terminalservice.md) represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-123">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-123">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-124">rappresenta la configurazione per un server Host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="cb88c-124">represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-125">**\_TerminalServiceToSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-125">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-126">rappresenta l'associazione tra un'istanza della classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e l'impostazione di una particolare proprietà [**\_ TerminalServiceSetting Win32**](win32-terminalservicesetting.md) .</span><span class="sxs-lookup"><span data-stu-id="cb88c-126">represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-127">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-127">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-128">rappresenta le impostazioni che è possibile applicare a un terminale.</span><span class="sxs-lookup"><span data-stu-id="cb88c-128">represents the settings that can be applied to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-129">**\_TerminalTerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-129">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-130">rappresenta l'associazione tra un terminale e le relative impostazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="cb88c-130">represents the association between a terminal and its configuration settings.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-131">**\_TSAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-131">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> <dd>

<span data-ttu-id="cb88c-132">consente l'eliminazione di un account esistente nel [**\_ terminale Win32**](win32-terminal.md) e la modifica delle autorizzazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="cb88c-132">allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-133">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-133">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-134">definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) correlate ai criteri di connessione.</span><span class="sxs-lookup"><span data-stu-id="cb88c-134">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-135">**\_TSDiscoveredLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-135">**Win32\_TSDiscoveredLicenseServer**</span></span>](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

<span data-ttu-id="cb88c-136">Fornisce informazioni dettagliate sul server licenze Desktop remoto individuato.</span><span class="sxs-lookup"><span data-stu-id="cb88c-136">Provides details about the discovered Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-137">**\_TSEnvironmentSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-138">definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) , inclusi i criteri di programma iniziali.</span><span class="sxs-lookup"><span data-stu-id="cb88c-138">defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-139">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-139">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-140">rappresenta le impostazioni generali del terminale, ad esempio il livello di crittografia e il protocollo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="cb88c-140">represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-141">**\_TSLogonSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-142">definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) correlate all'accesso client.</span><span class="sxs-lookup"><span data-stu-id="cb88c-142">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-143">**\_TSNetworkAdapterListSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-143">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-144">Enumera l'elenco di schede di rete che possono essere configurate per un [**\_ terminale Win32**](win32-terminal.md), in base al protocollo Terminal e al metodo di trasporto specificati.</span><span class="sxs-lookup"><span data-stu-id="cb88c-144">enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-145">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-145">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-146">definisce diverse impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) , incluse le proprietà correlate alla scheda di rete e il numero massimo di connessioni consentite.</span><span class="sxs-lookup"><span data-stu-id="cb88c-146">defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-147">**\_TSPermissionsSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-147">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-148">include un metodo per aggiungere nuovi account al terminale e un metodo per ripristinare le autorizzazioni predefinite per un terminale.</span><span class="sxs-lookup"><span data-stu-id="cb88c-148">includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-149">**\_TSRemoteControlSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-150">definisce le impostazioni di configurazione del controllo remoto per la classe [**\_ terminale Win32**](win32-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="cb88c-150">defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-151">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-151">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dd>

<span data-ttu-id="cb88c-152">Definisce le impostazioni di configurazione di Connessione Desktop remoto broker (gestore connessione Desktop remoto) per la classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="cb88c-152">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-153">**\_TSSessionDirectorySetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-153">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-154">Rappresenta l'associazione tra un'istanza della classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e un'istanza della classe [**\_ TSSessionDirectory Win32**](win32-tssessiondirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="cb88c-154">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-155">**\_TSSessionSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-155">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-156">definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) , ad esempio i limiti di tempo e le azioni di disconnessione e riconnessione.</span><span class="sxs-lookup"><span data-stu-id="cb88c-156">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-157">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-157">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> <dd>

<span data-ttu-id="cb88c-158">Definisce le impostazioni di virtualizzazione IP (Internet Protocol) per un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="cb88c-158">Defines Internet protocol (IP) virtualization settings for a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="cb88c-159">**\_TSVirtualIPSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cb88c-159">**Win32\_TSVirtualIPSetting**</span></span>](win32-tsvirtualipsetting.md)
</dt> <dd>

<span data-ttu-id="cb88c-160">Rappresenta l'associazione tra una classe di elementi [**Win32 \_ TerminalService**](win32-terminalservice.md) e una classe di impostazioni [**\_ TSVirtualIP Win32**](win32-tsvirtualip.md) .</span><span class="sxs-lookup"><span data-stu-id="cb88c-160">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

</dd> </dl>

<span data-ttu-id="cb88c-161">Nella figura seguente sono illustrate le relazioni tra queste classi.</span><span class="sxs-lookup"><span data-stu-id="cb88c-161">The following illustration shows the relationships between these classes.</span></span>

![relazioni tra le classi supportate](images/tswmi.png)

 

 