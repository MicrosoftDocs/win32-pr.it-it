---
description: '\\Desktop del pannello di controllo HKCU \\ .'
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401478"
---
# <a name="scrnsaveexe"></a>SCRNSAVE.EXE

**\\Desktop del pannello di controllo HKCU \\**



| Tipo di dati | Range       | Valore predefinito |
|-----------|-------------|---------------|
| REG \_ SZ   | *Nome file* | (nessuna)        |



 

## <a name="description"></a>Descrizione

Specifica il nome del file eseguibile screen saver.

## <a name="change-method"></a>Cambia metodo

Per modificare il valore di questa voce, nel pannello di controllo fare doppio clic su **schermo**, fare clic sulla scheda **screen saver** , quindi selezionare un screen saver dall'elenco **screen saver** .

È anche possibile modificare questa voce con la funzione Application Programming Interface (API) **InstallScreenSaver**, che viene esportata da Desk.cpl. È possibile accedere a questa funzione con la riga di comando **rundll32.exe desk.cpl** *file* InstallScreenSaver, dove *file* è il nome di un file eseguibile di screen saver.

## <a name="activation-method"></a>Metodo di attivazione

Le modifiche apportate a questa voce diventano effettive al successivo avvio di un screen saver da parte del sistema. Le modifiche apportate a questa voce mentre un screen saver è in esecuzione non hanno alcun effetto sulla screen saver in esecuzione.

## <a name="notes"></a>Note

-   I sistemi operativi Windows aggiungono questa voce al registro di sistema quando si usa **Visualizza** nel pannello di controllo per selezionare un screen saver. Se si disabilitano tutti i salvaschermi selezionando **(nessuno)** dall'elenco Screen saver, il sistema operativo elimina questa voce dal registro di sistema e chiama la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con *uiAction* uguale a spi \_ SETSCREENSAVEACTIVE e *uiParam* uguale a **false**.
-   Questa voce può essere sostituita da un'impostazione di Criteri di gruppo nei sistemi che supportano Criteri di gruppo. Mentre il **nome dell'eseguibile screen saver** criteri di gruppo impostazione è abilitato, il sistema ignora questa voce. La configurazione di questa impostazione dei criteri viene archiviata nella voce **SCRNSAVE.EXE** , che si trova nella sottochiave **policy** .

 

 
