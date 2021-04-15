---
title: Finestra dei caratteri
description: Finestra dei caratteri
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399971"
---
# <a name="the-character-window"></a>Finestra dei caratteri

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Microsoft Agent Visualizza i caratteri animati nelle rispettive finestre che vengono sempre visualizzate nella parte superiore della finestra z-order (ovvero always on top). Un utente può spostare la finestra di un carattere trascinando il carattere con il pulsante sinistro del mouse. L'immagine del carattere viene spostata con il puntatore. Inoltre, un'applicazione può spostare un carattere utilizzando il metodo [**MoveTo**](moveto-method.md) .

Quando l'utente fa clic con il pulsante destro del mouse su un carattere, viene visualizzato un menu popup che Visualizza i comandi seguenti:

Apre \| la <span class="underline"></span>finestra comandi OICE di chiusura

IDE <span class="underline">H</span>

----------------------------…

Comando\*


*OtherHostingApplicationCaption\*\**

\*I comandi elencati sono basati sul client attivo per l'input. Per ulteriori informazioni sulla definizione dei comandi visualizzati nel menu a comparsa, vedere la panoramica dell'interfaccia di programmazione Microsoft Agent.

\*\*Le voci elencate sono tutte le altre applicazioni che attualmente ospitano il carattere. Per ulteriori informazioni sulla definizione di questa voce, vedere Cenni preliminari sull'interfaccia di programmazione Microsoft Agent.

Il \| comando Apri Chiudi voce comandi finestra Controlla la visualizzazione della finestra comandi del carattere attivo corrente. Se i servizi di riconoscimento vocale sono disabilitati, questo comando è disabilitato. Se servizi di riconoscimento vocale non è installato, questo comando non viene visualizzato.

Il comando Hide nasconde il carattere. L'animazione assegnata allo stato di **Nascondi** del carattere viene riprodotta e nasconde il carattere. La lettera "H" in Hide è la chiave di accesso del comando (mnemonico).

I comandi per le applicazioni che attualmente ospitano il carattere seguono il comando Hide, preceduto da un separatore. Vengono quindi visualizzati i nomi di altre applicazioni che utilizzano il carattere, preceduti anche da un separatore.

 

 




