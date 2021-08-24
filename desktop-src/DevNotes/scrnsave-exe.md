---
description: HKCU \\ Pannello di controllo \\ Desktop.
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1ac7c0f2ee9d87911c0db195df89e2c27dcf1b19c0e9dac70d1517b0ad30ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571351"
---
# <a name="scrnsaveexe"></a>SCRNSAVE.EXE

**HKCU \\ Pannello di controllo \\ Desktop**



| Tipo di dati | Range       | Valore predefinito |
|-----------|-------------|---------------|
| REG \_ SZ   | *Nome file* | (nessuna)        |



 

## <a name="description"></a>Descrizione

Specifica il nome del file screen saver file eseguibile.

## <a name="change-method"></a>Cambia metodo

Per modificare il valore di questa voce, in Pannello di controllo doppio clic su Visualizza **,** fare clic sulla scheda Screen **saver** e quindi selezionare un screen saver dall'elenco **Screen saver** .

È anche possibile modificare questa voce con la funzione **dell'API InstallScreenSaver,** che viene esportata da Desk.cpl. È possibile accedere a questa funzione con la riga di comando **rundll32.exe desk.cpl,InstallScreenSaver** *file*, dove *file* è il nome di un screen saver file eseguibile.

## <a name="activation-method"></a>Metodo di attivazione

Le modifiche apportate a questa voce diventano effettive al successivo avvio di un screen saver. Le modifiche apportate a questa voce mentre screen saver è in esecuzione non hanno alcun effetto sul screen saver.

## <a name="notes"></a>Note

-   Windows sistemi operativi aggiungere questa voce al Registro di sistema quando si usa Visualizza **Pannello di controllo** per selezionare un screen saver. Se si disabilitano tutti gli screen saver scegliendo **(Nessuno)** dall'elenco screen saver, il sistema operativo elimina questa voce dal Registro di sistema e chiama la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con *uiAction* uguale a SPI \_ SETSCREENSAVEACTIVE e *uiParam* uguale a **FALSE.**
-   Questa voce può essere sostituita da un'Criteri di gruppo predefinita nei sistemi che supportano Criteri di gruppo. Mentre **l'impostazione Nome eseguibile** dello screen saver Criteri di gruppo è abilitata, il sistema ignora questa voce. La configurazione di questa impostazione dei criteri viene archiviata **nella voceSCRNSAVE.EXE,** che si trova nella **sottochiave** Criteri.

 

 
