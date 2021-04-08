---
title: Introduzione con Windows Media Player SDK
description: Introduzione con Windows Media Player SDK
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobile, plug-in
- Plug-in di Windows Media Player Mobile, interfaccia utente
- Plug-in di Windows Media Player Mobile
- plug-in, interfaccia utente
- plug-in, Windows Media Player Mobile
- plug-in dell'interfaccia utente, Windows Media Player Mobile
- Plug-in dell'interfaccia utente, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739303"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a>Introduzione con Windows Media Player SDK

Per creare il plug-in, è prima di tutto necessario installare Microsoft eMbedded Visual C++ 4,0 e Visual Studio 2003. È inoltre necessario installare Pocket PC 2003 SDK o Smartphone 2003 SDK, che sono download distinti. Per compilare ed eseguire il progetto, un dispositivo Pocket PC o smartphone che esegue il sistema operativo Windows Mobile 2003 Second Edition deve essere sincronizzato con il computer di sviluppo tramite Microsoft ActiveSync® 3.7.1 o versione successiva.

Poiché i plug-in dell'interfaccia utente nei dispositivi Windows Mobile utilizzano lo stesso modello di plug-in delle versioni desktop, è possibile utilizzare la creazione guidata plug-in di Windows Media Player come punto di partenza per la creazione di un plug-in di interfaccia utente in background che funzionerà con Windows Media Player 10 Mobile.

Per creare il codice del plug-in dell'interfaccia utente, eseguire le operazioni seguenti:

1.  Aprire Visual Studio 2003 e avviare un nuovo progetto in Visual C++.
2.  Selezionare **creazione guidata plug-in di Windows Media Player** dal riquadro **modelli** .
3.  Assegnare al progetto il nome NetworkPlugin e fare clic su **OK**.
4.  Selezionare il **plug-in dell'interfaccia utente** e fare clic su **Avanti**.
5.  Selezionare **sfondo** , quindi fare clic su **Avanti**.
6.  Fare clic su **Avanti** per uscire dalla procedura guidata. Se si intende monitorare gli eventi con il plug-in, è necessario controllare l' **ascolto degli eventi** prima di completare la procedura guidata ed è necessario leggere la documentazione per l'interfaccia **IWMPEvents** per scoprire quali eventi sono supportati in Windows Media Player 10 Mobile.

Ora che è stato creato il codice del plug-in dell'interfaccia utente, è necessario creare un progetto di Windows CE DLL vuoto in eMbedded Visual C++ 4,0. Copiare quindi i file di origine generati dalla procedura guidata nel nuovo progetto in modo che vengano compilati con il compilatore ARM4.

Per creare un progetto vuoto

1.  Avviare un nuovo progetto in eMbedded Visual C++, quindi selezionare **WCE Dynamic-Link Library** dal riquadro **progetti** .
2.  Assegnare un nome al progetto e fare clic su **OK**.
3.  Verificare che sia selezionato **un progetto di Windows CE dll vuoto** , quindi fare clic su **fine**.
4.  Fare clic sulla voce di menu **progetto** .
5.  Selezionare **Aggiungi al progetto**, quindi fare clic su **file**.
6.  Selezionare i file C++ creati con la creazione guidata plug-in, quindi fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un plug-in dell'interfaccia utente per Windows Media Player 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[**Interfaccia IWMPEvents**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




