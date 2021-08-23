---
description: Il Windows Installer ridistribuibile è un pacchetto di aggiornamento software.
ms.assetid: 8491dfa6-b9be-4e37-8a61-a405c8eb0ab0
title: Componenti ridistribuibili di Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 831abe9a19f8b2d4999229b1d40e701c5869aa79e6dda9f0933ab8117656652b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526701"
---
# <a name="windows-installer-redistributables"></a>Componenti ridistribuibili di Windows Installer

Windows Il programma di installazione 4.5 e versioni precedenti è disponibile come pacchetto di aggiornamento software ridistribuibile. Vedere la sezione [Versioni rilasciate di Windows installer](released-versions-of-windows-installer.md) per determinare quali prodotti sono stati spediti al programma Windows programma di installazione. Il pacchetto di aggiornamento ridistribuibile per una versione viene reso disponibile dopo il rilascio del prodotto fornito con una versione specifica Windows programma di installazione.

> [!NOTE]
> Non è disponibile alcun ridistribuibile per Windows Installer 5.0. Questa versione è inclusa con il sistema operativo in Windows 7, Windows Server 2008 R2 e versioni client e server successive (incluso Windows 10).

## <a name="obtaining-the-windows-installer-redistributable-45-and-earlier"></a>Recupero di Windows Installer Redistributable (4.5 e versioni precedenti)

-   Tutti i componenti ridistribuibili Windows Installer disponibili sono disponibili [nell'Area download Microsoft.](https://www.microsoft.com/Downloads/)
-   Il download per il pacchetto [Windows Installer 4.5 Redistributable è](https://support.microsoft.com/kb/942288) disponibile all'indirizzo: https://go.microsoft.com/fwlink/p/?LinkID=101159 .
-   Il nome del ridistribuibile che installa Windows Installer 4.5 nei computer basati su x86 che eseguono Windows Vista, Windows Vista con Service Pack 1 (SP1) e Windows Server 2008 è Windows6.0-KB942288-v2-x86.MSU.
-   Il nome del ridistribuibile che installa Windows Installer 4.5 nei computer basati su x64 che eseguono Windows Vista, Windows Vista con SP1 e Windows Server 2008 è Windows6.0-KB942288-v2-x64.MSU.
-   Il nome del ridistribuibile che installa Windows Installer 4.5 nei computer Itanium-Based Systems che eseguono Windows Vista, Windows Vista con SP1 e Windows Server 2008 è Windows6.0-KB942288-v2-ia64.MSU.
-   Il nome del ridistribuibile che installa Windows Installer 4.5 nei computer basati su x86 che eseguono Windows XP con Service Pack 2 (SP2) e Windows XP con Service Pack 3 (SP3) è WindowsXP-KB942288-v3-x86.exe.
-   Il nome del ridistribuibile che installa Windows Installer 4.5 nei computer basati su x86 che eseguono Windows Server 2003 con Service Pack 1 (SP1) e Windows Server 2003 con Service Pack 2 (SP2) è WindowsServer2003-KB942288-v4-x86.exe.
-   Il nome del ridistribuibile che installa Windows Installer 4.5 nei computer basati su x64 che eseguono Windows Server 2003 con SP1 e Windows Server 2003 con SP2 è WindowsServer2003-KB942288-v4-x64.exe.
-   Il nome del ridistribuibile che installa Windows Installer 4.5 nei computer Itanium-Based Systems che eseguono Windows Server 2003 con SP1 e Windows Server 2003 con SP2 è WindowsServer2003-KB942288-v4-ia64.exe.
-   Non è disponibile alcun componente ridistribuibile che Windows Installer 4.0. Questa versione del programma di installazione Windows viene fornita con Windows Vista.
-   Il nome del ridistribuibile che installa Windows Installer 3.1 è WindowsInstaller-KB893803-v2-x86.exe. Il download per il [pacchetto Windows Installer 3.1 Redistributable (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c) è disponibile all'indirizzo: https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c .
    > [!Note]  
    > Se è stato eseguito l'aggiornamento a Windows Installer 3.1 installando Windows Server 2003 con SP1 o una versione precedente di questo ridistribuibile, potrebbe essere necessario installare anche l'aggiornamento per [Windows Server 2003 Service Pack 1 (KB898715)](https://www.microsoft.com/downloads/details.aspx?FamilyID=8b4e6b93-1886-4d47-a18d-35581c42eca0) per ottenere tutti gli aggiornamenti disponibili in [Windows Installer 3.1 Redistributable (v2).](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c)

     

-   Il componente ridistribuibile che Windows Installer 3.0 è WindowsInstaller-KB884016-v2-x86.exe. Il download per Windows [Installer 3.0 Redistributable](https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8) è disponibile all'indirizzo: https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8 .
-   Il Windows Installer 2.0 usava una convenzione di denominazione precedente per il ridistribuibile: [Instmsi.exe](instmsi-exe.md). Il componente ridistribuibile per l'installazione o l'aggiornamento a Windows Installer 2.0 in Windows 2000 non deve essere usato per installare o aggiornare Windows Installer 2.0 in Windows Server 2003 e Windows XP.

    Il download per [Windows Installer 2.0 Redistributable per Windows NT 4.0 e Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f) è disponibile all'indirizzo https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f .

## <a name="installing-the-windows-installer-redistributable-45-and-earlier"></a>Installazione di Windows Installer Redistributable (4.5 e versioni precedenti)

Il programma di installazione di Windows 4.5 ridistribuibile viene fornito per i sistemi operativi Windows Vista e Windows Server 2008 come file con estensione msu e deve essere installato usando il programma di installazione autonomo di [Windows Update](https://support.microsoft.com/kb/934307/) (Wusa.exe).

È possibile installare Windows Installer 4.5 Redistributable per i sistemi operativi Windows XP e Windows Server 2003 usando la sintassi e le opzioni della riga di comando seguenti.

I componenti Windows Installer 3.1 e Windows Installer 3.0 possono essere installati usando la sintassi e le opzioni della riga di comando seguenti.

### <a name="syntax"></a>Sintassi

Usare la sintassi seguente per installare i componenti ridistribuibili per Windows Installer 4.5 in Windows XP e Windows Server 2003.

```CMD
<Name of the Redistributable>\[<options>\]*
```

### <a name="command-line-options"></a>Opzioni della riga di comando

I Windows di aggiornamento software ridistribuibile del programma di installazione di windows usano le opzioni della riga di comando seguenti senza distinzione tra maiuscole e minuscole.



| Opzione     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /norestart | Impedisce al pacchetto ridistribuibile di chiedere all'utente di riavviare il sistema anche se è stato necessario sostituire i file in uso durante l'installazione. Se il pacchetto di aggiornamento viene richiamato con questa opzione, restituisce **ERROR \_ SUCCESS REBOOT \_ \_ REQUIRED** se è stato necessario sostituire i file in uso.<br/> Se non è stato necessario sostituire i file in uso, restituisce **ERROR \_ SUCCESS**. Per altre informazioni sui riavvii ritardati, vedere la sezione osservazioni.<br/> |
| /quiet     | Per l'uso da parte di applicazioni che ridistribuino Windows programma di installazione come parte di un'applicazione di bootstrap. Un'interfaccia utente non viene presentata all'utente. L'applicazione di bootstrap deve controllare il codice restituito per determinare se è necessario un riavvio per completare l'installazione del Windows installazione.<br/>                                                                                                                                                |
| /help      | Visualizza la Guida per tutte le opzioni disponibili.                                                                                                                                                                                                                                                                                                                                                                                                                                     |

### <a name="delayed-restart-on-windows-vista-and-windows-server-2008"></a>Riavvio ritardato Windows Vista e Windows Server 2008

L'opzione della riga di comando /norestart impedisce wusa.exe riavvio del computer. Tuttavia, se un file aggiornato dal pacchetto MSU è in uso, il pacchetto non viene applicato al computer fino a quando l'utente non riavvia il computer. Ciò significa che le applicazioni che usano Windows Installer 4.5 Redistributable per Windows Vista e Windows Server 2008 non possono usare la funzionalità Windows Installer 4.5 fino al riavvio del computer.

### <a name="delayed-restart-on-windows-xp-and-windows-server-2003"></a>Riavvio ritardato Windows XP e Windows Server 2003

È consigliabile che il Windows Installer sia arrestato quando si usa il pacchetto di aggiornamento. Quando il pacchetto viene eseguito in modalità interfaccia utente completa, rileva se il servizio Windows Installer è in esecuzione e richiede all'utente di arrestare il servizio. Se l'utente continua senza arrestare il servizio, l'aggiornamento sostituisce Windows programma di installazione.

[Il bootstrap di](bootstrapping.md) applicazioni che usano il pacchetto ridistribuibile per installare il programma di installazione di Windows con un'altra applicazione può richiedere un riavvio del sistema aggiuntivo oltre ai riavvii necessari per installare l'applicazione. L'opzione di riavvio ritardato è consigliata solo nei casi in cui è necessario eliminare un riavvio aggiuntivo causato dall'installazione di file in uso. Gli sviluppatori devono eseguire le operazioni seguenti nell'applicazione di configurazione per usare l'opzione di riavvio ritardato.

-   Chiamare il pacchetto ridistribuibile con l'opzione della riga di comando /norestart.
-   Considerare la restituzione di **ERROR \_ SUCCESS o** ERROR SUCCESS REBOOT **\_ \_ \_ REQUIRED** come operazione riuscita.
-   Richiamare Msiexec nel pacchetto dell'applicazione ed eseguire altro codice di installazione specifico dell'applicazione. Se l'applicazione di installazione [**usa MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), l'applicazione deve caricare MSI.DLL dalla directory di sistema. Se non si verifica alcun riavvio e se il ridistribuibile ha restituito **ERROR \_ SUCCESS REBOOT \_ \_ REQUIRED**, richiedere all'utente un riavvio per completare l'installazione dei file binari del programma di installazione di Windows. Se si verifica un riavvio, non sono necessari passaggi aggiuntivi.
    > [!Note]  
    > Le applicazioni che chiamano [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) sul nuovo MSI.DLL dopo la riuscita del pacchetto ridistribuibile devono garantire che una versione precedente di MSI.DLL non sia già stata caricata all'interno del processo. Se è stata caricata una versione precedente di MSI.DLL, deve essere scaricata dallo spazio degli indirizzi del processo prima di chiamare **LoadLibrary** per il nuovo MSI.DLL.

     

Per altre informazioni, vedere [l'Windows bootstrap del programma di installazione.](windows-installer-bootstrapping.md)

 

 
