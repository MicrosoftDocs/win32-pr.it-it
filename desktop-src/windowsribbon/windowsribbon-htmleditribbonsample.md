---
title: Esempio HTMLEditRibbon
description: Questo esempio di codice mostra il markup e il codice necessari per eseguire la migrazione di un'applicazione Microsoft Foundation Classes (MFC) esistente per usare la barra multifunzione di Windows.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f98d4d76508b812d86a4dab38f8dcec96dadc52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048077"
---
# <a name="htmleditribbon-sample"></a>Esempio HTMLEditRibbon

Questo esempio di codice mostra il markup e il codice necessari per eseguire la migrazione di un'applicazione Microsoft Foundation Classes (MFC) esistente per usare la barra multifunzione di Windows. È stato creato prendendo l'applicazione di esempio MFC HTMLEdit esistente e modificando il codice e le risorse per usare la barra multifunzione di Windows.

-   [Osservazioni:](#remarks)
-   [Utilizzo](#usage)
    -   [Compilazione dell'esempio](#building-the-sample)
    -   [Esecuzione dell'esempio](#running-the-sample)
-   [Supporto](#support)
-   [Requisiti minimi](#minimum-requirements)

## <a name="remarks"></a>Commenti

Per l'esempio MFC, vedere [esempio HTMLEdit: esegue il wrapping del controllo di modifica MSHTML di Internet Explorer](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).

## <a name="usage"></a>Utilizzo

L'esempio HTMLEditRibbon può essere scaricato come un progetto Microsoft Visual Studio autonomo dall' [area download Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) o installato come parte di [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).

-   Area download Microsoft: [esempi della barra multifunzione di Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)
-   Windows Software Development Kit (SDK) (percorso di installazione standard):% ProgramFiles% \\ Microsoft \\ SDK \\ \[ numero di versione Windows \] \\ esempi \\ WinUI \\ WindowsRibbon \\ HTMLEditRibbon

### <a name="building-the-sample"></a>Compilazione dell'esempio

Scaricare l'esempio nel disco rigido.

Installare la Windows SDK per Windows 7 e aprire la finestra di comando dell'ambiente di compilazione. Fare clic sul menu Start, quindi scegliere Tutti i programmi, Microsoft Windows SDK, quindi fare clic su CMD Shell.

Per compilare l'esempio dalla finestra di comando dell'ambiente di compilazione, passare alla directory di origine dell'esempio. Al prompt dei comandi digitare MSBUILD.

Per compilare l'esempio in Microsoft Visual Studio, caricare il file della soluzione o del progetto dell'esempio e premere CTRL+MAIUSC+B.

### <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio dalla finestra di comando dell'ambiente di compilazione, eseguire i file con estensione exe nella \\ cartella bin debug o bin \\ Release contenuta nella cartella di origine dell'esempio.

Per eseguire l'esempio compilato con il debug in Visual Studio, premere F5.

## <a name="support"></a>Supporto

Il [Forum di sviluppo della barra multifunzione di Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) è disponibile per discutere argomenti e porre domande relative allo sviluppo di applicazioni della barra multifunzione di Windows.

## <a name="minimum-requirements"></a>Requisiti minimi



| Requisito | Valore |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) e [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Server minimo supportato | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 e [aggiornamento della piattaforma per Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| File di intestazione e IDL     | UIRibbon. h, UIRibbon. idl                                                                                                                                                 |



 

> [!Note]  
> L' [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l' [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di utilizzare applicazioni della barra multifunzione di Windows in Windows vista e Windows Server 2008. Gli aggiornamenti della piattaforma saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l' [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l' [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) possono avere Windows Update rilevare se l'aggiornamento richiesto è installato; in caso contrario, Windows Update lo scaricherà e installerà in background.

 

 

 





