---
title: Esempio CustomAccServer
description: .
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c047bde41bdf4a486e14ce6f293113a41ae9e285
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398674"
---
# <a name="customaccserver-sample"></a>Esempio CustomAccServer

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Informazioni sul download](#download-information)
-   [Requisiti minimi](#minimum-requirements)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

Questo esempio illustra come implementare un server Microsoft Active Accessibility per un controllo personalizzato semplice. L'oggetto accessibile per il controllo è costituito dall'elemento radice (casella di riepilogo) e dai relativi elementi figlio (elementi dell'elenco).

## <a name="download-information"></a>Informazioni sul download

L'esempio CustomAccServer viene installato come parte del [Software Development Kit (SDK) di Microsoft Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) ed è disponibile nel percorso seguente.



| Location    | Percorso/URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Windows SDK | % Programmi% \\ Microsoft SDK \\ numero di versione di Windows \\ \[ \] \\ esempi \\ WinUI \\ MSAA |



 

## <a name="minimum-requirements"></a>Requisiti minimi



| Prodotto          | Versione                         |
|------------------|---------------------------------|
| Sistema operativo | Windows XP, Windows Server 2003 |
| Windows SDK      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio con Visual Studio 2008:

1.  Eseguire lo strumento di configurazione di Microsoft Windows Software Development Kit (SDK) fornito con l'SDK per aggiungere directory di inclusione SDK a Visual Studio.
2.  Aprire Esplora risorse e passare alla directory del progetto.
3.  Fare doppio clic sull'icona del file con estensione sln (soluzione) per aprire il progetto in Visual Studio.
4.  Scegliere **Compila soluzione** dal menu **Compila** per compilare la soluzione. L'applicazione verrà compilata nella \\ directory di debug o di \\ versione predefinita.

Per compilare l'esempio dalla riga di comando, vedere compilazione di esempi nelle note sulla versione di Windows SDK nel percorso seguente:% Program Files% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio:

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Digitare AccServer.exe dalla riga di comando oppure fare doppio clic sull'icona AccServer.exe per avviarla da Esplora risorse.

Per eseguire da Visual Studio, premere F5 o fare clic su **Avvia debug** dal menu **debug** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi](samples.md)
</dt> </dl>

 

 




