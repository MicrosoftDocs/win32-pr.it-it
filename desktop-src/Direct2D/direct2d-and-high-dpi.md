---
title: Direct2D e High-DPI
description: Viene descritto il modo in cui Direct2D supporta la visualizzazione a DPI elevato.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, High-DPI
- DPI elevato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963402"
---
# <a name="direct2d-and-high-dpi"></a>Direct2D e High-DPI

La scrittura di un'applicazione in grado di riconoscere DPI è la chiave per rendere l'interfaccia utente (UI) molto coerente in un'ampia gamma di impostazioni di visualizzazione a DPI elevato. Un'applicazione che non è compatibile con DPI ma è in esecuzione in un'impostazione di visualizzazione a DPI elevato può soffrire di molti artefatti visivi, inclusa la scalabilità non corretta di elementi dell'interfaccia utente, testo ritagliato e immagini sfocate. Aggiungendo il supporto nell'applicazione per la compatibilità con DPI, è possibile rendere la presentazione dell'interfaccia utente dell'applicazione più prevedibile, rendendola più visivamente accattivante e più facile da leggere per gli utenti. Per fortuna, Direct2D rende più semplice che mai scrivere applicazioni che funzionano correttamente in un valore DPI elevato. In questo argomento sono contenute le sezioni seguenti.

-   [Supporto di valori DPI alti in Direct2D](#high-dpi-support-in-direct2d)
-   [Windows 8 e High-DPI](#windows-8-and-high-dpi)
-   [Che cos'è un DIP?](#what-is-a-dip)
-   [Argomenti correlati](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a>Supporto di valori DPI alti in Direct2D

Direct2D fornisce le seguenti funzionalità per l'utilizzo di scenari ad alta risoluzione:

-   Viene rispettato automaticamente il valore DPI del sistema quando si crea una destinazione di rendering a finestra, purché il manifesto dell'applicazione indichi che l'applicazione gestisce correttamente il valore DPI. Per informazioni su come dichiarare che l'applicazione è compatibile con DPI, vedere [come assicurarsi che l'applicazione venga visualizzata correttamente in schermi con valori DPI alti](how-to--size-a-window-properly-for-high-dpi-displays.md).
-   Esprime le coordinate in DIP (device independent pixel), che consente la scalabilità automatica dell'applicazione in caso di modifica dell'impostazione DPI.
-   Consente alle bitmap di avere un valore DPI e di ridimensionarle correttamente tenendo conto del valore DPI. Questa funzionalità può essere usata anche per gestire le icone con diverse risoluzioni.
-   Esprime la maggior parte delle risorse in DIP, rendendo automaticamente le risorse indipendenti dalla risoluzione.
-   Usa uno spazio delle coordinate a virgola mobile e l'anti-aliasing, quindi qualsiasi contenuto può essere ridimensionato in qualsiasi valore DPI arbitrario.

La pipeline di grafica Direct2D è progettata per la scalabilità da 96 DPI a 1200DPI.

## <a name="windows-8-and-high-dpi"></a>Windows 8 e High-DPI

A partire da Windows 8 sono disponibili funzionalità aggiuntive per il supporto di valori DPI alti.

Se il valore DPI del contesto di dispositivo è sufficientemente elevato, Direct2D modifica la soglia utilizzata per abilitare l'anti-aliasing verticale del testo. In questo modo si ottiene un rendering del testo più veloce sulle visualizzazioni con valori DPI alti. Inoltre, è possibile impostare la modalità unità su pixel anziché DIP usando il metodo [**ID2D1DeviceContext:: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) . Se si imposta la modalità unità su pixel e il valore DPI del contesto di dispositivo sul valore DPI dello schermo, l'ottimizzazione è ancora abilitata.

## <a name="what-is-a-dip"></a>Che cos'è un DIP?

Un Device Independent Pixel (DIP) è un pixel logico che esegue il mapping ai pixel del dispositivo fisico tramite un valore scalare, il valore DPI. DPI corrisponde ai punti per pollice, dove un punto rappresenta un pixel del dispositivo fisico. La nomenclatura deriva dalla stampa, dove i punti rappresentano il punto di input penna più piccolo che può produrre un processo di stampa. Poiché un monitor standard ha usato 96 punti per pollice, un valore DPI 96 significava che un Device Independent Pixel (o DIP) ha eseguito il mapping di 1:1 con un pixel fisico. Ad esempio, se il valore DPI era 96 \* 2 = 192, un singolo DIP includerebbe due pixel fisici.

Esistono molti motivi per cui le applicazioni non gestiscono necessariamente questo ridimensionamento correttamente; uno dei motivi più semplici è che richiede un lavoro aggiuntivo per individuare e usare questo valore scalare durante il rendering. In Direct2D il ridimensionamento viene applicato per impostazione predefinita. A causa di questo mapping, i pixel del dispositivo fisico possono finire con le coordinate del DIP frazionario, uno dei motivi per cui Direct2D usa uno spazio delle coordinate a virgola mobile.

<dl> pixel fisico = (DIP × DPI)/96  
</dl>

Per convertire un pixel fisico in un DIP, utilizzare la formula seguente:

<dl> DIP = (pixel fisico × 96)/DPI  
</dl>

> [!Note]
>
> A partire da Windows 8, è possibile impostare la modalità unità su pixel anziché DIP usando il metodo [**ID2D1DeviceContext:: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come verificare che l'applicazione venga visualizzata correttamente su schermi con DPI elevato](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 