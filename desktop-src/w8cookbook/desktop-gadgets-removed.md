---
title: Gadget desktop rimossi
description: Gadget desktop rimossi
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- Gadget
- gadget desktop
- Barra laterale di Windows
- Barra laterale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104399813"
---
# <a name="desktop-gadgets-removed"></a>Gadget desktop rimossi

## <a name="platforms"></a>Piattaforme

 **Client** -Windows 8  
**Server** -Windows Server 2012  



## <a name="description"></a>Descrizione

Dal punto di vista della funzionalità, i gadget sono già stati deprecati e sono stati sottoclassati da nuovi riquadri animati e app. I gadget presentano anche un rischio per la sicurezza per gli utenti. Come piattaforma, esistono vulnerabilità in modo che possano essere sfruttati anche i gadget benigni. Pertanto, per poter sostenere Windows 8 come sistema operativo più moderno e sicuro, si è scelto di rimuovere i gadget dal sistema operativo. Gli utenti di Windows 7 con gadget sul desktop riceveranno una notifica e i gadget verranno disinstallati.

## <a name="manifestation"></a>Manifestazione

I gadget desktop non saranno disponibili sul desktop di Windows.

## <a name="mitigation"></a>Strategia di riduzione del rischio

L'API gadget desktop e la struttura di cartelle rimarranno invariate per Windows 8. Le applicazioni che installano ed eseguono i Gadget a livello di codice tramite questa API continueranno a funzionare senza errori (anche se i gadget non lo sono).

## <a name="solution"></a>Soluzione

Gli sviluppatori di app desktop non devono creare pacchetti di gadget nei programmi di installazione. In questi gadget sarà sufficiente spazio per l'utente e non sarà possibile eseguirlo nel sistema.

## <a name="tests"></a>Test

Gli sviluppatori sono in grado di testare la compatibilità di questa modifica disabilitando il componente facoltativo per i gadget desktop in Windows 7. Per disabilitare i gadget in un PC Windows 7, attenersi alla procedura seguente:

1.  Passare a attivare o disattivare le funzionalità Windows dal pannello di controllo.
2.  Deselezionare la casella accanto a "piattaforma Gadget Windows".
3.  Fare clic su OK e seguire le istruzioni aggiuntive sullo schermo.

## <a name="resources"></a>Risorse

[Le vulnerabilità nei gadget potrebbero consentire l'esecuzione di codice in modalità remota](https://support.microsoft.com/kb/2719662)

 

 




