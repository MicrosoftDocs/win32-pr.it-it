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
# <a name="remote-desktop-services-configuration-classes"></a>Classi di configurazione Servizi Desktop remoto

Il provider WMI per la configurazione di Servizi Desktop remoto fornisce le classi seguenti. Di seguito è riportata un'illustrazione.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dd>

Rappresenta l'associazione tra gli elementi del sistema gestito e la classe di impostazione definita.

</dd> <dt>

[**\_LogicalElement CIM**](cim-logicalelement.md)
</dt> <dd>

Classe di base per tutti i componenti di sistema che rappresentano componenti di sistema astratti, ad esempio profili, processi o funzionalità di sistema, sotto forma di dispositivi logici.

</dd> <dt>

[**\_MANAGEDSYSTEMELEMENT CIM**](cim-managedsystemelement.md)
</dt> <dd>

Classe base per la gerarchia degli elementi di sistema.

</dd> <dt>

[**\_Impostazione CIM**](cim-setting.md)
</dt> <dd>

Rappresenta i parametri operativi e relativi alla configurazione per uno o più elementi di sistema gestiti.

</dd> <dt>

[**\_Terminale Win32**](win32-terminal.md)
</dt> <dd>

rappresenta un terminale.

</dd> <dt>

[**\_TerminalError Win32**](win32-terminalerror.md)
</dt> <dd>

Rappresenta un errore del terminale.

</dd> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dd>

sottoclasse della classe [**del \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) . [**Win32 \_ TerminalService**](win32-terminalservice.md) rappresenta la proprietà dell' **elemento** dell' [**associazione \_ TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md) .

</dd> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> <dd>

rappresenta la configurazione per un server Host sessione Desktop remoto (host sessione Desktop remoto).

</dd> <dt>

[**\_TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md)
</dt> <dd>

rappresenta l'associazione tra un'istanza della classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e l'impostazione di una particolare proprietà [**\_ TerminalServiceSetting Win32**](win32-terminalservicesetting.md) .

</dd> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> <dd>

rappresenta le impostazioni che è possibile applicare a un terminale.

</dd> <dt>

[**\_TerminalTerminalSetting Win32**](win32-terminalterminalsetting.md)
</dt> <dd>

rappresenta l'associazione tra un terminale e le relative impostazioni di configurazione.

</dd> <dt>

[**\_TSAccount Win32**](win32-tsaccount.md)
</dt> <dd>

consente l'eliminazione di un account esistente nel [**\_ terminale Win32**](win32-terminal.md) e la modifica delle autorizzazioni esistenti.

</dd> <dt>

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> <dd>

definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) correlate ai criteri di connessione.

</dd> <dt>

[**\_TSDiscoveredLicenseServer Win32**](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

Fornisce informazioni dettagliate sul server licenze Desktop remoto individuato.

</dd> <dt>

[**\_TSEnvironmentSetting Win32**](win32-tsenvironmentsetting.md)
</dt> <dd>

definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) , inclusi i criteri di programma iniziali.

</dd> <dt>

[**\_TSGeneralSetting Win32**](win32-tsgeneralsetting.md)
</dt> <dd>

rappresenta le impostazioni generali del terminale, ad esempio il livello di crittografia e il protocollo di trasporto.

</dd> <dt>

[**\_TSLogonSetting Win32**](win32-tslogonsetting.md)
</dt> <dd>

definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) correlate all'accesso client.

</dd> <dt>

[**\_TSNetworkAdapterListSetting Win32**](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

Enumera l'elenco di schede di rete che possono essere configurate per un [**\_ terminale Win32**](win32-terminal.md), in base al protocollo Terminal e al metodo di trasporto specificati.

</dd> <dt>

[**\_TSNetworkAdapterSetting Win32**](win32-tsnetworkadaptersetting.md)
</dt> <dd>

definisce diverse impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) , incluse le proprietà correlate alla scheda di rete e il numero massimo di connessioni consentite.

</dd> <dt>

[**\_TSPermissionsSetting Win32**](win32-tspermissionssetting.md)
</dt> <dd>

include un metodo per aggiungere nuovi account al terminale e un metodo per ripristinare le autorizzazioni predefinite per un terminale.

</dd> <dt>

[**\_TSRemoteControlSetting Win32**](win32-tsremotecontrolsetting.md)
</dt> <dd>

definisce le impostazioni di configurazione del controllo remoto per la classe [**\_ terminale Win32**](win32-terminal.md) .

</dd> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> <dd>

Definisce le impostazioni di configurazione di Connessione Desktop remoto broker (gestore connessione Desktop remoto) per la classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .

</dd> <dt>

[**\_TSSessionDirectorySetting Win32**](win32-tssessiondirectorysetting.md)
</dt> <dd>

Rappresenta l'associazione tra un'istanza della classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e un'istanza della classe [**\_ TSSessionDirectory Win32**](win32-tssessiondirectory.md) .

</dd> <dt>

[**\_TSSessionSetting Win32**](win32-tssessionsetting.md)
</dt> <dd>

definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) , ad esempio i limiti di tempo e le azioni di disconnessione e riconnessione.

</dd> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> <dd>

Definisce le impostazioni di virtualizzazione IP (Internet Protocol) per un server Host sessione Desktop remoto.

</dd> <dt>

[**\_TSVirtualIPSetting Win32**](win32-tsvirtualipsetting.md)
</dt> <dd>

Rappresenta l'associazione tra una classe di elementi [**Win32 \_ TerminalService**](win32-terminalservice.md) e una classe di impostazioni [**\_ TSVirtualIP Win32**](win32-tsvirtualip.md) .

</dd> </dl>

Nella figura seguente sono illustrate le relazioni tra queste classi.

![relazioni tra le classi supportate](images/tswmi.png)

 

 