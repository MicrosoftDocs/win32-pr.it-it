---
description: Il Windows Installer ridistribuibile è un pacchetto di aggiornamento software.
ms.assetid: 8491dfa6-b9be-4e37-8a61-a405c8eb0ab0
title: Componenti ridistribuibili di Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 9fc175a96ae1d2daed9798981b0dbe679505975e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313782"
---
# <a name="windows-installer-redistributables"></a>Componenti ridistribuibili di Windows Installer

Windows Installer 4,5 e versioni precedenti è disponibile come pacchetto di aggiornamento software ridistribuibile. Vedere la sezione [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md) per determinare quali prodotti hanno fornito versioni del Windows Installer. Il pacchetto di aggiornamento ridistribuibile per una versione viene reso disponibile dopo il rilascio del prodotto fornito con una specifica versione di Windows Installer.

> [!NOTE]
> Non è disponibile alcun componente ridistribuibile per Windows Installer 5,0. Questa versione è inclusa nel sistema operativo in Windows 7, Windows Server 2008 R2 e versioni successive di client e server (incluso Windows 10).

## <a name="obtaining-the-windows-installer-redistributable-45-and-earlier"></a>Recupero del Windows Installer ridistribuibile (4,5 e versioni precedenti)

-   È possibile trovare tutti i Windows Installer ridistribuibili disponibili nell' [area download Microsoft](https://www.microsoft.com/Downloads/).
-   Il download per il [pacchetto ridistribuibile Windows Installer 4,5](https://support.microsoft.com/kb/942288) è disponibile all'indirizzo: https://go.microsoft.com/fwlink/p/?LinkID=101159 .
-   Il nome del file ridistribuibile che installa Windows Installer 4,5 in computer basati su x86 che eseguono Windows Vista, Windows Vista con Service Pack 1 (SP1) e Windows Server 2008 è Windows 6.0-KB942288-v2-x86. MSU.
-   Il nome del file ridistribuibile che installa Windows Installer 4,5 in computer basati su x64 che eseguono Windows Vista, Windows Vista con SP1 e Windows Server 2008 è Windows 6.0-KB942288-v2-x64. MSU.
-   Il nome del file ridistribuibile che installa Windows Installer 4,5 nei computer dei sistemi Itanium-Based in cui viene eseguito Windows Vista, Windows Vista con SP1 e Windows Server 2008 è Windows 6.0-KB942288-v2-ia64. MSU.
-   Il nome del file ridistribuibile che installa Windows Installer 4,5 in computer basati su x86 che eseguono Windows XP con Service Pack 2 (SP2) e Windows XP con Service Pack 3 (SP3) è WindowsXP-KB942288-v3-x86.exe.
-   Il nome del file ridistribuibile che installa Windows Installer 4,5 in computer basati su x86 che eseguono Windows Server 2003 con Service Pack 1 (SP1) e Windows Server 2003 con Service Pack 2 (SP2) è WindowsServer2003-KB942288-v4-x86.exe.
-   Il nome del file ridistribuibile che installa Windows Installer 4,5 in computer basati su x64 che eseguono Windows Server 2003 con SP1 e Windows Server 2003 con SP2 è WindowsServer2003-KB942288-v4-x64.exe.
-   Il nome del file ridistribuibile che installa Windows Installer 4,5 nei computer dei sistemi Itanium-Based in cui è in esecuzione Windows Server 2003 con SP1 e Windows Server 2003 con SP2 è WindowsServer2003-KB942288-v4-ia64.exe.
-   Non è disponibile alcun componente ridistribuibile che installa Windows Installer 4,0. Questa versione di Windows Installer viene fornita con Windows Vista.
-   Il nome del file ridistribuibile che installa Windows Installer 3,1 è WindowsInstaller-KB893803-v2-x86.exe. Il download per il pacchetto [ridistribuibile di Windows Installer 3,1 (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c) è disponibile all'indirizzo: https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c .
    > [!Note]  
    > Se è stato eseguito l'aggiornamento a Windows Installer 3,1 installando Windows Server 2003 con SP1 o una versione precedente di questo ridistribuibile, potrebbe essere necessario installare anche l' [aggiornamento per Windows server 2003 Service Pack 1 (KB898715)](https://www.microsoft.com/downloads/details.aspx?FamilyID=8b4e6b93-1886-4d47-a18d-35581c42eca0) per ottenere tutti gli aggiornamenti disponibili in [Windows Installer 3,1 Redistributable (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c).

     

-   Il ridistribuibile che installa Windows Installer 3,0 è WindowsInstaller-KB884016-v2-x86.exe. Il download per la [Windows Installer 3,0 ridistribuibile](https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8) è disponibile all'indirizzo: https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8 .
-   Il Windows Installer 2,0 usava una convenzione di denominazione precedente per il ridistribuibile: [Instmsi.exe](instmsi-exe.md). Il ridistribuibile per l'installazione o l'aggiornamento a Windows Installer 2,0 in Windows 2000 non deve essere utilizzato per installare o aggiornare Windows Installer 2,0 in Windows Server 2003 e Windows XP.

    Il download per la [Windows Installer 2,0 Redistributable per Windows NT 4,0 e windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f) è disponibile all'indirizzo https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f .

## <a name="installing-the-windows-installer-redistributable-45-and-earlier"></a>Installazione del Windows Installer ridistribuibile (4,5 e versioni precedenti)

Il Windows Installer 4,5 resdistributable viene fornito per i sistemi operativi Windows Vista e Windows Server 2008 come file con estensione msu e deve essere installato tramite il [programma di installazione autonomo di Windows Update](https://support.microsoft.com/kb/934307/) (Wusa.exe).

I sistemi operativi Windows Installer 4,5 Redistributable per Windows XP e Windows Server 2003 possono essere installati utilizzando la sintassi della riga di comando e le opzioni seguenti.

I ridistribuibili Windows Installer 3,1 e Windows Installer 3,0 possono essere installati utilizzando la sintassi della riga di comando e le opzioni seguenti.

### <a name="syntax"></a>Sintassi

Utilizzare la sintassi seguente per installare i ridistribuibili per Windows Installer 4,5 in Windows XP e Windows Server 2003.

```CMD
<Name of the Redistributable>\[<options>\]*
```

### <a name="command-line-options"></a>Opzioni della riga di comando

I pacchetti di aggiornamento software ridistribuibili Windows Installer utilizzano le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole.



| Opzione     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /norestart | Impedisce al pacchetto ridistribuibile di richiedere all'utente di riavviare il computer anche se è necessario sostituire i file in uso durante l'installazione. Se il pacchetto di aggiornamento viene richiamato con questa opzione, viene restituito l' **errore \_ operazione di \_ riavvio \_ necessario** se è necessario sostituire i file in uso.<br/> Se non è necessario sostituire i file in uso, viene restituito l' **errore \_ Success**. Per ulteriori informazioni sui riavvii ritardati, vedere la sezione Osservazioni.<br/> |
| /quiet     | Per l'uso da parte di applicazioni che ridistribuiscono il Windows Installer come parte di un'applicazione di bootstrap. Un'interfaccia utente (UI) non viene presentata all'utente. L'applicazione di bootstrap deve controllare il codice restituito per determinare se è necessario riavviare il computer per completare l'installazione del Windows Installer.<br/>                                                                                                                                                |
| /help      | Visualizza la guida su tutte le opzioni disponibili.                                                                                                                                                                                                                                                                                                                                                                                                                                     |

### <a name="delayed-restart-on-windows-vista-and-windows-server-2008"></a>Riavvio ritardato in Windows Vista e Windows Server 2008

L'opzione della riga di comando/norestart impedisce il riavvio del computer da parte di wusa.exe. Tuttavia, se un file aggiornato dal pacchetto MSU è in uso, il pacchetto non viene applicato al computer fino a quando l'utente non riavvia il computer. Ciò significa che le applicazioni che utilizzano la Windows Installer 4,5 ridistribuibile per Windows Vista e Windows Server 2008 non possono utilizzare la funzionalità Windows Installer 4,5 finché il computer non viene riavviato.

### <a name="delayed-restart-on-windows-xp-and-windows-server-2003"></a>Riavvio ritardato in Windows XP e Windows Server 2003

Quando si usa il pacchetto di aggiornamento, è consigliabile arrestare il servizio Windows Installer. Quando il pacchetto viene eseguito in modalità interfaccia utente completa, rileva se il servizio Windows Installer è in esecuzione e richiede all'utente di arrestare il servizio. Se l'utente continua senza arrestare il servizio, l'aggiornamento sostituisce Windows Installer.

Il [bootstrap](bootstrapping.md) di applicazioni che utilizzano il pacchetto ridistribuibile per installare il Windows Installer con un'altra applicazione può richiedere un riavvio del sistema aggiuntivo oltre ai riavvii necessari per installare l'applicazione. L'opzione di riavvio ritardato è consigliata solo nei casi in cui è necessario eliminare un riavvio aggiuntivo causato dall'installazione di file in uso. Gli sviluppatori devono eseguire le operazioni seguenti nell'applicazione di installazione per usare l'opzione di riavvio ritardato.

-   Chiamare il pacchetto ridistribuibile con l'opzione della riga di comando/norestart.
-   Considerare la restituzione di esito positivo **errore \_** o **errore \_ riavvio riuscito, \_ \_ necessario** come operazione riuscita.
-   Richiamare msiexec sul pacchetto dell'applicazione ed eseguire altro codice di installazione specifico dell'applicazione. Se l'applicazione di installazione usa [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), l'applicazione deve caricare MSI.DLL dalla directory di sistema. Se non si verifica alcun riavvio e se il ridistribuibile ha restituito un **errore di \_ \_ riavvio \_ necessario**, richiedere all'utente di riavviare il computer per completare l'installazione dei file binari Windows Installer. Se si verifica un riavvio, non sono necessari altri passaggi.
    > [!Note]  
    > Le applicazioni che chiamano [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) sul nuovo MSI.DLL dopo che il pacchetto ridistribuibile restituisce esito positivo devono garantire che una versione precedente di MSI.DLL non sia già stata caricata nel processo. Se è stata caricata una versione precedente di MSI.DLL, è necessario scaricarla dallo spazio degli indirizzi del processo prima di chiamare **LoadLibrary** per la nuova MSI.DLL.

     

Per ulteriori informazioni, vedere [Windows Installer bootstrap](windows-installer-bootstrapping.md).

 

 
