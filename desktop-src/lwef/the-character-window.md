---
title: Finestra Carattere
description: Finestra Carattere
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426aab4cbd6e0ad536135cb47ec9a636ea56a0509f3fb0cb75ad6440addc62da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474887"
---
# <a name="the-character-window"></a>Finestra Carattere

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Microsoft Agent visualizza i caratteri animati nelle proprie finestre che vengono sempre visualizzati nella parte superiore dell'ordine z della finestra, ovvero sempre in alto. Un utente può spostare la finestra di un carattere trascinando il carattere con il pulsante sinistro del mouse. L'immagine del carattere viene spostata con il puntatore . Inoltre, un'applicazione può spostare un carattere usando il [**metodo MoveTo.**](moveto-method.md)

Quando l'utente fa clic con il pulsante destro del mouse su un carattere, viene visualizzato un menu a comparsa che visualizza i comandi seguenti:

Aprire \| la finestra Comandi chiudi <span class="underline">V</span>oice

<span class="underline">Ide H</span>

----------------------------…

Comando\*


*OtherHostingApplicationCaption\*\**

\*I comandi elencati si basano sul client attivo di input. Per altre informazioni sulla definizione dei comandi visualizzati nel menu a comparsa, vedere Panoramica dell'interfaccia di programmazione di Microsoft Agent.

\*\*Le voci elencate sono tutte le altre applicazioni che ospitano il carattere. Per altre informazioni sulla definizione di questa voce, vedere Panoramica dell'interfaccia di programmazione di Microsoft Agent.

Il comando \| Apri finestra comandi vocali di chiusura controlla la visualizzazione della finestra Comandi del carattere attivo corrente. Se i servizi di riconoscimento vocale sono disabilitati, questo comando è disabilitato. Se i servizi di riconoscimento vocale non sono installati, questo comando non viene visualizzato.

Il comando Nascondi nasconde il carattere. L'animazione assegnata allo stato **Nascondi** del carattere riproduce e nasconde il carattere. La lettera "H" in hide è la chiave di accesso del comando (mnemotica).

I comandi per le applicazioni che attualmente ospitano il carattere seguono il comando Nascondi, preceduto da un separatore. Vengono quindi visualizzati i nomi di altre applicazioni che usano il carattere, preceduti anche da un separatore.

 

 




