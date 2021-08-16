---
title: Esempio di HTMLEditRibbon
description: Questo esempio di codice illustra il markup e il codice necessari per eseguire la migrazione di un'applicazione mfc (Microsoft Foundation Classes) esistente per l'uso della Windows multifunzione.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 0f1299bdc20b1b94a5113d3cfcdda205b6ad8e513a59706d708362fbc8383bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202119"
---
# <a name="htmleditribbon-sample"></a>Esempio di HTMLEditRibbon

Questo esempio di codice illustra il markup e il codice necessari per eseguire la migrazione di un'applicazione mfc (Microsoft Foundation Classes) esistente per l'uso della Windows multifunzione. È stato creato usando l'applicazione di esempio HTMLEdit MFC esistente e modificandone il codice e le risorse per l'uso Windows barra multifunzione.

- [Osservazioni:](#remarks)
- [Utilizzo](#usage)
  - [Compilazione dell'esempio](#building-the-sample)
  - [Esecuzione dell'esempio](#running-the-sample)
- [Supporto](#support)
- [Requisiti minimi](#minimum-requirements)

## <a name="remarks"></a>Commenti

Per l'esempio MFC, vedere [HtmlEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).

## <a name="usage"></a>Utilizzo

Gli esempi Windows framework della barra multifunzione possono essere scaricati come progetti Microsoft Visual Studio autonomi dall'Area download [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o installati come parte di [Windows Software Development Kit (SDK).](https://developer.microsoft.com/windows/downloads/sdk-archive/)

- Windows Software Development Kit (SDK) (percorso di installazione standard): %ProgramFiles% Microsoft SDKs Windows numero di versione \\ \\ Esempi \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ HTMLEditRibbon

### <a name="building-the-sample"></a>Compilazione dell'esempio

Scaricare l'esempio.

Installare l'SDK Windows per Windows 7 e aprire la finestra di comando dell'ambiente di compilazione. Fare clic sul menu Start, quindi scegliere Tutti i programmi, Microsoft Windows SDK, quindi fare clic su CMD Shell.

Per compilare l'esempio dalla finestra di comando dell'ambiente di compilazione, passare alla directory di origine dell'esempio. Al prompt dei comandi digitare MSBUILD.

Per compilare l'esempio in Microsoft Visual Studio, caricare il file della soluzione o del progetto dell'esempio e premere CTRL+MAIUSC+B.

### <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio dalla finestra di comando dell'ambiente di compilazione, eseguire i file .exe nella cartella Bin Debug o Bin Release contenuta \\ nella cartella di origine \\ dell'esempio.

Per eseguire l'esempio compilato con il debug in Visual Studio, premere F5.

## <a name="support"></a>Supporto

Il [Windows di sviluppo della](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) barra multifunzione è disponibile per discutere di argomenti e porre domande relative allo sviluppo Windows applicazioni della barra multifunzione.

## <a name="minimum-requirements"></a>Requisiti minimi



| Requisito | Valore |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) e aggiornamento della [piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Server minimo supportato | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 e [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| File di intestazione e IDL     | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> L'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di scegliere come destinazione le applicazioni della barra multifunzione Windows Windows Vista e Windows Server 2008. Gli aggiornamenti della piattaforma saranno disponibili per tutti i Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) possono fare in modo che Windows Update rilevi se l'aggiornamento richiesto è installato; In caso contrario, Windows Update lo scarierà e lo installerà in background.

 

 

 





