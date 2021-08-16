---
description: Controllo dell'account utente influisce sui dati WMI restituiti da uno strumento da riga di comando, sull'accesso remoto e sulla modalità di esecuzione degli script. Per altre informazioni sul controllo dell'account utente, Attività iniziali controllo dell'account utente.
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
ms.openlocfilehash: 2da001117fa75ccef737647038d3e58b942f666ba40e1fd14ec98cb4ebdd44af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553317"
---
# <a name="user-account-control-and-wmi"></a>Controllo dell'account utente e WMI

Controllo dell'account utente influisce sui dati WMI restituiti da uno strumento da riga di comando, sull'accesso remoto e sulla modalità di esecuzione degli script. Per altre informazioni sul controllo dell'account utente, [Attività iniziali controllo dell'account utente.](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)

Le sezioni seguenti descrivono la funzionalità controllo dell'account utente:

-   [Controllo dell'account utente](#user-account-control-and-wmi)
-   [Account necessario per eseguire wmi Command-Line Tools](#account-needed-to-run-wmi-command-line-tools)
-   [Gestione delle connessioni remote in Controllo dell'account utente](#handling-remote-connections-under-uac)
-   [Effetto di Controllo dell'account utente sui dati WMI restituiti a script o applicazioni](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [Argomenti correlati](#related-topics)

## <a name="user-account-control"></a>Controllo dell'account utente

In Controllo dell'account utente gli account nel gruppo Administrators locale hanno due [*token*](/windows/desktop/SecGloss/a-gly)di accesso, uno con privilegi utente standard e uno con privilegi di amministratore. A causa del filtro dei token di accesso di Controllo dell'account utente, uno script viene in genere eseguito con il token utente standard, a meno che non venga eseguito "come amministratore" in modalità con privilegi elevati. Non tutti gli script hanno richiesto privilegi amministrativi.

Gli script non possono determinare a livello di codice se vengono eseguiti con un token di sicurezza utente standard o un token amministratore. Lo script potrebbe non riuscire con un errore di accesso negato. Se lo script richiede privilegi di amministratore, deve essere eseguito in modalità con privilegi elevati. L'accesso agli spazi dei nomi WMI varia a seconda che lo script sia eseguito in modalità con privilegi elevati. Alcune operazioni WMI, ad esempio il recupero dei dati o l'esecuzione della maggior parte dei metodi, non richiedono l'esecuzione dell'account come amministratore. Per altre informazioni sulle autorizzazioni di accesso predefinite, vedere [Accesso agli spazi](access-to-wmi-namespaces.md) dei nomi WMI ed Esecuzione di operazioni con [privilegi.](executing-privileged-operations.md)

A causa di Controllo account utente, l'account che esegue lo script deve essere nel gruppo Administrators del computer locale per poter essere eseguito con diritti elevati.

È possibile eseguire uno script o un'applicazione con diritti elevati eseguendo uno dei metodi seguenti:

**Per eseguire uno script in modalità con privilegi elevati**

1.  Aprire una finestra del prompt dei comandi facendo clic con il pulsante destro del mouse su Prompt dei menu Start e quindi scegliendo **Esegui come amministratore**.
2.  Pianificare l'esecuzione con privilegi elevati dello script usando Utilità di pianificazione. Per altre informazioni, vedere [Contesti di sicurezza per l'esecuzione di attività.](/windows/desktop/TaskSchd/security-contexts-for-running-tasks)
3.  Eseguire lo script usando l'account Administrator predefinito.

## <a name="account-needed-to-run-wmi-command-line-tools"></a>Account necessario per eseguire strumenti di Command-Line WMI

Per eseguire gli strumenti [WMI Command-Line ,](wmi-command-line-tools.md)l'account deve essere nel gruppo Administrators e lo strumento deve essere eseguito da un prompt dei comandi con privilegi elevati. Questi strumenti possono essere eseguiti anche dall'account amministratore predefinito.

-   [**mofcomp**](mofcomp.md)

-   [**wmic**](wmic.md)

    La prima volta che si esegue Wmic dopo l'installazione del sistema, è necessario eseguirlo da un prompt dei comandi con privilegi elevati. La modalità con privilegi elevati potrebbe non essere necessaria per le esecuzioni successive di Wmic, a meno che le operazioni WMI non richiedano privilegi di amministratore.

-   [**Winmgmt**](winmgmt.md)

-   [**wmiadap**](wmiadap.md)

Per eseguire il controllo [*WMI*](gloss-w.md) (Wmimgmt.msc) e apportare modifiche alle impostazioni di sicurezza o controllo dello spazio dei nomi WMI, l'account deve disporre del diritto Modifica sicurezza concesso in modo esplicito o essere nel gruppo Administrators locale. L'account Administrator predefinito può anche modificare la sicurezza o il controllo per uno spazio dei nomi.

Wbemtest.exe, uno strumento da riga di comando non supportato dal Servizio Supporto Tecnico Clienti Microsoft, può essere eseguito da account non presenti nel gruppo Administrators locale, a meno che un'operazione specifica non richieda privilegi normalmente concessi agli account amministratore.

## <a name="handling-remote-connections-under-uac"></a>Gestione delle connessioni remote in Controllo dell'account utente

Se ci si connette a un computer remoto in un dominio o in un gruppo di lavoro, determina se viene eseguito il filtro di Controllo dell'account utente.

Se il computer fa parte di un dominio, connettersi al computer di destinazione usando un account di dominio che si trova nel gruppo Administrators locale del computer remoto. Il filtro dei token di accesso di Controllo dell'account utente non influirà quindi sugli account di dominio nel gruppo Administrators locale. Non usare un account locale non di dominio nel computer remoto, anche se l'account è nel gruppo Administrators.

In un gruppo di lavoro l'account che si connette al computer remoto è un utente locale in tale computer. Anche se l'account è nel gruppo Administrators, il filtro di Controllo dell'account utente indica che uno script viene eseguito come utente standard. Una procedura consigliata consiste nel creare un gruppo di utenti locale dedicato o un account utente nel computer di destinazione in modo specifico per le connessioni remote.

La sicurezza deve essere modificata per poter usare questo account perché l'account non ha mai avuto privilegi amministrativi. Assegnare all'utente locale:

-   Diritti di avvio remoto e attivazione per accedere a DCOM. Per altre informazioni, vedere [Connessione a WMI in un computer remoto.](connecting-to-wmi-on-a-remote-computer.md)
-   Diritti per accedere allo spazio dei nomi WMI in modalità remota (Abilita remoto). Per altre informazioni, vedere [Accesso agli spazi dei nomi WMI.](access-to-wmi-namespaces.md)
-   Diritto di accedere all'oggetto a protezione diretta specifico, a seconda della sicurezza richiesta dall'oggetto.

Se si usa un account locale, perché si fa parte di un gruppo di lavoro o si tratta di un account del computer locale, potrebbe essere necessario assegnare attività specifiche a un utente locale. Ad esempio, è possibile concedere all'utente il diritto di arrestare o avviare un servizio specifico tramite il comando SC.exe, i metodi [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) e [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) del servizio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service)o tramite Criteri di gruppo tramite Gpedit.msc. Alcuni oggetti a protezione diretta potrebbero non consentire a un utente standard di eseguire attività e non offrire alcun mezzo per modificare la sicurezza predefinita. In questo caso, potrebbe essere necessario disabilitare controllo dell'account utente in modo che l'account utente locale non venga filtrato e diventi invece un amministratore completo. Tenere presente che, per motivi di sicurezza, la disabilitazione di Controllo dell'account utente deve essere un'ultima risorsa.

La disabilitazione di Controllo dell'account utente remoto modificando la voce del Registro di sistema che controlla Controllo dell'account utente remoto non è consigliata, ma potrebbe essere necessaria in un gruppo di lavoro. La voce del Registro di sistema **è HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **system** \\ **LocalAccountTokenFilterPolicy**. Quando il valore di questa voce è zero (0), il filtro dei token di accesso di Controllo dell'account utente remoto è abilitato. Quando il valore è 1, controllo dell'account utente remoto è disabilitato.

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a>Effetto di Controllo dell'account utente sui dati WMI restituiti a script o applicazioni

Se uno script o un'applicazione è in esecuzione con un account nel gruppo Administrators, ma non con privilegi elevati, è possibile che non si otterrà tutti i dati restituiti perché l'account è in esecuzione come utente standard. I provider WMI [*per*](gloss-p.md) alcune classi non restituiscono tutte le istanze a un account utente standard o a un account amministratore che non è in esecuzione come amministratore completo a causa del filtro di Controllo dell'account utente.

Le classi seguenti non restituiscono alcune istanze quando l'account viene filtrato in base al controllo dell'account utente:

-   [**Win32 \_ Bus**](/windows/desktop/CIMWin32Prov/win32-bus)
-   [**Stampante \_ Win32**](/windows/desktop/CIMWin32Prov/win32-printer)
-   [**Win32 \_ ComponentCategory**](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [**Win32 \_ LogicalProgramGroupItem**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [**Win32 \_ LogicalProgramGroup**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [**Connessione di rete Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [**Account utente \_ Win32**](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [**Win32 \_ PrinterDriver**](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [**Win32 \_ PortResource**](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [**Win32 \_ DeviceMemoryAddress**](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

Le classi seguenti non restituiscono alcune proprietà quando l'account viene filtrato in base al controllo dell'account utente:

-   [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [**Win32 \_ DCOMApplication**](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [**Win32 \_ Baseboard**](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [**Scheda madre \_ Win32Device**](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [**Win32 \_ VideoController**](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [**Win32 \_ ParallelPort**](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [**Disco logico \_ Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [**Risorsa \_ IRQ Win32**](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [**Win32 \_ NetworkProtocol**](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> <dt>

[Accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md)
</dt> <dt>

[Modifica della sicurezza dell'accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
