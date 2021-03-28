---
description: Viene illustrato come controllare il comportamento di raggruppamento della barra delle applicazioni per le finestre di un'applicazione tramite la proprietà System.AppUserModel.ID.
title: Esempio di proprietà delle finestre ID modello utente applicazione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980343"
---
# <a name="application-user-model-id-appid-window-property-sample"></a>Esempio di proprietà della finestra ID modello utente applicazione (AppID)

Viene illustrato come controllare il comportamento di raggruppamento della barra delle applicazioni per le finestre di un'applicazione tramite la proprietà [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) .

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio viene illustrato come impostare la proprietà [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) tramite l'utilizzo dell'implementazione di [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) della finestra, ottenuta tramite [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio AppUserModelIDWindowProperty](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **AppUserModelIDWindowProperty** .
2.  Immettere `msbuild AppUserModelIDWindowProperty.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **AppUserModelIDWindowProperty** .
2.  Fare doppio clic sull'icona per il file AppUserModelIDWindowProperty. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Nella riga di comando, immettere `AppUserModelIDWindowProperty.exe` . In alternativa, in Esplora risorse fare doppio clic sull'icona per AppUserModelIDWindowProperty.exe.
3.  Per dimostrare l'effetto degli ID del modello utente dell'applicazione (AppUserModelIDs) sul raggruppamento della barra delle applicazioni, avviare almeno tre istanze dell'applicazione nello stesso momento.
4.  Usare il menu per impostare un AppUserModelID diverso in ognuna delle tre finestre. Si noti che ogni AppUserModelID separato genera un pulsante della barra delle applicazioni separato e che Windows può modificare la propria identità in fase di esecuzione.
5.  Impostare almeno due finestre sul secondo AppUserModelID. Si noti che entrambi si spostano nello stesso gruppo di barra delle applicazioni.
6.  Per aprire la **barra delle applicazioni e il menu Start** , fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere **Proprietà** dal menu di scelta rapida. Modificare i **pulsanti della barra delle applicazioni:** elenco a discesa tra le **combinazioni quando la barra delle applicazioni è piena** e **non combinare mai** i valori. Si noti che ogni finestra può ottenere un pulsante separato, ma che i pulsanti sono raggruppati in base a AppUserModelID.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ID modello utente applicazione (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 
