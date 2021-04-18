---
description: Il controllo dell'account utente influiscono sui dati WMI restituiti da uno strumento da riga di comando, accesso remoto e su come devono essere eseguiti gli script. Per ulteriori informazioni su UAC, vedere Introduzione con controllo dell'account utente.
ms.assetid: f6840aaa-834b-42c8-b641-01c570078fcb
ms.tgt_platform: multiple
title: Controllo dell'account utente e WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 39d48abcffa537d886397092c6d4a7b558825021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315187"
---
# <a name="user-account-control-and-wmi"></a>Controllo dell'account utente e WMI

Il controllo dell'account utente influiscono sui dati WMI restituiti da uno strumento da riga di comando, accesso remoto e su come devono essere eseguiti gli script. Per ulteriori informazioni su UAC, vedere [Introduzione con controllo dell'account utente](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

Le sezioni seguenti descrivono la funzionalità controllo dell'account utente:

-   [Controllo dell'account utente](#user-account-control-and-wmi)
-   [Account necessario per l'esecuzione di strumenti di Command-Line WMI](#account-needed-to-run-wmi-command-line-tools)
-   [Gestione delle connessioni remote in controllo dell'account utente](#handling-remote-connections-under-uac)
-   [Effetto UAC sui dati WMI restituiti a script o applicazioni](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [Argomenti correlati](#related-topics)

## <a name="user-account-control"></a>Controllo dell'account utente

In controllo dell'account utente, gli account nel gruppo Administrators locale hanno due [*token di accesso*](/windows/desktop/SecGloss/a-gly), uno con privilegi utente standard e uno con privilegi di amministratore. A causa del filtraggio dei token di accesso del controllo dell'account utente, uno script viene in genere eseguito con il token utente standard, a meno che non venga eseguito "come amministratore" in modalità privilegi elevati. Non tutti gli script richiedono privilegi amministrativi.

Gli script non possono determinare a livello di codice se sono in esecuzione con un token di sicurezza utente standard o un token di amministratore. Lo script potrebbe non riuscire con un errore di accesso negato. Se lo script richiede privilegi di amministratore, è necessario eseguirlo in modalità con privilegi elevati. L'accesso agli spazi dei nomi WMI varia a seconda che lo script venga eseguito in modalità con privilegi elevati. Per alcune operazioni WMI, ad esempio il recupero di dati o l'esecuzione della maggior parte dei metodi, non è necessario che l'account venga eseguito come amministratore. Per ulteriori informazioni sulle autorizzazioni di accesso predefinite, vedere [accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md) ed [esecuzione di operazioni con privilegi](executing-privileged-operations.md).

A causa del controllo dell'account utente, l'account che esegue lo script deve appartenere al gruppo Administrators nel computer locale per poter essere eseguito con diritti elevati.

È possibile eseguire uno script o un'applicazione con diritti elevati eseguendo uno dei metodi seguenti:

**Per eseguire uno script in modalità con privilegi elevati**

1.  Aprire una finestra del prompt dei comandi facendo clic con il pulsante destro del mouse sul prompt dei comandi nel menu Start e scegliendo **Esegui come amministratore**.
2.  Pianificare lo script per l'esecuzione con privilegi elevati utilizzando Utilità di pianificazione. Per ulteriori informazioni, vedere [contesti di sicurezza per l'esecuzione di attività](/windows/desktop/TaskSchd/security-contexts-for-running-tasks).
3.  Eseguire lo script utilizzando l'account Administrator predefinito.

## <a name="account-needed-to-run-wmi-command-line-tools"></a>Account necessario per l'esecuzione di strumenti di Command-Line WMI

Per eseguire gli [strumenti di Command-Line WMI](wmi-command-line-tools.md)seguenti, l'account deve appartenere al gruppo Administrators e lo strumento deve essere eseguito da un prompt dei comandi con privilegi elevati. L'account Administrator predefinito può inoltre eseguire questi strumenti.

-   [**mofcomp**](mofcomp.md)

-   [**wmic**](wmic.md)

    La prima volta che si esegue WMIC dopo l'installazione del sistema, è necessario eseguirlo da un prompt dei comandi con privilegi elevati. La modalità con privilegi elevati potrebbe non essere necessaria per le successive esecuzioni di WMIC, a meno che le operazioni WMI non richiedano privilegi di amministratore.

-   [**winmgmt**](winmgmt.md)

-   [**wmiadap**](wmiadap.md)

Per eseguire il [*controllo WMI*](gloss-w.md) (wmimgmt. msc) e apportare modifiche alla sicurezza o alle impostazioni di controllo dello spazio dei nomi WMI, è necessario che l'account disponga del diritto modifica sicurezza esplicitamente concesso o che si trovi nel gruppo Administrators locale. L'account Administrator predefinito può anche modificare la sicurezza o il controllo per uno spazio dei nomi.

Wbemtest.exe, uno strumento da riga di comando non supportato dal servizio supporto tecnico clienti Microsoft, può essere eseguito da account non inclusi nel gruppo Administrators locale, a meno che un'operazione specifica non richieda privilegi normalmente concessi agli account amministratore.

## <a name="handling-remote-connections-under-uac"></a>Gestione delle connessioni remote in controllo dell'account utente

Se si sta effettuando la connessione a un computer remoto in un dominio o in un gruppo di lavoro, determina se si verifica il filtro UAC.

Se il computer fa parte di un dominio, connettersi al computer di destinazione utilizzando un account di dominio appartenente al gruppo Administrators locale del computer remoto. Il filtro dei token di accesso del controllo dell'account utente non influirà sugli account di dominio del gruppo Administrators locale. Non usare un account locale non di dominio nel computer remoto, anche se l'account si trova nel gruppo Administrators.

In un gruppo di lavoro, l'account che si connette al computer remoto è un utente locale del computer. Anche se l'account si trova nel gruppo Administrators, il filtro UAC indica che uno script viene eseguito come utente standard. Una procedura consigliata consiste nel creare un account utente o un gruppo di utenti locale dedicato nel computer di destinazione in modo specifico per le connessioni remote.

Per poter usare questo account, è necessario modificare la sicurezza perché l'account non dispone mai di privilegi amministrativi. Assegnare all'utente locale:

-   Avvio remoto e attivazione dei diritti per accedere a DCOM. Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).
-   Diritti di accesso allo spazio dei nomi WMI in modalità remota (abilitazione remota). Per ulteriori informazioni, vedere [accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).
-   Diritto di accedere all'oggetto a protezione diretta specifico, a seconda della sicurezza richiesta dall'oggetto.

Se si usa un account locale, perché si è in un gruppo di lavoro o è un account computer locale, è possibile che venga richiesto di assegnare attività specifiche a un utente locale. Ad esempio, è possibile concedere all'utente il diritto di arrestare o avviare un servizio specifico tramite il comando SC.exe, i metodi [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) e [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service)oppure tramite criteri di gruppo con gpedit. msc. Alcuni oggetti a protezione diretta potrebbero non consentire a un utente standard di eseguire attività e non offrire alcun mezzo per modificare la sicurezza predefinita. In questo caso, potrebbe essere necessario disabilitare UAC in modo che l'account utente locale non venga filtrato e diventi invece un amministratore completo. Tenere presente che, per motivi di sicurezza, la disabilitazione del controllo dell'account utente deve essere l'ultima risorsa.

Disabilitare il controllo dell'account utente remoto modificando la voce del registro di sistema che controlla l'UAC remoto non è consigliabile, ma potrebbe essere necessario in un gruppo di lavoro. La voce del registro di sistema è **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy**. Quando il valore di questa voce è zero (0), il filtro dei token di accesso remoto UAC è abilitato. Quando il valore è 1, il controllo dell'account utente remoto è disabilitato.

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a>Effetto UAC sui dati WMI restituiti a script o applicazioni

Se uno script o un'applicazione è in esecuzione con un account nel gruppo Administrators, ma non con privilegi elevati, è possibile che non si ottengano tutti i dati restituiti perché questo account viene eseguito come utente standard. I [*provider*](gloss-p.md) WMI per alcune classi non restituiscono tutte le istanze a un account utente standard o a un account amministratore che non è in esecuzione come amministratore completo a causa del filtraggio del controllo dell'account utente.

Le classi seguenti non restituiscono alcune istanze quando l'account viene filtrato in base all'UAC:

-   [**\_Bus Win32**](/windows/desktop/CIMWin32Prov/win32-bus)
-   [**\_Stampante Win32**](/windows/desktop/CIMWin32Prov/win32-printer)
-   [**\_ComponentCategory Win32**](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [**\_LogicalProgramGroupItem Win32**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [**\_LogicalProgramGroup Win32**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [**\_NetworkConnection Win32**](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [**\_AccountUtente Win32**](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [**\_PrinterDriver Win32**](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [**\_PortResource Win32**](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [**\_DeviceMemoryAddress Win32**](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

Quando l'account viene filtrato in base all'UAC, le classi seguenti non restituiscono alcune proprietà:

-   [**\_NetworkAdapterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [**\_DCOMApplicationSetting Win32**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [**\_DCOMApplication Win32**](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [**\_Battiscopa Win32**](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [**\_ComputerSystem Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [**\_NetworkAdapter Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [**\_MotherboardDevice Win32**](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [**\_DiskDrive Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [**\_PnPEntity Win32**](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [**\_VideoController Win32**](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [**\_ParallelPort Win32**](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [**\_Disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [**\_SystemDriver Win32**](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [**\_IRQResource Win32**](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [**\_NetworkProtocol Win32**](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> <dt>

[Accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md)
</dt> <dt>

[Modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
