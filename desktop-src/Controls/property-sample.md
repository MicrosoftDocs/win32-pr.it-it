---
title: Esempio di proprietà
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 'Ulteriori informazioni su: esempio di proprietà'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c11fda9b133ca6fa3b2f9942d8d48bec3a9e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125976"
---
# <a name="property-sample"></a>Esempio di proprietà

Questo argomento descrive l'esempio di codice di esempio della proprietà. Contiene le sezioni seguenti:

-   [Descrizione](#description)
-   [Requisiti minimi](#minimum-requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

Nell'esempio di proprietà viene illustrato come implementare tre stili diversi di finestre delle proprietà: modale, non modale e procedura guidata. Viene inoltre illustrato come utilizzare la funzione [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) per modificare la finestra di dialogo della finestra delle proprietà prima o dopo la creazione.

## <a name="minimum-requirements"></a>Requisiti minimi



| Prodotto          | Versione                              |
|------------------|--------------------------------------|
| DLL              | comctl32.dll versione 4,0             |
| Sistema operativo | Windows 95, Microsoft Windows NT 3,1 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

L'esempio di proprietà viene installato come parte di [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) ed è disponibile nel percorso seguente.



| Location    | Percorso/URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| Windows SDK | % Program Files% \\ Microsoft SDK \\ numero di versione di Windows \\ \[ \] \\ esempi \\ WinUI \\ controlli di \\ \\ Proprietà comuni |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio utilizzando il prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto.
2.  Immettere `msbuild [project file]`.

Per compilare l'esempio con Visual Studio:

1.  Aprire Esplora risorse e passare alla directory del progetto.
2.  Fare doppio clic sull'icona del file con estensione vcproj per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** per compilare la soluzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle finestre delle proprietà](property-sheets.md)
</dt> </dl>

 

 




