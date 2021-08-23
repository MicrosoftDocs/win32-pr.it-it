---
title: Rimozione dei dispositivi desktop
description: Rimozione dei dispositivi desktop
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- Gadget
- desktop
- Windows Barra laterale
- Barra laterale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254c4794c93c6afeeec9374e7c1c73f7d538c82b343ffaea984369a72231deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707011"
---
# <a name="desktop-gadgets-removed"></a>Rimozione dei dispositivi desktop

## <a name="platforms"></a>Piattaforme

 **Client** - Windows 8  
**Server** - Windows Server 2012  



## <a name="description"></a>Descrizione

Dal punto di vista delle funzionalità, i funzionalità sono già stati deprecati e sono stati superati da nuovi riquadri animati e app. I dispositivi di protezione presentano anche un rischio per la sicurezza per gli utenti. Come piattaforma esistono vulnerabilità tali da poter sfruttare anche i benigni. Pertanto, per mantenere Windows 8 sistema operativo più moderno e sicuro, è stato scelto di rimuovere completamente i dispositivi dal sistema operativo. Windows 7 utenti con i propri accessori sul desktop riceveranno una notifica e i dispositivi verranno disinstallati.

## <a name="manifestation"></a>Manifestazione

I desktop non saranno disponibili nella Windows Desktop.

## <a name="mitigation"></a>Strategia di riduzione del rischio

L'API Desktop Gadgets e la struttura di cartelle rimarranno invariate per Windows 8. Le applicazioni che installano ed eseguono i visualizzatori a livello di codice usando questa API continueranno a essere eseguite senza errori (anche se non lo saranno).

## <a name="solution"></a>Soluzione

Gli sviluppatori di app desktop non devono creare pacchetti di icone nei programmi di installazione. Questi accessori avranno solo spazio per l'utente e non potranno essere eseguiti nel sistema.

## <a name="tests"></a>Test

Gli sviluppatori possono testare la compatibilità di questa modifica disabilitando il componente facoltativo per Desktop Gadgets in Windows 7. Per disabilitare i dispositivi in un pc Windows 7, seguire questa procedura:

1.  Passare a Attiva Windows funzionalità dal Pannello di controllo.
2.  Deselezionare la casella accanto a "Windows Piattaforma del dispositivo".
3.  Fare clic su OK e seguire eventuali istruzioni aggiuntive sullo schermo.

## <a name="resources"></a>Risorse

[Le vulnerabilità nei dispositivi di protezione potrebbero consentire l'esecuzione di codice in modalità remota](https://support.microsoft.com/kb/2719662)

 

 




