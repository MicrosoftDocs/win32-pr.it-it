---
title: classi Servizi Desktop remoto Configuration
description: Il provider WMI Servizi Desktop remoto configuration fornisce le classi seguenti. Di seguito è riportata una figura.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de40784e1e0c9e0387b8d6ff60193639032f7e0cbe5e34c4a8b35aeb32cc37cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000127"
---
# <a name="remote-desktop-services-configuration-classes"></a>classi Servizi Desktop remoto Configuration

Il provider WMI Servizi Desktop remoto configuration fornisce le classi seguenti. Di seguito è riportata una figura.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**CIM \_ ElementSetting**](cim-elementsetting.md)
</dt> <dd>

Rappresenta l'associazione tra gli elementi di sistema gestiti e la classe di impostazione definita per essi.

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

Classe di base per tutti i componenti di sistema che rappresentano componenti di sistema astratti, ad esempio profili, processi o funzionalità di sistema, sotto forma di dispositivi logici.

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

Classe di base per la gerarchia degli elementi di sistema.

</dd> <dt>

[**Impostazione \_ CIM**](cim-setting.md)
</dt> <dd>

Rappresenta i parametri operativi e correlati alla configurazione per uno o più elementi di sistema gestiti.

</dd> <dt>

[**Terminale Win32 \_**](win32-terminal.md)
</dt> <dd>

rappresenta un terminale.

</dd> <dt>

[**Terminale \_ Win32Error**](win32-terminalerror.md)
</dt> <dd>

Rappresenta un errore terminale.

</dd> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dd>

sottoclasse della [**classe Del \_ servizio Win32.**](/windows/desktop/CIMWin32Prov/win32-service) [**Win32 \_ TerminalService rappresenta**](win32-terminalservice.md) la **proprietà Element** dell'associazione [**\_ TerminalServiceToSetting Win32.**](win32-terminalservicetosetting.md)

</dd> <dt>

[**\_Terminale Win32ServiceSetting**](win32-terminalservicesetting.md)
</dt> <dd>

rappresenta la configurazione per un Desktop remoto host sessione Desktop remoto.

</dd> <dt>

[**\_Terminale Win32ServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dd>

rappresenta l'associazione tra un'istanza della [**classe \_ TerminalService Win32**](win32-terminalservice.md) e l'impostazione di una determinata proprietà [**\_ TerminalServiceSetting Win32.**](win32-terminalservicesetting.md)

</dd> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dd>

rappresenta le impostazioni che possono essere applicate a un terminale.

</dd> <dt>

[**\_Terminale Win32TerminalSetting**](win32-terminalterminalsetting.md)
</dt> <dd>

rappresenta l'associazione tra un terminale e le relative impostazioni di configurazione.

</dd> <dt>

[**Account \_ TS Win32**](win32-tsaccount.md)
</dt> <dd>

consente l'eliminazione di un account esistente nel [**\_ terminale Win32**](win32-terminal.md) e la modifica delle autorizzazioni esistenti.

</dd> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> <dd>

definisce le impostazioni di configurazione per la [**classe \_ Terminale Win32**](win32-terminal.md) correlata ai criteri di connessione.

</dd> <dt>

[**Win32 \_ TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

Fornisce informazioni dettagliate sul server licenze Desktop remoto individuato.

</dd> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> <dd>

definisce le impostazioni di configurazione per la classe [**\_ Terminale Win32,**](win32-terminal.md) inclusi i criteri di programma iniziali.

</dd> <dt>

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> <dd>

rappresenta le impostazioni generali del terminale, ad esempio il livello di crittografia e il protocollo di trasporto.

</dd> <dt>

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> <dd>

definisce le impostazioni di configurazione per la [**classe \_ Terminale Win32**](win32-terminal.md) correlata all'accesso client.

</dd> <dt>

[**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

enumera l'elenco di schede di rete che possono essere configurate per un [**\_ terminale Win32,**](win32-terminal.md)in base al protocollo terminale e al metodo di trasporto specificati.

</dd> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> <dd>

definisce varie impostazioni di configurazione per la [**classe \_ Terminale Win32,**](win32-terminal.md) incluse le proprietà correlate alla scheda di rete e il numero massimo di connessioni consentite.

</dd> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> <dd>

include un metodo per aggiungere nuovi account al terminale e un metodo per ripristinare le autorizzazioni predefinite in un terminale.

</dd> <dt>

[**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md)
</dt> <dd>

definisce le impostazioni di configurazione del controllo remoto per la [**classe \_ Terminale Win32.**](win32-terminal.md)

</dd> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dd>

Definisce le Connessione Desktop remoto di configurazione di Gestore connessione Desktop remoto per la [**classe \_ Win32 TSSessionDirectorySetting.**](win32-tssessiondirectorysetting.md)

</dd> <dt>

[**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md)
</dt> <dd>

Rappresenta l'associazione tra un'istanza della [**classe \_ TerminalService Win32**](win32-terminalservice.md) e un'istanza della [**classe \_ TSSessionDirectory Win32.**](win32-tssessiondirectory.md)

</dd> <dt>

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> <dd>

definisce le impostazioni di configurazione per la [**classe \_ Terminale Win32,**](win32-terminal.md) ad esempio i limiti di tempo e le azioni di disconnessione e riconnessione.

</dd> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> <dd>

Definisce le impostazioni di virtualizzazione IP (Internet Protocol) per un server Host sessione Desktop remoto.

</dd> <dt>

[**Win32 \_ TSVirtualIPSetting**](win32-tsvirtualipsetting.md)
</dt> <dd>

Rappresenta l'associazione tra [**una classe di elementi \_ TerminalService Win32**](win32-terminalservice.md) e una classe di impostazione [**\_ TSVirtualIP Win32.**](win32-tsvirtualip.md)

</dd> </dl>

Nella figura seguente vengono illustrate le relazioni tra queste classi.

![le relazioni tra le classi supportate](images/tswmi.png)

 

 