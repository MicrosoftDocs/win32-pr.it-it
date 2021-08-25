---
title: Esempio di CustomAccServer
description: Esempio di CustomAccServer
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ebf1ecde2821208d788b20b5cb0fc1a00403c1607fb4604eb92845daf49d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325990"
---
# <a name="customaccserver-sample"></a>Esempio di CustomAccServer

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Informazioni sul download](#download-information)
-   [Requisiti minimi](#minimum-requirements)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio viene illustrato come implementare un Microsoft Active Accessibility server per un controllo personalizzato semplice. L'oggetto accessibile per il controllo è costituito dall'elemento radice (una casella di riepilogo) e dai relativi elementi figlio (gli elementi elenco).

## <a name="download-information"></a>Informazioni sul download

L'esempio CustomAccServer viene installato come parte di [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) ed è disponibile nel percorso seguente.



| Località    | Percorso/URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Windows SDK | %Programmi% \\ Microsoft SDKs Windows \\ numero di versione Esempi \\ \[ \] \\ \\ winui \\ msaa |



 

## <a name="minimum-requirements"></a>Requisiti minimi



| Prodotto          | Versione                         |
|------------------|---------------------------------|
| Sistema operativo | Windows XP, Windows Server 2003 |
| Windows SDK      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio Visual Studio 2008:

1.  Eseguire lo strumento di configurazione Microsoft Windows Software Development Kit (SDK) fornito con l'SDK per aggiungere le directory di inclusione dell'SDK Visual Studio.
2.  Aprire Windows Explorer e passare alla directory del progetto.
3.  Fare doppio clic sull'icona per il file con estensione sln (soluzione) per aprire il progetto in Visual Studio.
4.  Scegliere **Compila** soluzione **dal** menu Compila per compilare la soluzione. L'applicazione verrà compilata nella \\ directory Debug o Release \\ predefinita.

Per compilare l'esempio dalla riga di comando, vedere Building Samples (Compilazione di esempi) nelle note sulla versione di Windows SDK nel percorso seguente: %Program Files% \\ Microsoft SDKs \\ Windows \\ v7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Per eseguire l'esempio:

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.
2.  Digitare AccServer.exe nella riga di comando oppure fare doppio clic sull'icona per AccServer.exe per avviarla da Windows Explorer.

Per eseguire da Visual Studio, premere F5 o scegliere **Avvia** debug dal menu **Debug.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi](samples.md)
</dt> </dl>

 

 




