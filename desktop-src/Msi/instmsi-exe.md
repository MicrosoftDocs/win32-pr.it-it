---
description: Instmsi.exe è il pacchetto ridistribuibile per l'installazione di Windows Installer&\# 160; 2.0 e le versioni precedenti di Windows Installer. Vedere Windows Installer i ridistribuibili per i ridistribuibili per Windows Installer&\# 160; 3.0 e versioni successive.
ms.assetid: 74ea4530-3a73-4169-b0b7-f0272229192d
title: Instmsi.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 229d748cda68731627a6af2af992e321755b5ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317127"
---
# <a name="instmsiexe"></a>Instmsi.exe

Instmsi.exe è il pacchetto ridistribuibile per l'installazione di Windows Installer 2,0 e versioni precedenti di Windows Installer. Vedere [Windows Installer i ridistribuibili](windows-installer-redistributables.md) per i ridistribuibili per Windows Installer 3,0 e versioni successive.

Per ulteriori informazioni sulla versione del Windows Installer fornita con il sistema operativo, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).

Alcuni ridistribuibili non devono essere eseguiti in determinate versioni del sistema operativo. La tabella seguente descrive quali Instmsi sono compatibili con il sistema operativo in uso.



| Se Instmsi.exe installa questa versione di Windows Installer | Instmsi.exe può essere eseguito in questi sistemi operativi                    | Instmsi.exe non devono essere eseguiti in questi sistemi operativi                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Windows Installer versione 1,0                                 | Windows 95, Windows 98, Windows NT 4.0 + SP3                           | Windows me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Installer versione 1,1                                 | Windows 95, Windows 98, Windows NT 4.0 + SP3                           | Windows me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Installer versione 1,2                                 | Windows 95, Windows 98, Windows me, Windows NT 4.0 + SP3               | Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008             |
| Windows Installer versione 2,0                                 | Windows 95, Windows 98, Windows me, Windows NT 4.0 + SP6, Windows 2000 | Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008                           |



 

Ad esempio, un'applicazione che ridistribuisce Windows Installer versione 1,1 deve verificare che il sistema operativo sia Windows NT 4,0 SP3 o Windows 98/95 prima di eseguire il pacchetto ridistribuibile. Le applicazioni che utilizzano il pacchetto ridistribuibile devono inoltre garantire che la versione ANSI del Windows Installer sia installata in Windows 98/95 e che la versione Unicode sia installata in Windows NT o Windows 2000. Si noti che in alcune applicazioni la versione Unicode viene rinominata in InstMsiW.

## <a name="syntax"></a>Sintassi

 *Opzioni* di Instmsi

## <a name="command-line-options"></a>Opzioni da riga di comando

Le opzioni della riga di comando non fanno distinzione tra maiuscole e minuscole.



| Opzione                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /q                         | Per l'uso da parte di applicazioni che ridistribuiscono il Windows Installer come parte di un'applicazione di bootstrap. Non viene visualizzata alcuna interfaccia utente. L'applicazione di bootstrap deve controllare il codice restituito per determinare se è necessario riavviare il computer per completare l'installazione del Windows Installer.                                                                                                                                                                                                                          |
| /t                         | Utilizzato solo a scopo di debug.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /c: "msiinst/delayreboot"  | Opzione di riavvio ritardato. Impedisce a Instmsi di richiedere all'utente un riavvio anche se è necessario sostituire i file in uso durante l'installazione. Se Instmsi viene richiamato con questa opzione, viene restituito l'errore \_ \_ reboot riuscito \_ se è necessario sostituire i file in uso. Se non è necessario sostituire i file in uso, viene restituito l'errore \_ Success. Disponibile con Instmsi per Windows Installer 2,0 o versione successiva. Per ulteriori informazioni sui riavvii ritardati, vedere la sezione Osservazioni.<br/> |
| /c: "msiinst/delayrebootq" | Versione non interattiva dell'opzione di riavvio ritardato. Non presenta alcuna interfaccia utente per l'utente. In caso contrario, il comportamento è identico all'opzione precedente. Disponibile con Instmsi per Windows Installer 2,0 o versione successiva. Per ulteriori informazioni sui riavvii ritardati, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                                           |
| /?                         | Visualizza la Guida.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

Le applicazioni di [bootstrap](bootstrapping.md) che usano Instmsi.exe per installare il Windows Installer con un'altra applicazione possono richiedere un riavvio del sistema aggiuntivo. Si tratta potenzialmente di un riavvio aggiuntivo, oltre a tutti i riavvii necessari per installare l'applicazione.

L'opzione di riavvio ritardato è consigliata solo per gli sviluppatori di installazione che desiderano eliminare un riavvio aggiuntivo causato dall'utilizzo di Instmsi.exe con un'applicazione di installazione che consente di installare i file in uso.

Gli sviluppatori devono eseguire le operazioni seguenti nell'applicazione di installazione per usare l'opzione di riavvio ritardato. Questa opzione non è disponibile con Instmsi.exe versioni che installano versioni di Windows Installer precedenti alla versione 2,0:

**Per utilizzare l'opzione di riavvio ritardato**

1.  Chiamare Instmsi.exe con una delle opzioni della riga di comando per il riavvio ritardato.
2.  Considerare la restituzione di esito positivo errore \_ o errore \_ \_ riavvio riuscito \_ , necessario come operazione riuscita.
3.  Ottenere il percorso della cartella che contiene i file binari di Windows Installer appena installati dal valore InstallerLocation in:

    **HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Installer**

    Questo valore è di tipo **reg \_ SZ**.

4.  Impostare la directory corrente sul percorso ottenuto nel passaggio 3.
5.  Richiamare msiexec sul pacchetto dell'applicazione ed eseguire altro codice di installazione specifico dell'applicazione. Se l'applicazione di installazione usa [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), l'applicazione deve caricare MSI.DLL dal percorso ottenuto nel passaggio 3.
    > [!Note]  
    > Le applicazioni che chiamano **LoadLibrary** sul nuovo MSI.DLL nella posizione ottenuta nel passaggio 3 devono garantire che una versione precedente di MSI.DLL non sia già stata caricata nel processo. Se nel processo è stata caricata una versione precedente di MSI.DLL, è necessario scaricarla dallo spazio degli indirizzi del processo prima della chiamata a **LoadLibrary** per la nuova MSI.DLL.

     

6.  Se il passaggio (5) non richiede un riavvio e se Instmsi.exe ha restituito un \_ errore \_ \_ nel passaggio (1), richiedere all'utente di riavviare il computer per completare l'installazione dei file binari Windows Installer nel sistema. Tuttavia, se si verifica un riavvio nel passaggio (5), non sono necessari passaggi aggiuntivi.

Instmsi.exe è disponibile nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bootstrap](bootstrapping.md)
</dt> <dt>

[Bootstrap di download Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> </dl>

 

 




