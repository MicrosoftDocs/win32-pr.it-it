---
title: Esempio di FontControl
description: Questo esempio di codice illustra il markup e il codice necessari per implementare un controllo FontControl all'interno di un'Windows ribbon.
ms.assetid: 8fb84bd1-5e63-447c-b7a0-b3d7cb8c3be7
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 99e7ad587820ac18ce83d673efaa972f0f3b75c4547ddc7e8b4889a0e17e3bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202174"
---
# <a name="fontcontrol-sample"></a>Esempio di FontControl

Questo esempio di codice illustra il markup e il codice necessari per implementare un controllo FontControl all'interno di un'Windows ribbon.

- [Utilizzo](#usage)
  - [Compilazione dell'esempio](#building-the-sample)
  - [Esecuzione dell'esempio](#running-the-sample)
- [Supporto](#support)
- [Requisiti minimi](#minimum-requirements)
- [Argomenti correlati](#related-topics)

## <a name="usage"></a>Utilizzo

Gli Windows di framework della barra multifunzione possono essere scaricati come progetti Microsoft Visual Studio autonomi dall'Area download [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o installati come parte di [Windows Software Development Kit (SDK).](https://developer.microsoft.com/windows/downloads/sdk-archive/)

- Windows Software Development Kit (SDK) (percorso di installazione standard): %ProgramFiles% Microsoft SDK Windows numero di versione \\ \\ Esempi \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ FontControl

### <a name="building-the-sample"></a>Compilazione dell'esempio

Scaricare l'esempio.

Installare l'SDK Windows per Windows 7 e aprire la finestra di comando dell'ambiente di compilazione. Fare clic sul menu Start, quindi scegliere Tutti i programmi, Microsoft Windows SDK, quindi fare clic su CMD Shell.

Per compilare l'esempio dalla finestra di comando dell'ambiente di compilazione, passare alla directory di origine dell'esempio. Al prompt dei comandi digitare MSBUILD.

Per compilare l'esempio in Microsoft Visual Studio, caricare il file della soluzione o del progetto dell'esempio e premere CTRL+MAIUSC+B.

### <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio dalla finestra di comando dell'ambiente di compilazione, eseguire i file .exe nella cartella Bin Debug o Bin Release contenuta nella cartella \\ di origine \\ dell'esempio.

Per eseguire l'esempio compilato con il debug in Visual Studio, premere F5.

## <a name="support"></a>Supporto

Il [Windows di sviluppo della](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) barra multifunzione è disponibile per discutere argomenti e porre domande relative allo sviluppo di applicazioni Windows ribbon.

## <a name="minimum-requirements"></a>Requisiti minimi



| Requisito | Valore |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Server minimo supportato | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 e aggiornamento della piattaforma [per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| File di intestazione e IDL     | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> L'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di scegliere come destinazione le applicazioni della barra multifunzione Windows Windows Vista e Windows Server 2008. Gli aggiornamenti della piattaforma saranno disponibili per tutti i clienti Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) possono fare in modo che Windows Update rilevi se l'aggiornamento richiesto è installato; In caso contrario, Windows update lo scariderà e lo installerà in background.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo Carattere](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> </dl>

 

 





