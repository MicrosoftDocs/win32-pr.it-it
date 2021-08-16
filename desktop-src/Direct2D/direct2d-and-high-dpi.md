---
title: Direct2D e valori DPI alti
description: Descrive in che modo Direct2D supporta la visualizzazione con valori DPI alti.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, valori DPI alti
- valori DPI alti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5c48f9a1b3552115ebbec8a54a6878716ef34675e41193ae08fb9cb8e55bc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825983"
---
# <a name="direct2d-and-high-dpi"></a>Direct2D e valori DPI alti

La scrittura di un'applicazione con supporto DPI è la chiave per fare in modo che un'interfaccia utente (UI) sia coerente in un'ampia gamma di impostazioni di visualizzazione con valori DPI elevati. Un'applicazione che non supporta DPI ma è in esecuzione in un'impostazione di visualizzazione con valori DPI elevati può subire molti artefatti visivi, tra cui il ridimensionamento non corretto degli elementi dell'interfaccia utente, il testo ritagliato e le immagini sfocate. Aggiungendo il supporto nell'applicazione per il riconoscimento DPI, si rende più prevedibile la presentazione dell'interfaccia utente dell'applicazione, rendendola più visivamente accattivante e più facile da leggere per gli utenti. Fortunatamente, Direct2D rende più semplice che mai scrivere applicazioni che funzionano bene con valori DPI elevati. In questo argomento sono contenute le sezioni seguenti.

-   [Supporto di valori DPI elevati in Direct2D](#high-dpi-support-in-direct2d)
-   [Windows 8 e valori DPI alti](#windows-8-and-high-dpi)
-   [Che cos'è un DIP?](#what-is-a-dip)
-   [Argomenti correlati](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a>Supporto di valori DPI elevati in Direct2D

Direct2D offre le funzionalità seguenti per l'uso di scenari con valori DPI elevati:

-   Rispetta automaticamente il valore DPI di sistema durante la creazione di una destinazione di rendering finestra, purché il manifesto dell'applicazione indichi che il valore DPI viene gestito correttamente dall'applicazione. Per informazioni su come dichiarare che l'applicazione è in grado di riconoscere DPI, vedere Come assicurarsi che l'applicazione venga visualizzata correttamente in schermi con [valori DPI alti.](how-to--size-a-window-properly-for-high-dpi-displays.md)
-   Esprime le coordinate in DIP (Device Independent Pixel), che consente all'applicazione di ridimensionarsi automaticamente quando viene modificata l'impostazione DPI.
-   Consente alle bitmap di avere un valore DPI e di ridimensionarle correttamente prendendo in considerazione il valore DPI. Questa funzionalità può essere usata anche per mantenere le icone a risoluzioni diverse.
-   Esprime la maggior parte delle risorse nei dip, che rende automaticamente le risorse indipendenti dalla risoluzione.
-   Usa uno spazio delle coordinate a virgola mobile e un antialiasing, quindi qualsiasi contenuto può essere ridimensionato in base a qualsiasi valore DPI arbitrario.

La pipeline grafica Direct2D è progettata per la scalabilità da 96 DPI a 1200DPI.

## <a name="windows-8-and-high-dpi"></a>Windows 8 e valori DPI alti

A partire Windows 8, sono disponibili funzionalità aggiuntive per il supporto di valori DPI elevati.

Se il valore DPI del contesto di dispositivo è sufficientemente elevato, Direct2D modifica la soglia che usa per abilitare l'antialiasing verticale del testo. In questo modo, il rendering del testo su schermi con valori DPI elevati risulta più veloce. È anche possibile impostare la modalità unità su pixel anziché DIP usando il [**metodo ID2D1DeviceContext::SetUnitMode.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) Se si imposta la modalità unità su pixel e il DPI del contesto di dispositivo sul valore DPI dello schermo, l'ottimizzazione è ancora abilitata.

## <a name="what-is-a-dip"></a>Che cos'è un DIP?

Un DIP (Device Independent Pixel) è un pixel logico che esegue il mapping ai pixel del dispositivo fisico tramite un valore scalare, il valore DPI. DPI è l'acronimo di dots per inch( punti per pollice), dove un punto rappresenta un pixel fisico del dispositivo. La nomenclatura deriva dalla stampa, in cui i punti sono il punto input penna più piccolo che un processo di stampa può produrre. Poiché un monitor standard usava 96 punti per pollice, un valore DPI di 96 significava che un dip (Device Independent Pixel) eseguiva il mapping 1:1 con un pixel fisico. Ad esempio, se il valore DPI fosse 96 2 = 192, un singolo DIP includerebbe \* due pixel fisici.

Esistono molti motivi per cui le applicazioni non gestiscono necessariamente questo ridimensionamento correttamente. uno dei motivi più semplici è che richiede lavoro aggiuntivo per individuare e usare questo valore scalare durante il rendering. In Direct2D il ridimensionamento viene applicato per impostazione predefinita. A causa di questo mapping, i pixel del dispositivo fisico potrebbero finire in corrispondenza di coordinate DIP frazionarie. Questo è uno dei motivi per cui Direct2D usa uno spazio delle coordinate a virgola mobile.

<dl> pixel fisico = (dip × DPI) / 96  
</dl>

Per convertire un pixel fisico in diP, usare questa formula:

<dl> dip = (pixel fisico × 96) / DPI  
</dl>

> [!Note]
>
> A partire Windows 8, è possibile impostare la modalità unità su pixel anziché DIP usando il metodo [**ID2D1DeviceContext::SetUnitMode.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come assicurarsi che l'applicazione venga visualizzata correttamente su schermi con valori DPI alti](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 