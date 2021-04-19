---
title: Esempio VListVW
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'Altre informazioni su: esempio VListVW'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305088"
---
# <a name="vlistvw-sample"></a>Esempio VListVW

Questo argomento descrive l'esempio di codice di esempio VListVW. Contiene le sezioni seguenti:

-   [Descrizione](#description)
-   [Requisiti minimi](#minimum-requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

Nell'esempio VListVW viene illustrato come implementare un semplice controllo visualizzazione elenco virtuale in un'applicazione. Un controllo di visualizzazione elenco virtuale è un controllo di visualizzazione elenco standard con lo **stile \_ OWNERDATA di LVS** . In questo esempio viene creato un controllo di visualizzazione elenco che "virtualmente" include 100.000 elementi. Gli elementi non vengono mai effettivamente aggiunti. Al contrario, il controllo di visualizzazione elenco virtuale indica il numero di elementi che contiene con il messaggio [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md) . Quando è necessario disegnare un elemento, il controllo elenco-visualizzazione esegue una query sulla finestra padre per visualizzare le informazioni con la notifica [ \_ GETDISPINFO LVN](lvn-getdispinfo.md) .

## <a name="minimum-requirements"></a>Requisiti minimi



| Prodotto          | Versione                               |
|------------------|---------------------------------------|
| DLL              | comctl32.dll versione 4,70             |
| Sistema operativo | Windows 95, Microsoft Windows NT 3,51 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

L'esempio VListVW è disponibile in GitHub nel repository di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples). Gli esempi di elementi di controllo di visualizzazione elenco sono disponibili [qui](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)

 

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

[Informazioni sui controlli List-View](list-view-controls-overview.md)
</dt> </dl>

 

 




