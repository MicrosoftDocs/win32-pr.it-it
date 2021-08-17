---
title: Esempio di VListVW
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'Altre informazioni su: Esempio VListVW'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefcd39c44e79ab4eec23f7becf202d1a3cd3566f6be9496e9fd61b577c87f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957560"
---
# <a name="vlistvw-sample"></a>Esempio di VListVW

Questo argomento descrive l'esempio di codice di esempio VListVW. Contiene le sezioni seguenti:

-   [Descrizione](#description)
-   [Requisiti minimi](#minimum-requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

L'esempio VListVW illustra come implementare un controllo visualizzazione elenco virtuale semplice in un'applicazione. Un controllo visualizzazione elenco virtuale è un controllo visualizzazione elenco standard con lo stile **LVS \_ OWNERDATA.** In questo esempio viene creato un controllo visualizzazione elenco che contiene "virtualmente" 100.000 elementi. Gli elementi non vengono mai effettivamente aggiunti. Al controllo di visualizzazione elenco virtuale viene invece "detto" il numero di elementi contenuti con il messaggio [**LVM \_ SETITEMCOUNT.**](lvm-setitemcount.md) Quando è necessario disegnare un elemento, il controllo visualizzazione elenco esegue una query nella finestra padre per visualizzare informazioni con la notifica [ \_ LVN GETDISPINFO.](lvn-getdispinfo.md)

## <a name="minimum-requirements"></a>Requisiti minimi



| Prodotto          | Versione                               |
|------------------|---------------------------------------|
| DLL              | comctl32.dll versione 4.70             |
| Sistema operativo | Windows 95, Microsoft Windows NT 3.51 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

L'esempio VListVW è disponibile in github nel [repository Windows esempi classici](https://github.com/microsoft/Windows-classic-samples). Gli esempi di elementi del controllo visualizzazione elenco sono disponibili [qui](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)

 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio usando il prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto.
2.  Immettere `msbuild [project file]`.

Per compilare l'esempio usando Visual Studio:

1.  Aprire Windows Explorer e passare alla directory del progetto.
2.  Fare doppio clic sull'icona per il file con estensione vcproj per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu Compila **per** compilare la soluzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni List-View seguenti](list-view-controls-overview.md)
</dt> </dl>

 

 




