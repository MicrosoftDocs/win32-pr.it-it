---
description: Instmsi.exe è il pacchetto ridistribuibile per l'installazione di Windows Installer&\# 160;2.0 e versioni precedenti di Windows Installer. Vedere Windows Installer Redistributables per i componenti ridistribuibili per Windows Installer&\# 160;3.0 e versioni successive.
ms.assetid: 74ea4530-3a73-4169-b0b7-f0272229192d
title: Instmsi.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2177fbb145dbfe2817dba2207cff95e5d80b801cc2f442085ba396f461870f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946119"
---
# <a name="instmsiexe"></a>Instmsi.exe

Instmsi.exe è il pacchetto ridistribuibile per l'installazione di Windows Installer 2.0 e delle versioni precedenti di Windows Installer. Vedere [Windows Installer Redistributables](windows-installer-redistributables.md) per i componenti ridistribuibili per Windows Installer 3.0 e versioni successive.

Per altre informazioni sulla versione del Windows installer fornita con il sistema operativo, vedere [Versioni rilasciate](released-versions-of-windows-installer.md)di Windows Installer .

Alcuni ridistribuibili non devono essere eseguiti in determinate versioni del sistema operativo. Nella tabella seguente viene descritto quale Instmsi è compatibile con il sistema operativo.



| Se Instmsi.exe installa questa versione del programma di installazione Windows | Instmsi.exe possono essere eseguiti in questi sistemi operativi                    | Instmsi.exe non deve essere eseguito in questi sistemi operativi                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Windows Programma di installazione versione 1.0                                 | Windows 95, Windows 98, Windows NT 4.0+SP3                           | Windows Me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Programma di installazione versione 1.1                                 | Windows 95, Windows 98, Windows NT 4.0+SP3                           | Windows Me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Programma di installazione versione 1.2                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0+SP3               | Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008             |
| Windows Programma di installazione versione 2.0                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0+SP6, Windows 2000 | Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008                           |



 

Ad esempio, un'applicazione che ridistribuisce Windows Installer versione 1.1 deve verificare che il sistema operativo sia Windows NT 4.0 SP3 o Windows 98/95 prima di eseguire il pacchetto ridistribuibile. Le applicazioni che usano il pacchetto ridistribuibile devono anche garantire che la versione ANSI del programma di installazione di Windows sia installata in Windows 98/95 e che la versione Unicode sia installata in Windows NT o Windows 2000. Si noti che alcune applicazioni rinominano la versione Unicode in InstMsiW.

## <a name="syntax"></a>Sintassi

**opzioni instmsi** 

## <a name="command-line-options"></a>Opzioni da riga di comando

Per le opzioni della riga di comando non viene fatto distinzione tra maiuscole e minuscole.



| Opzione                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /q                         | Per l'uso da parte di applicazioni che ridistribuino Windows installer come parte di un'applicazione di bootstrap. All'utente non viene presentata alcuna interfaccia utente. L'applicazione di bootstrap deve controllare il codice restituito per determinare se è necessario un riavvio per completare l'installazione del Windows installer.                                                                                                                                                                                                                          |
| /t                         | Usato solo a scopo di debug.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /c:"msiinst /delayreboot"  | Opzione di riavvio ritardata. Impedisce a Instmsi di richiedere un riavvio all'utente anche se è necessario sostituire i file in uso durante l'installazione. Se Instmsi viene richiamato con questa opzione, restituisce ERROR SUCCESS REBOOT REQUIRED se è necessario sostituire i file \_ \_ in \_ uso. Se non è necessario sostituire i file in uso, restituisce ERROR \_ SUCCESS. Disponibile con Instmsi per Windows Installer 2.0 o versione successiva. Per altre informazioni sui riavvii ritardati, vedere la sezione osservazioni.<br/> |
| /c:"msiinst /delayrebootq" | Versione non interattiva dell'opzione di riavvio posticipato. Non presenta alcuna interfaccia utente all'utente. In caso contrario, il comportamento è identico all'opzione precedente. Disponibile con Instmsi per Windows Installer 2.0 o versione successiva. Per altre informazioni sui riavvii ritardati, vedere la sezione osservazioni.<br/>                                                                                                                                                                                                                           |
| /?                         | Visualizza la Guida.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

[Il bootstrap di](bootstrapping.md) applicazioni che usano Instmsi.exe per installare il Windows installer con un'altra applicazione può richiedere un riavvio del sistema aggiuntivo. Si tratta potenzialmente di un riavvio aggiuntivo, oltre ai riavvii necessari per installare l'applicazione.

L'opzione di riavvio ritardato è consigliata solo per gli sviluppatori che vogliono eliminare un riavvio aggiuntivo causato dall'uso di Instmsi.exe con un'applicazione di installazione che installa i file in uso.

Gli sviluppatori devono eseguire le operazioni seguenti nell'applicazione di installazione per usare l'opzione di riavvio ritardato. Questa opzione non è disponibile con le versioni Instmsi.exe che installano Windows Installer versioni precedenti alla versione 2.0:

**Per usare l'opzione di riavvio ritardato**

1.  Chiamare Instmsi.exe con una delle opzioni della riga di comando per il riavvio ritardato.
2.  Considerare la restituzione di ERROR \_ SUCCESS o ERROR SUCCESS REBOOT REQUIRED come operazione \_ \_ \_ riuscita.
3.  Ottenere il percorso della cartella contenente i file binari del programma di installazione Windows appena installati dal valore InstallerLocation in:

    **HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Installer**

    Questo valore è di tipo **REG \_ SZ**.

4.  Impostare la directory corrente sul percorso ottenuto nel passaggio 3.
5.  Richiamare Msiexec nel pacchetto dell'applicazione ed eseguire altro codice di installazione specifico per l'applicazione. Se l'applicazione di installazione [**usa MsiInstallProduct,**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)l'applicazione deve caricare MSI.DLL dal percorso ottenuto nel passaggio 3.
    > [!Note]  
    > Le applicazioni che chiamano **LoadLibrary** sul nuovo MSI.DLL nel percorso ottenuto nel passaggio 3 devono garantire che una versione precedente di MSI.DLL non sia già stata caricata all'interno del processo. Se una versione precedente di MSI.DLL è stata caricata all'interno del processo, deve essere scaricata dallo spazio degli indirizzi del processo prima della chiamata **a LoadLibrary** per il nuovo MSI.DLL.

     

6.  Se il passaggio (5) non richiede un riavvio e se Instmsi.exe ha restituito ERROR SUCCESS REBOOT REQUIRED nel passaggio \_ (1), richiedere all'utente un riavvio per completare l'installazione dei file binari del programma di installazione \_ \_ di Windows nel sistema. Tuttavia, se si verifica un riavvio nel passaggio (5), non sono necessari passaggi aggiuntivi.

Instmsi.exe è disponibile in componenti sdk [Windows per sviluppatori Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bootstrap](bootstrapping.md)
</dt> <dt>

[Bootstrap di download Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> </dl>

 

 




