---
title: Esempio SimpleRibbon
description: Questo esempio di codice illustra come implementare una semplice Windows barra multifunzione.
ms.assetid: 9196ae63-ca9e-43ae-8b4c-a30f1ef700f0
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: b2a7ab939239bd3c0017dfeeeab1487bcb1dce26
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691660"
---
# <a name="simpleribbon-sample"></a>Esempio SimpleRibbon

Questo esempio di codice illustra come implementare una semplice Windows barra multifunzione.

- [Utilizzo](#usage)
  - [Compilazione dell'esempio](#building-the-sample)
  - [Esecuzione dell'esempio](#running-the-sample)
- [Supporto](#support)
- [Requisiti minimi](#minimum-requirements)

## <a name="usage"></a>Utilizzo

Gli esempi Windows framework della barra multifunzione possono essere scaricati come progetti Microsoft Visual Studio autonomi dall'Area [download Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o installati come parte di Windows Software Development [Kit (SDK).](https://developer.microsoft.com/windows/downloads/sdk-archive/)

- Windows Software Development Kit (SDK) (percorso di installazione standard): %ProgramFiles% Microsoft SDKs Windows numero di versione \\ \\ Esempi \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ SimpleRibbon

### <a name="building-the-sample"></a>Compilazione dell'esempio

Scaricare l'esempio.

Installare l'SDK Windows per Windows 7 e aprire la finestra di comando dell'ambiente di compilazione. Fare clic sul menu Start, quindi scegliere Tutti i programmi, Microsoft Windows SDK, quindi fare clic su CMD Shell.

Per compilare l'esempio dalla finestra di comando dell'ambiente di compilazione, passare alla directory di origine dell'esempio. Al prompt dei comandi digitare MSBUILD.

Per compilare l'esempio in Microsoft Visual Studio, caricare il file della soluzione o del progetto dell'esempio e premere CTRL+MAIUSC+B.

### <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio dalla finestra di comando dell'ambiente di compilazione, eseguire i file .exe nella cartella Bin Debug o Bin Release contenuta nella cartella \\ \\ di origine dell'esempio.

Per eseguire l'esempio compilato con il debug in Visual Studio, premere F5.

## <a name="support"></a>Supporto

Il [Windows di sviluppo della](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) barra multifunzione è disponibile per discutere di argomenti e porre domande relative allo sviluppo di applicazioni Windows ribbon.

## <a name="minimum-requirements"></a>Requisiti minimi



| Requisito | Valore |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) e aggiornamento della [piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Server minimo supportato | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 e [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| File di intestazione e IDL     | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> L'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di scegliere come destinazione le applicazioni della barra multifunzione Windows di Windows Vista e Windows Server 2008. Gli aggiornamenti della piattaforma saranno disponibili per tutti i clienti Windows Vista e Windows Server 2008 tramite Windows Update. Per le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l'aggiornamento della piattaforma per Windows Server [2008,](https://msdn.microsoft.com/library/dd378748.aspx) l'aggiornamento di Windows può rilevare se è installato l'aggiornamento necessario. In caso contrario, Windows Update lo scarierà e lo installerà in background.

 

 

 





